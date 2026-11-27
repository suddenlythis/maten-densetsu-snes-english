# Installing the Legend of Maten English translation (v1.0)

The download contains only the changes to the game, not the game. You need your own ROM of
Maten Densetsu - Senritsu no Ooparts (Japan) for the Super Famicom.

## What you need

- The ROM **Maten Densetsu - Senritsu no Ooparts (Japan)**. It must be exactly:

  | Size | CRC32 | SHA-1 |
  |---|---|---|
  | 3,145,728 bytes | `0F02330F` | `64d3f337e06fa33eb012c98169426a92e4058f1f` |

  With any other file the patch refuses to apply. If your file is 512 bytes larger
  (3,146,240 bytes), it has a copier header: remove it first, for example with the
  "remove header" option of your patcher.
- A BPS patcher: Floating IPS (Flips), or Rom Patcher JS, which runs in a web browser.
- A Super Famicom emulator. Tested in Mesen 2.1.1.

## What is in the zip

| File | What it is |
|---|---|
| `MatenDensetsu-EN-v1.0.bps` | The patch |
| `README.txt` | What the patch is, how to install it, and what was tested |

## How to apply

### With Floating IPS

1. Start Flips and choose Apply Patch.
2. Select `MatenDensetsu-EN-v1.0.bps`.
3. Select your ROM.
4. Choose a name for the new file, for example `Legend of Maten (English).sfc`.

Your original ROM is not changed.

### With Rom Patcher JS

1. Open Rom Patcher JS in a web browser.
2. ROM file = your ROM. Patch file = `MatenDensetsu-EN-v1.0.bps`.
3. Apply patch, and save the file it offers.

### With the command line

```
flips --apply MatenDensetsu-EN-v1.0.bps "Maten Densetsu - Senritsu no Ooparts (Japan).sfc" "Legend of Maten (English).sfc"
```

### Check the result

The patched ROM is:

| Size | CRC32 | SHA-1 |
|---|---|---|
| 4,194,304 bytes | `5CFC6DA1` | `abb502dcd1a1656c46f3cffbbf6c502ff08d8366` |

It is 1 MB larger than the original. That is expected: the English text is stored in the
added space.

## After patching

Start a new game. A save made with the Japanese game keeps its names in Japanese letters,
and was not tested with the patch. An emulator save state made with the Japanese game keeps
the old program in memory, so load the game normally instead.

Controls: A confirms, B cancels, X opens and closes the status menu on the field, Y shows
the radar, Select opens the config screen. On the name-entry screen, X changes between the letters page and
the two kana pages, and Start jumps to OK.

On the save screen and the "Save?" question the cursor starts on CANCEL or No: press Up
first.

## Tested on

Mesen 2.1.1. Not tested in other emulators or on real hardware.
