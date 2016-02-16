mkv-remove-language
==================

A BASH script that removes the audio track with the specified language from a matroska file.

Requires mkvmerge

Usage:  
`chmod +x mkv-remove-language`
`./mkv-remove-language "My File.mkv" "eng"`
This will create a new file called "My File [without eng].mkv".

For batch processing all .mkv files in the current directoy copy mkv-remove-language to a directory in your PATH and execute:
`find -iname "*.mkv" -exec mkv-remove-language '{}' "lang" \;`
