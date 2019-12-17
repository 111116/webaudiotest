# web audio mp3 decode test

[live demo](https://111116.github.io/webaudiotest/)

## What this page does

It loads, decodes and plays an mp3 file using `AudioContext`. The mp3 contains 9 identical, evenly timed click sounds.

For comparison, A wave file is also played several times. The first time starts at the same time when the mp3 playback starts. Ideally it should perfectly match the mp3 sound.

It can be easily heared whether the mp3 & wav are synchonized. You can also use Audacity to record & visualize the result. Also compare the result using different browsers.

## Explanation

The mp3 was encoded with LAME, which introduces a delay and an info frame that describes the delay. A decoder that supports the LAME tag should skip that delay & the info frame.

See [LAME Technical FAQ](https://lame.sourceforge.io/tech-FAQ.txt).
[Alternative link](https://web.archive.org/web/20180116235404/http://lame.sourceforge.net/tech-FAQ.txt)

It turns out in this test that some web audio implementations are not using the LAME tag.
