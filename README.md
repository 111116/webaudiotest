# web audio mp3 decode test

[live demo](https://111116.github.io/webaudiotest/)

## Explanation

The mp3 was encoded with LAME, which introduces a delay and an info frame that describes the delay. A decoder that supports the LAME tag should skip that delay & the info frame.

See [LAME Technical FAQ](https://lame.sourceforge.io/tech-FAQ.txt).
[Alternative link](https://web.archive.org/web/20180116235404/http://lame.sourceforge.net/tech-FAQ.txt)

It turns out in this test that some web audio implementations are not using the LAME tag.
