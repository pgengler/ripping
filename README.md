# ripping
These are various scripts for ripping video from DVD/BD sources.

## Dependencies
* [HandBrake CLI](https://handbrake.fr/)
* `lsdvd`
* [makemkv](http://www.makemkv.com/) [for BD sources]

## The Scripts
### rip-bd
This script encodes the output file from `makemkv` from a Blueray disc into an MP4.

Usage: `rip-bd <makemkv file> <output filename>`

### rip-dvd
This script is used to rip the main feature from a DVD.

Usage: `rip-dvd <filename>.mp4`

This rips the main feature from the disc in the drive referenced by /dev/dvd to a file called `filename.mp4`.

### rip-tv
This script rips TV episodes from a DVD disc.

Usage: `rip-tv <basename>`

This rips all titles with a length between 20 and 120 minutes from the disc in /dev/dvd. Output files are named `basename-#.mp4`, where # is the number in the sequence (1 for the first, 2 for the second, etc.). This is usually, but not always, the same order as the episodes on the disc.
Run `rip-tv --usage` for more information about other available options.

### rip-tv-ep
This script rips a single title from a disc; it's meant for ripping a single episode of a TV show on a DVD.

Usage: `rip-tv-ep <title #> <basename>`

This script isn't well-documented so I'm not entirely sure what it's real-world use is,
