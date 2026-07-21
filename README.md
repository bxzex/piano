# Piano — a machine for playing

A single-file, offline-capable web piano with a hand-built synthesis engine and a Swiss-editorial / neo-brutalist interface. No frameworks, no samples, no build step — just open `index.html`.

**▶ Live: https://bxzex.github.io/piano/**

---

## Features

- **Six voices** — Grand, Soft/Felt, Bright, Honky-Tonk, Electric (Rhodes-style) and Harpsichord, each built from its own set of decaying partials.
- **Real synthesis, not samples** — additive partials with per-harmonic decay, string *inharmonicity* (upper partials stretched slightly sharp, like a real soundboard), a hammer-noise attack transient, a convolution reverb built from generated noise, plus a master compressor.
- **Live console** — Volume, Brightness (filter cutoff), Reverb, Attack and Release sliders that shape the sound in real time.
- **Learn a song** — step mode glows the next key and waits for you to play it (previewing the following note in a lighter shade); demo mode auto-plays with a progress bar. Includes Twinkle Twinkle, Ode to Joy, Happy Birthday, Jingle Bells and the intro to Für Elise.
- **Play it your way** — mouse/touch on any key, or your computer keyboard across the centre two octaves.
- **Fully offline** — everything is synthesised in the browser via the Web Audio API. The only network request is for the display fonts, which fall back to system serif/mono if unavailable.

## Playing with the keyboard

| | Keys |
|---|---|
| **White** | `A S D F G H J K L ; '` |
| **Black** | `W E T Y U O P` |
| **Sustain** | hold `Space` |

Click a key once to start — browsers require a first interaction before audio can play.

## Run it locally

```bash
git clone https://github.com/bxzex/piano.git
cd piano
open index.html      # macOS — or just double-click the file
```

That's it. There is nothing to install.

## How it's built

Everything lives in **one `index.html`** — markup, styles and script.

- **Sound** — the `VOICES` table defines each instrument as harmonic ratios with individual gains and decay times; `play()` wires an oscillator + gain per partial through a low-pass filter into dry/reverb buses.
- **Songs** — stored as `[note, beats]` sequences; the demo player and step-through learner both read from the same data.
- **Design** — bone-paper canvas, heavy ink borders, hard offset shadows and a single vermillion accent. Type is *Fraunces*, *Space Grotesk* and *Space Mono*.

## License

MIT — do whatever you like with it.
