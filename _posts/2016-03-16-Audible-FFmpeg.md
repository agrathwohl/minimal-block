---
layout: post
title:  "Make Audible Audio Files Work in Linux"
date:   2016-03-16 00:00:00
categories: tips
tags: ffmpeg, audio, audible, audiobook, drm
---

If you want to convert an Audible .aax file into a less restrictive file format, you can do so with ease using [FFmpeg](https://ffmpeg.org/), one of my all-time favorite free software projects.

Navigate to the directory where the .aax file is that you'd like to test on, and perform the following on the command line:

```
ffmpeg -activation_bytes 1CEB00DA -i test.aax -vn -c:a copy output.mp4
```

Doing this creates an mp4 container with only an AAC audio stream inside. By adding the `-c:a copy` argument, we're telling FFmpeg to do a stream copy of the audio, negating the need to compress and process the audio again. Since Audible audio is encoded at 64kbps HE-AAC or lower, this argument is essential!

This MP4 can now be played on any conventional audiovisual playback software that supports the MP4 container file and the HEv1 AAC codec format. Enjoy!
