# Piano

A piano you play in the browser. There are no recordings in it: every note is built from scratch while you play.

Play: https://bxzex.github.io/piano/

Each of the six voices is a set of harmonics that fade at their own rates. The voices are grand, felt, bright, honky-tonk, electric and harpsichord. I stretched the upper harmonics slightly sharp the way real strings are, and added a little hammer noise at the start of each note. The reverb is generated too. Sliders for volume, brightness, reverb, attack and release change the sound as you play.

To learn a song, step mode lights up the next key and waits for you. Demo mode plays it for you. It knows Twinkle Twinkle, Ode to Joy, Happy Birthday, Jingle Bells and the opening of Für Elise.

## Keyboard

| | Keys |
|---|---|
| White keys | `A S D F G H J K L ; '` |
| Black keys | `W E T Y U O P` |
| Sustain | hold `Space` |

Click once first. Browsers won't play sound until you do.

## Running it

It's one `index.html` with no build step. Clone it and open the file. It works offline too, apart from the fonts, which fall back to system ones.

MIT licensed. Made by [bxzex](https://bxzex.com).
