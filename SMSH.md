# SMSH: a piano smash for the Machinedrum

SMSH is a custom USR machine for the Elektron Machinedrum running the community **X.20** firmware ([MDX](https://github.com/jmamma/MDX)). It plays an upright piano being hit: with a sledgehammer, a fist on the keys, a bar on the strings inside, a drop to the floor, or wood splintering.

Each trigger plays the whole event. A short knock and crack from the hit itself, then a cluster of strings ringing out, with unison pairs beating against each other, and a soft wash of sympathetic strings when the pedal is down. Strings sometimes snap. With the dampers on, the case gives a short thump instead.

The behaviour was fitted to recordings of pianos being hit and smashed. No recordings are in the machine: everything it plays is synthesised.

**Download: [SMSH.syx](https://github.com/SamplesAndSnacks/machinedrum-rasp/raw/main/SMSH.syx)** (version 0.1, 18,706 bytes; SHA-256 `92f918ae0ded858b575a3bf29f0848659edcc870a3a5fb1fedb953ed46a7e0b6`)

## Requirements

- Any Machinedrum (MKI or MKII, UW or non-UW) on **X.20**. SMSH does not use the sample banks, so UW isn't needed.
- One free slot in the machine bank. SMSH is a large machine (4,884 words of the 14,052 that X.20 shares between all installed machines).

## Install

With any SysEx tool (for example Elektron's C6, SysEx Librarian or MIDI-OX):
1. On the Machinedrum, open the machine manager (**FUNC + GLOBAL → FILE → MACHINE MGR**), choose an empty slot and select **RECV**.
2. Send `SMSH.syx` from your SysEx tool.
3. SMSH appears in the machine list as **PNO-SM**. Press **FUNC + YES** to audition it.

Back up your Machinedrum before installing any third-party machine. You install it at your own risk.

## Controls

| Knob | What it does |
|---|---|
| **HIT** | What hits it: **sledgehammer** (0-25), **fist on the keys** (26-50), **metal inside** (51-76), **drop / slam** (77-101), **splinter** (102-127) |
| **HARD** | How hard: soft to very hard |
| **PTCH** | The centre of the struck cluster, about 45 to 450 Hz |
| **SPRD** | How many notes the cluster covers: from one note up to about 4 octaves |
| **PEDL** | Dampers on (short, dead) to pedal down (long ring and wash) |
| **NOIS** | The hit noise: the knock, crack and thump of the impact, from full (127) down to none (0) |
| **SNAP** | How often a string snaps and slides down in pitch |
| **BODY** | The case: light to heavy, with a floor thump at the top |

**Default:** HIT 19 (sledgehammer), HARD 100, PTCH 28, SPRD 41, PEDL 97, NOIS 127, SNAP 0, BODY 109.

Each trigger is different, as a real hit would be, but the notes are locked to PTCH and SPRD, so the same settings give the same cluster.

## Performance

SMSH declares 3,950 of the 3,951 DSP cycles a USR machine may use per block, and that figure covers its worst case. It has been tested on hardware on X.20 B with SMSH on all 16 tracks and a trig on every step.

The hit sounds at once; the strings join about 17 ms later, while the machine sets them up (for a few PTCH and SPRD settings, about 1.5 ms later still). With NOIS turned down, that short gap before the strings is easier to hear.

## Notes

- SMSH is self-contained: everything it plays is built into the machine.
- Built with assistance from AI coding tools, and tuned by ear.
- Not affiliated with Elektron or with the MDX firmware project.

## Licence

SMSH is released under the [MIT licence](LICENSE): you're free to use, share and redistribute it, on its own or bundled with other machines, as long as the licence notice goes with it.
