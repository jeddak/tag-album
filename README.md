# tag-album

A Zsh script to tag a set of audio files that comprise an album by a single artist.

Currently supports only .mp3 files.

* Dependencies
  - mid3v2
  - sed
  - zsh
  - zsh/mapfile

* Usage

        tag-album {artist} {album} {recording_date}

Execute this script in the same directory as an `album_titles.txt` file

`album_titles.txt` should be an ASCII or UTF-8 text file, where each line
contains the filename followed by a pipe ('|') and then the track title, like so:

```
path/name_of_file   |   track_title
```

You can include additional spaces before and after each pipe for better
readability; the spaces won't be included in the audio file tags.

Lines starting with '#' (comments) are ignored.

# Known Bugs

1. Filenames and track names cannot contain pipe characters
