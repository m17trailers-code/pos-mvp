# Chapter Streak

A Duolingo-style app for reading books: one short passage at a time, on a
lesson path, with a daily streak, XP, hearts and exercises that check you
actually took the passage in.

Single self-contained `index.html` — no build step, no server, no dependencies.
Open the file in a browser, or serve the folder with any static server.

```
npx serve chapter-streak
```

## How it works

**Any plain text becomes a course.** Paste text or load a `.txt` file. The text
is split into paragraphs and sentences and grouped into passages of about 110
words — roughly a minute of reading each. Project Gutenberg header and licence
blocks are trimmed automatically.

**Exercises are generated from the passage**, so a book you bring needs no
authoring:

| Exercise | How it is built |
| --- | --- |
| Fill the gap | A distinctive word is blanked from one sentence. The three decoys are real words pulled from neighbouring passages, matched to within three characters of the answer's length. |
| Put these back in order | Three consecutive sentences from the passage, shuffled. |

Generation is seeded from the book id and passage number, so the same passage
always produces the same exercises.

**Progression.** Passages unlock in order. A mistake costs a heart; five
mistakes ends the session with no credit for that passage, and hearts refill
the next day or for 50 XP. Finishing a passage awards 4 XP per correct answer
plus 8 for a clean run, extends the day streak, and adds to your words-read
total. A perfect passage is marked with a star on the path.

All state lives in `localStorage` under `chapter-streak/v1` — nothing is
uploaded, and books stay on the device that imported them.

## The cast

Four original characters, drawn as inline SVG so they animate, scale and
re-theme with the palette. They are not decoration — each one owns a moment:

| Who | What they are | When they appear |
| --- | --- | --- |
| **Wick** | A stub of candle | Greets you on the shelf with your streak, stands beside the live node, confirms right answers, fronts the results card |
| **Nib** | A quill pen | Sets every question |
| **Marge** | A bookworm | Reads alongside you during the passage |
| **Blot** | A spill of ink | Turns up on wrong answers and when you run out of hearts, and blames himself |

Lines are pooled per moment and never repeat twice in a row. Blot's excuses
differ for a missing word and a scrambled order.

Idle motion (breathing, blinking, a flickering flame), reactions (cheer,
wobble, peek), speech-bubble pops, staggered shelf and path entrances, a stamp
on the node you just earned, counting-up XP, and short WebAudio blips — no
audio files — with a mute toggle in the header. Everything respects
`prefers-reduced-motion`.

## Content

The bundled sample story, *The Lamplighter's Almanac*, is original writing
included so the app has something real to read on first launch. No third-party
book text ships with the app; anything else comes from the file you import.

## Known limits

- Word detection is Latin-alphabet only. Non-Latin scripts read fine but will
  not produce good fill-the-gap exercises.
- Sentence splitting is heuristic (it knows common abbreviations and initials);
  unusual punctuation may occasionally merge two sentences into one.
- `localStorage` caps out around 5 MB. A very long book is refused with a
  message rather than silently failing — remove a book or import a shorter text.
- Reading position within a single passage is not saved; leaving mid-passage
  restarts that passage.

## Tests

`npm ls -g playwright` provides the browser driver used by the smoke scripts
during development: they drive shelf → path → read → exercises → results,
verify persistence across reload, the import flow, and the out-of-hearts path.
