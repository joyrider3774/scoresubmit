# scoresubmit
Repo containing code to submit scores to your own created leaderboards on https://scores.joyrider3774.xyz with QR Codes or directly

## Leaderboards
I expanded a [site](https://scores.joyrider3774.xyz) someone created on github to submit score so you can create your own leaderboards and let people submit scores to them by generating QR Codes, or doing http calls.
It originated from an idea i proposed on playdate discord.

## Score Submitting Support
These list code / devices where there is code for submitting scores to the leaderboard site along with information and changes i did to libs used.

### Playdate
Works by creating a QR code that people can scan using their phone.
You can see my [Formula 1](https://github.com/joyrider3774/formula1_playdate) game source code to see an example C Api implementation

In theory someone could export these functions to LUA SDK but i don't use LUA so feel free to submit a PR if needed

| Libs used | License | Changes|
|-----|---------|--------|
| [Teeny SHA-1](https://github.com/CTrabant/teeny-sha1) | MIT | commented snprintf statements to generate hex string (snprintf does not work on playdate) |
| [QR Code generator library](https://www.nayuki.io/page/qr-code-generator-library) | MIT | replaced assert statements with if statements (assert does not work on playdate) |
| [HMAC-SHA1](https://github.com/h5p9sl) | Public Domain / Unlicense | Code was made for sha256-HMAC, adapted with minor changes to make it work for SHA1-HMAC |
| [BASE64 Encoder](https://web.mit.edu/freebsd/head/contrib/wpa/src/utils/) | BSD License | no changes |
| [URLEncode function](https://gist.github.com/jesobreira/4ba48d1699b7527a4a514bfa1d70f61a) | ??? | no changes |



