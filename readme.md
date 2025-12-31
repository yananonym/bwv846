# BWV846 < 1kB

Two implementations of Bach's Prelude in C Major BWV 846 from the first book of Das Wohltemperierte, one in 12-TET and one in 5-limit tuning. Each renders as a complete audio waveform in a single click via Web Audio API from less than 1kB of code.

## Implementation

The encoding strategy compresses pitch data through a Hamiltonian path of intervals mapped to ASCII characters. Each character encodes a just intonation ratio without escape sequences, reducing what would require explicit arrays into single symbols. The full pitch palette occupies minimal space. A variant optimized for alternative tuning goals would require a distinct Hamiltonian path calculation.

Synthesis renders pitches as sine waves with rectangular amplitude envelopes. The rhythmic structure preserves note durations from the original score, with sustained notes in the lower voices and staccato in the right hand's part. The semi-random rhythmic quality produced by rectangular envelopes, where clicks occur at waveform resets, proved aesthetically preferred and was chosen over smooth alternatives.

## Files

| File | Date | Tuning | Concert Pitch |
|------|------|--------|---------------|
| BWV846_12edo.html | 2025-10-30 | 12-TET | A=440Hz |
| BWV846_5limit.html | 2025-10-31 | 5-limit | A=415Hz |

## Run It

Open an HTML file in any browser as of 2025 supporting ES6 JavaScript, Web Audio API, and Float32Array. Click anywhere to generate and play the prelude once.

## Notes

Both tunings function as viable implementations of their respective frameworks. Neither represents subjective optimal tuning, nor any of the temperaments used by Bach.

The project executed from 2025-10-28 through 2025-10-31, though the concept remained dormant for considerably longer.

## License

GNU General Public License v3.0 or later. Attribution required.

---

The code is the specification.
