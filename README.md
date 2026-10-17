# RASP: a trill machine for the Machinedrum

RASP is a custom USR machine for the Elektron Machinedrum running the community **X.20** firmware ([MDX](https://github.com/jmamma/MDX)). It plays a blown raspberry: a trill.

The core of the sound is a stream of short closure clicks, cut from real recordings, and timed by a small breath model. The model sets how hard you blow, how long the breath lasts, and whether it buzzes steadily or breaks up. RUFF sweeps from a dark, steady, harmonic **buzz** to a bright, broken **sputter** that stalls and pops.

**Download: [RASP.syx](https://github.com/SamplesAndSnacks/machinedrum-rasp/raw/main/RASP.syx)** (version 0.1, 15,666 bytes; SHA-256 `482300c133eb82607921e52108f81d141f7f2797236d41f71019f17d957ca6b8`)

## Requirements

- Any Machinedrum (MKI or MKII, UW or non-UW) on **X.20**. RASP does not use the sample banks, so UW isn't needed.
- One free slot in the machine bank.

## Install

With any SysEx tool (for example Elektron's C6, SysEx Librarian or MIDI-OX):
1. On the Machinedrum, open the machine manager (**FUNC + GLOBAL → FILE → MACHINE MGR**), choose an empty slot and select **RECV**.
2. Send `RASP.syx` from your SysEx tool.
3. RASP appears in the machine list as **RSP-LV**. Press **FUNC + YES** to audition it.

Back up your Machinedrum before installing any third-party machine. You install it at your own risk.

## Controls

| Knob | What it does |
|---|---|
| **TRIL** | Trill rate: from slow, separate claps (~30 per second) up to a tight squeak (~300) |
| **PUFF** | How much breath: from a short puff to a long one (about 0.1 to 2.5 s) |
| **BLOW** | How hard. Low settings are mostly breath, with only a faint buzz. |
| **RUFF** | Steady buzz → broken sputter |
| **SPIT** | Wet clicks |
| **BODY** | Dark → bright |
| **AIR** | Breath noise riding on each opening |
| **CUP** | Resonance |

**Default:** TRIL 46, PUFF 71, BLOW 127, RUFF 101, SPIT 103, BODY 56, AIR 0, CUP 127.

Each trigger is slightly different, as a real one would be. Try p-locking TRIL and RUFF across a pattern.

## Performance

RASP declares 3,900 of the 3,951 DSP cycles a USR machine may use per block, and that figure covers its worst case. It has been tested on hardware on X.20 B with RASP on all 16 tracks at its heaviest settings, with a trig on every step, and ran without glitches.

A new trigger takes about 1.5 ms (two blocks) before the sound starts.

## Notes

- RASP is self-contained: everything it plays is built into the machine.
- Built with assistance from AI coding tools, and tuned by ear.
- Not affiliated with Elektron or with the MDX firmware project.

## Licence

RASP is released under the [MIT licence](LICENSE): you're free to use, share and redistribute it, on its own or bundled with other machines, as long as the licence notice goes with it.
