# KOOK: a laughing kookaburra for the Machinedrum

KOOK is a custom USR machine for the Elektron Machinedrum running the community **X.20** firmware ([MDX](https://github.com/jmamma/MDX)). It plays a laughing kookaburra.

Each trigger plays a whole call, from a single "ha" up to the full laugh: low chuckles, a run of rising "ha" notes, then a wind-down. Every note is a pitch-synchronous pulse with breath noise and the period doubling that gives a real laugh its rasp, shaped by a small beak filter. KOOK is one bird. For a chorus, put KOOK on a few tracks with different PTCH and VARI settings and let them overlap.

The note timing, pitch contours, harmonics and roughness were measured from field recordings of laughing kookaburras. No recordings are in the machine: everything it plays is synthesised.

**Download: [KOOK.syx](https://github.com/SamplesAndSnacks/machinedrum-rasp/raw/main/KOOK.syx)** (version 0.1, 10,360 bytes; SHA-256 `15b095217ff0e866d28431f0baf568cfdb553746c32aadb33cf33a15cb8c33a0`)

## Requirements

- Any Machinedrum (MKI or MKII, UW or non-UW) on **X.20**. KOOK does not use the sample banks, so UW isn't needed.
- One free slot in the machine bank.

## Install

With any SysEx tool (for example Elektron's C6, SysEx Librarian or MIDI-OX):
1. On the Machinedrum, open the machine manager (**FUNC + GLOBAL → FILE → MACHINE MGR**), choose an empty slot and select **RECV**.
2. Send `KOOK.syx` from your SysEx tool.
3. KOOK appears in the machine list as **BRD-KK**. Press **FUNC + YES** to audition it.

Back up your Machinedrum before installing any third-party machine. You install it at your own risk.

## Controls

| Knob | What it does |
|---|---|
| **PTCH** | Pitch of the bird |
| **CALL** | Which call: **HA** (0-31, one note), **CHUK** (32-63, a chuckle), **HAHA** (64-95, a run of ha notes), **LAFF** (96-127, the full laugh) |
| **LEN** | Call length: how many notes |
| **RATE** | Note rate |
| **ARCH** | How far each note's pitch rises and falls |
| **RASP** | Roughness: smooth to raspy |
| **BEAK** | Beak size: the vowel of the notes |
| **VARI** | How much each call varies in timing, pitch and level |

**Default:** PTCH 35, CALL 79 (HAHA), LEN 89, RATE 68, ARCH 127, RASP 109, BEAK 64, VARI 56.

Each trigger is different, as a real bird's would be. Knob changes take effect from the next note.

## Performance

KOOK declares 3,900 of the 3,951 DSP cycles a USR machine may use per block, and that figure covers its worst case. It has been tested on hardware on X.20 B with KOOK on all 16 tracks and a trig on every step.

A new trigger takes about 3 ms (four blocks) before the first note.

## Notes

- KOOK is self-contained: everything it plays is built into the machine.
- Built with assistance from AI coding tools, and tuned by ear.
- Not affiliated with Elektron or with the MDX firmware project.

## Licence

KOOK is released under the [MIT licence](LICENSE): you're free to use, share and redistribute it, on its own or bundled with other machines, as long as the licence notice goes with it.
