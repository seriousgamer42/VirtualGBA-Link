# VirtualGBA-Link (PicoGBA-Link)

**An open-source USB-C to GameCube GBA Link Cable adapter**

Turn any modern device with a USB-C port (Android phone, Steam Deck, Android handheld, laptop, etc.) into a virtual Game Boy Advance that works with real GameCube and early Wii hardware via the official GBA–GameCube link cable protocol.

No more hunting for rare original GBAs, dead batteries, or worn-out link cables.

### Why this exists
Many classic GameCube (and early Wii) games have excellent features that only work with a connected GBA:
- **The Legend of Zelda: The Wind Waker** – Tingle Tuner (map, hints, and items on the second screen)
- **The Legend of Zelda: Four Swords Adventures** – Full 4-player multiplayer
- **Final Fantasy Crystal Chronicles** – Co-op multiplayer
- **Pokémon Colosseum / XD** – Bonus content and transfers
- **Sonic Adventure 2: Battle** – Chao Garden transfers
- Dozens of other titles with second-screen maps, inventory, trading, unlockables, and more.

This project brings those experiences back in 2026 using cheap, widely available parts and modern emulation.

### Features (planned / in progress)
- USB-C connection to host device (powers the phone/handheld while connected)
- RP2040-based dongle emulates the GBA side of the Joybus protocol
- Companion Android app runs **mGBA** to emulate the actual GBA game/ROM
- Real-time second screen experience (map on phone while main game runs on TV)
- Fully open source: hardware (KiCad), firmware, and software
- Low cost to build (~$10–25 in parts)
- 3D-printable case option

### How it works
1. Plug the dongle into a GameCube controller port (or early Wii GC port).
2. Connect the USB-C end to your phone or handheld.
3. Launch the companion app, load your legally dumped GBA ROM (or the companion mode for the GC game).
4. Start your GameCube game — it detects the "GBA" and enables all link features.
5. The phone displays the GBA content in real time.

### Repository Structure
- `/hardware/` — KiCad schematics, PCB, BOM, and 3D-printable case files
- `/firmware/` — RP2040 firmware (C/C++ with PIO for Joybus timing)
- `/android/` — Companion Android app (mGBA integration + USB communication)
- `/docs/` — Protocol notes, compatibility list, build guides
- `/tools/` — Desktop testing tools and utilities

### Getting Started (for developers)
This project is in early stages and **needs contributors** in the following areas:
- RP2040 firmware (Joybus protocol implementation using PIO)
- Android USB Host + mGBA integration
- Hardware design & testing
- Compatibility testing across supported GameCube titles

**Useful existing open-source resources:**
- [afska/gba-link-connection](https://github.com/afska/gba-link-connection) — Includes LinkCube Joybus implementation
- [JonnyHaystack/joybus-pio](https://github.com/JonnyHaystack/joybus-pio) — Excellent GameCube/N64 Joybus library for RP2040
- [Doridian/Joybus-PIO](https://github.com/Doridian/N64-Pico-PIO) — Another solid Joybus PIO reference
- mGBA emulator core

### Building your own
Detailed build guides will be added to `/docs/` as development progresses.

**Current status:** Concept → Planning → Early prototyping

### Contributing
We welcome pull requests, issues, and discussions!  
Whether you're experienced with RP2040 PIO, Android development, retro protocol reverse engineering, or just want to help test games — your contributions are valuable.

Please read [CONTRIBUTING.md](CONTRIBUTING.md) (coming soon) and join the discussion.

### License
- Hardware: [CERN-OHL-S 2.0](https://ohwr.org/project/cernohl) (or CC-BY-SA)
- Firmware & Software: MIT License (unless otherwise noted)

This is a community-driven project. Let's bring these forgotten GameCube + GBA features back to life without needing rare 20+ year old hardware!

### Related projects
- Dolphin Emulator (software-only GBA link support)
- agtbaskara's Game Boy Pico Link Board (similar USB link adapter concept)

---

**Made with ❤️ for the retro gaming community.**

Star the repo if you're interested — it helps attract more contributors!
