sh-flac
=======

Set of shell utilities to manage [FLAC](https://en.wikipedia.org/wiki/FLAC) collections. Each takes advantage of multi-core systems where possible.

Utilities
---------

<pre>flacmp3</pre>
Uses [ffmpeg](https://en.wikipedia.org/wiki/FFmpeg) to convert the FLAC files in the current directory to MP3, placing the new files in their own directory for easy transfer to external players. Quality settings, or indeed output format, easily changed.

<pre>flactest, flactest-sub</pre>
Runs a test decode on all FLACs found in the current directory and below, printing the names of any that have errors.

<pre>reflac</pre>
Reencode all FLACS in the current directory and below to maximum compression. As FLAC is lossless and has a fixed binary format, this will not affect any downstream file consumers. It will simply reduce the file size, where possible. Before/After size measurements are printed on completion.

<pre>rgflac</pre>
Builds a list of all FLACS in the current directory and below, and feeds them to 'metaflac' such that it can calculate the __album__ [replaygain](https://en.wikipedia.org/wiki/ReplayGain). This gives albums a more consistent volume than simply processing the files in isolation.

<pre>music-clean</pre>
Simple whitelist of desired file extensions. Will print out the paths of any _undesirable_ files found in the current directory, and below.
