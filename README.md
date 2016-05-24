This snippet is meant to be used for optimizing video on a WebKit-based browser, with very low bandwith.
It is not meant to be used (or reused).

# Install FFMpeg
If you don't have FFMpeg installed and you are using Ubuntu, [you can install everything in this way](https://trac.ffmpeg.org/wiki/CompilationGuide/Ubuntu)

# Install

```
$ pip install -r requirements.txt
$ chmod u+x optimizer.py
```

# Usage

FFMpeg is configured out of the box to use 1.5x number of cores (using `libx264`).
If you use it on machine with high number of CPU, you can spawn multiple instances of FFMpeg using the worker option.

```
$ ./optimizer.py --workers=1 --source=/path/to/video
```