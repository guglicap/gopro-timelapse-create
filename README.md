# gopro-timelapse-create

A simple Bash script to generate GoPro timelapse videos from images.
Tested with a GoPro Hero Plus.

```
Usage: gopro-timelapse-create [options] [image-dir] [out-file]
    Generate timelapse video from GoPro images. image-dir defaults to current directory if not specified.
    
    Options:
        -h, --help: show this message.
        -n, --dry-run: do nothing, print out the commands which would be invoked instead.
        -sn, --start-number <start_number>: number of the first image which should be part of the video. defaults to the first one in alphabetical order.
        --scale <w:h>: scale the frames to width w and height h. can also be relative, e.g. '--scale iw*.5:ih*.5'. refer to https://trac.ffmpeg.org/wiki/Scaling for further details.
        --ffmpeg-options <options>: set ffmpeg encode options. refer to ffmpeg documentation.
        --ffmpeg-options-append: append these options to the default ffmpeg options.
            default options: ${FFMPEG_OPTS}
```
