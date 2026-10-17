# ELRSVoices — Custom EdgeTX Voice Packs

A set of alternative voice packs for EdgeTX radios (tested on the RadioMaster Boxer).
Choose the character you fancy, drop it onto your SD card, and your radio starts
talking in a whole new voice.

Every pack is a complete drop-in replacement: it covers the radio's system sounds
(numbers, units, telemetry events) as well as the model sounds (arming, flight modes,
rates, alerts, and more), so nothing is left out.

---

## The characters

### Alice — the clean baseline
- **Voice:** `af_heart` (calm US female)
- **Vibe:** Clear, neutral and easy to understand. Stock EdgeTX wording, nothing added.
- **Best for:** Anyone who wants a tidy, dependable voice with no personality getting in the way.

### Gaby Gimbals — the excitable race commentator
- **Voice:** `af_sky` (bright US female), delivered fast
- **Vibe:** Hyper-energetic track announcer. Punchy and quick, with a playful streak —
  she is not above teasing you for flicking on a beginner mode.
- **Best for:** Racing, quick telemetry callouts, and anyone who wants their radio to
  sound like it just spotted the leader on the last lap.
- **Sample:** *"Angle mode. Aww. Look who needs training wheels."*

### Rupert Stone — the grumpy flight instructor
- **Voice:** `bm_george` (British male), delivered slowly and wearily
- **Vibe:** A tired, cutting, sarcastic old flight instructor who has seen it all and
  is thoroughly unimpressed. He does not suffer fools gladly.
- **Best for:** Pilots who respond better to withering disdain than to encouragement.
- **Sample:** *"Battery low. Land now, you idiot."*

### Clover — the stealthy whoop pilot
- **Voice:** `af_nicole` (hushed US female whisper)
- **Vibe:** A cheeky, whisper-soft accomplice for guerrilla whoop missions. She urges
  you to stay quiet and not get caught, but she will absolutely poke fun at you when
  you fumble a mode. Encouraging on the surface, gently mocking underneath.
- **Best for:** Stealthy FPV runs, sneaking around the neighbourhood, and anyone who
  wants their radio to feel like a co-conspirator rather than a passenger.
- **Samples:** *"Angle mode. Come on. You are better than this."* /
  *"Turtle mode on. I hope this works."* / startup: *"Welcome to EdgeTX, shhhh."*

---

## Installing a pack

1. Power off the radio and remove the SD card (or connect it to your computer).
2. Open the folder for the character you want, for example `GabyGimbals/`.
3. Copy its contents onto the SD card so the files end up in these locations:

   ```
   SD:/SOUNDS/en/*.wav           <- the .wav files in the character folder
   SD:/SOUNDS/en/SYSTEM/*.wav    <- the .wav files in its SYSTEM folder
   ```

   Back up your existing `SOUNDS/en` folder first if you want to keep the stock voice.

4. Put the SD card back in the radio and switch it on.
5. In the radio settings, make sure the voice language is set to **English** so it
   uses these sounds.

To swap between characters, just overwrite the same `SOUNDS/en` files with another
character's folder. Only one pack is active at a time.

---

## What's inside each pack

Each character folder contains:

```
<Character>/
├── *.wav            # 356 model / play-track sounds
└── SYSTEM/
    └── *.wav        # 212 system sounds
```

- **Model sounds** — arming, flight modes, rates, flaps and gear, VTX, telemetry
  alerts, and the various multiscript sounds used by Betaflight/INAV Lua tools.
- **SYSTEM sounds** — spoken numbers, decimals, units (volts, amps, RPM, and so on)
  and system events such as low battery, telemetry lost, and throttle/switch warnings.

All files are 16 kHz mono 16-bit PCM WAV, which is what EdgeTX expects.
