# mkv-bash-tools

[![Issue Count](https://codeclimate.com/github/HessiJames/mkv-bash-tools/badges/issue_count.svg)](https://codeclimate.com/github/HessiJames/mkv-bash-tools)


## mkv-transcode-flac

A BASH script that transcodes all FLAC tracks of a matroska file to Ogg Vorbis while preserving the track's name and language and it's default and forced flags as well as its delay.

![Screen shot of mkv-transcode-flac](mkv-transcode-flac.png)

### Depends on

mktemp  
mkvmerge  
mkvextract  
oggenc (with FLAC decoder enabled)

### Usage

`chmod +x mkv-transcode-flac`  
`./mkv-transcode-flac "My File.mkv"`  
This will create a new file called "My File [Ogg Vorbis].mkv".

For batch converting all .mkv files in the current directoy copy mkv-transcode-flac to a directory in your PATH and execute:  
`find -iname "*.mkv" -exec mkv-transcode-flac '{}' \;`


## mkv-remove-language

A BASH script that removes the audio track with the specified language from a matroska file.

### Depends on

mkvmerge  

![Screen shot of mkv-remove-language](mkv-remove-language.png)

### Usage

`chmod +x mkv-remove-language`  
`./mkv-remove-language "My File.mkv" "eng"`  
This will create a new file called "My File [without eng].mkv".

For batch processing all .mkv files in the current directoy copy mkv-remove-language to a directory in your PATH and execute:  
`find -iname "*.mkv" -exec mkv-remove-language '{}' "lang" \;`


## mkv-extract-subtitles

A BASH script that removes the audio track with the specified language from a matroska file.

### Depends on

mkvmerge  
mkvextract  

![Screen shot of mkv-extract-subtitles](mkv-extract-subtitles.png)

### Usage

`chmod +x mkv-extract-subtitles`  
`./mkv-extract-subtitles "My File.mkv"`  
This will create a new file for each subtitle in the current directory.

For batch processing all .mkv files in the current directoy copy mkv-extract-subtitles to a directory in your PATH and execute:  
`find -iname "*.mkv" -exec mkv-extract-subtitles '{}'\;`
