---
layout: post
title: "Convert mp3 files to ogg"
date: 2013-07-05 14:10
comments: true
categories: 
- code
- open source
- bestof
---

I have never expected this to be hard. Sure it won't be difficult to do this in 2013. But after sinking almost 1 hour into this, I decided to write it down hoping that it might save other people a bit time. 

So I started with [sox](sox.sourceforge.net/). I tried `sox zit.mp3 zit.ogg` and received an error message
> sox FAIL formats: no handler for file extension `ogg'. 

Then I tried `dir2ogg -q7 zit.mp3` which was recommended by a post on Ubuntu's discussion forum. But unfortunately, it still didn't work out. Here is the error message I got: 

> dir2ogg 0.11.8 (2009-08-04), converts audio files into ogg vorbis.
> 
> WARNING: Mutagen failed on zit.mp3, no tags available
> Traceback (most recent call last):
> ID3NoHeaderError: 'zit.mp3' doesn't start with an ID3 tag
> 
> INFO: Converting "zit.mp3" (using mpg123 as decoder)...
> [wav.c:143] error: cannot even write a single byte: Illegal seek
> [audio.c:630] error: failed to open audio device
> [mpg123.c:902] error: Failed to initialize output, goodbye.
> ERROR: Cannot open output file "zit.ogg": Permission denied
> WARNING: No tags found...
}}}

After much fiddling around, this is the final solution that was working for me. To chain `mpg123` and `oggenc` together. `mpg123` will generate a `.wav`  file to the standard output, which `oggenc` takes in and emit a corresponding `ogg` file. 

`for i in *.mp3; do mpg321 $i -w - | oggenc -q7 -o ${i/mp3/ogg} -; done`

A few caveats: 

- `$i` is the filename and `${i/mp3/ogg}` changes the output filename. 
- `-q7` select a level-7 sound quality. Since both mp3 and ogg are lossy sound format, converting one to another with the same sample rate would only decrease the sound quality. By specifying a higher bit rate, the `ogg` output would sound similar to the `mp3` file. 
- The `-` are quite important. 
- On Ubuntu/Debian, you might need to install the packages using `sudo apt-get install mpg321 vorbis-tools`
