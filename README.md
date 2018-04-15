# pyshuff

An inexact clone of GNU shuf. Free, implemented in Python.

### Install

### Usage

Same as shuf, but the script is invoked with pyshuf. Read the [GNU
manual](https://www.gnu.org/software/coreutils/manual/html_node/shuf-invocation.html)
for shuf for more details. I haven't used shuf -- I wrote this because it
didn't come standard on MacOS.

### "Cookbook" 

Generate a random number from 0 to 99

     $ pyshuf -i 0-99 -n 1
     73

Pick a random word from the dictionary (dictionary location may vary)

     $ pyshuf --input-file /usr/share/dict/words -n 1
     irreflectiveness

Shuffle the first 10 words from the dictionary

     $ head /usr/share/dict/words | pyshuf
     aardvark
     aalii
     Aaron
     a
     aa
     Aani
     aam
     aardwolf
     A
     aal

Use input from the command line

     pyshuf: error: argument -e/--echo: ignored explicit argument 'cho'
     $ pyshuf --echo one two three four five
     four
     two
     three
     one
     five

### Implemented

    --e, --echo
    -i, --input-range
    -n, --head-count

### Not implemented

    -o, --output-file
    --random-source
    -r, --repeat
    -z, --zero-terminated

### Added

    --input-file	specify an input file to read from
