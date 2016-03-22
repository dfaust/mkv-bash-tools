mkv-transcode-flac
==================

A BASH script that transcodes all FLAC tracks of a matroska file to Ogg Vorbis while preserving the track's name and language and it's default and forced flags.

Requires mktemp, mkvmerge, mkvextract and oggenc (with FLAC decoder enabled)

![Screen shot of mkv-transcode-flac](mkv-transcode-flac.png)

Usage:  
`chmod +x mkv-transcode-flac`  
`./mkv-transcode-flac "My File.mkv"`  
This will create a new file called "My File [Ogg Vorbis].mkv".

For batch converting all .mkv files in the current directoy copy mkv-transcode-flac to a directory in your PATH and execute:  
`find -iname "*.mkv" -exec mkv-transcode-flac '{}' \;`
