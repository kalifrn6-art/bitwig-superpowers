# Bitwig Superpowers

Native MIDI Tools and Audio Tools for Bitwig Studio.

This repository is the public download page. The implementation and development
history are private. Installers do not include Bitwig Studio, Bitwig vendor JARs,
license keys, or a Bitwig license. You must use your own valid Bitwig installation
and license.

**Superpowers is free and made by one person.** If it helps your music, please
[support the project](https://buy.stripe.com/9B64gA1b04jzaJbgyi1Jm00). It keeps new tools coming.

Website and feature tour: [kalifrn.com/superpowers](https://kalifrn.com/superpowers/)

## Downloads

Superpowers is now distributed **only as Patchbay mods**: no more installers, and
Bitwig Studio itself stays unmodified. Install Patchbay
0.36.0-dev.16, point it at your Bitwig installation and add the mods. Readable project
implementation source is not distributed. Compiled code can still be reverse-engineered.

Download only from the [Releases](https://github.com/kalifrn6-art/bitwig-superpowers/releases)
page. Do not use GitHub's automatically generated "Source code" archives; they
contain only this public download-page README.

### Superpowers for Patchbay 6.0.1-dev.1 (Bitwig 6.1.7 to 6.1.10)

| Platform | Bitwig | Bundle | Status |
|---|---|---|---|
| macOS (Apple Silicon) | **6.1.7** | [macOS ZIP](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-patchbay-6.0.1-dev.1/Superpowers-Patchbay-6.0.1-dev.1-macos.zip) | Tested by the author |
| macOS (Apple Silicon) | **6.1.8, 6.1.9, 6.1.10** | [macOS ZIP](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-patchbay-6.0.1-dev.1/Superpowers-Patchbay-6.0.1-dev.1-macos.zip) (map packs included) | Tested by the author on 6.1.10; offline checks on 6.1.9 and 6.1.10 |
| Windows x64 | **6.1.7, 6.1.9, 6.1.10** | [Windows ZIP](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-patchbay-6.0.1-dev.1/Superpowers-Patchbay-6.0.1-dev.1-windows.zip) (map packs included) | **Experimental:** offline checks only |
| Linux x64 | **6.1.7, 6.1.9, 6.1.10** | [Linux ZIP](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-patchbay-6.0.1-dev.1/Superpowers-Patchbay-6.0.1-dev.1-linux.zip) (map packs included) | **Experimental:** offline checks only |

Each platform ZIP includes everything in one download: the mods in `mods/` and the map packs in `maps/`
(macOS: 6.1.8, 6.1.9 and 6.1.10; Windows and Linux: 6.1.9 and 6.1.10).

**Install**

1. Download the ZIP for your OS and extract it. Leave the 25 ZIPs inside `mods/` compressed.
2. On Bitwig 6.1.8–6.1.10 (macOS) or 6.1.9 / 6.1.10 (Windows and Linux): in Patchbay, use **Import Map…**
   with the ZIP in `maps/` for your Bitwig version, leaving it compressed. Not needed on 6.1.7.
3. In Patchbay, choose your unmodified Bitwig installation in Settings, then use
   **Mods → Add Mod…** to add all 25 ZIPs for your OS. Do not mix platform sets.
4. Enable the mods you want and click **Load**.

Updating from 6.0.0-dev.2 or an earlier 6.0.1-dev.1 build: add the new ZIPs over the old ones; Patchbay replaces mods with the same id.

Included: 22 Superpowers mods, now with **Clean Waveforms**, and the 3 required frameworks (Actions and
Menus, Inspector, Preferences). Audio Tools still needs its external runtime.

**New in 6.0.1-dev.1**

- **Clean Waveforms is back, in our own version (5.3):** filled, rounded waveforms drawn from Bitwig's own
  peaks, with no lag and no trail under the cursor or playhead.
- **One download on every OS:** each platform ZIP carries its map packs in `maps/`.
- **Bitwig 6.1.8–6.1.10 on macOS, and 6.1.7, 6.1.9, 6.1.10 on Windows and Linux** through the included map packs.
- **Same placement as the Superpowers installer:** Freeze rows back at the top of the track menu,
  Assign Group Color right under the colours, and the read-only **Chord** row under Key in the Note Inspector.
- **Fixed:**
  - **Performance & UI responsiveness:** eliminates multi-second UI freezes when opening the default project, placing MIDI notes / opening the Note Inspector, and applying Glissando (lazy binary-indexed symbol tables + O(1) cached reflection, plus stripping unused tables for ~80–90 MB smaller downloads).
  - **Audio to MIDI timing:** bounced clips (which include Bitwig's silent bounce tail in the WAV file), trimmed/cropped clips, warped/stretched clips, looped clips and reversed clips now map extracted notes through Bitwig's native clip/event timing instead of compressing notes across the full WAV file duration.
  - **Freeze on Bitwig 6.1.10:** no longer freezes the UI or spikes GC after freezing a track.
  - **Capture MIDI with the loop on:** notes are placed from the playhead position at the click, folded into the loop, instead of keeping only the last 2 or 3 chords.
  - **Cmd+G on 6.1.10:** no longer crashes with Group Summary enabled.
  - **Bitwig 6.1.8 and later:** MIDI Tools, Freeze rows and the Capture toolbar button are shown again (including Windows and Linux 6.1.9–6.1.10).

Offline checks don't cover every project, plug-in or workflow. Save and back up your projects before trying a new version.

[Release notes](https://github.com/kalifrn6-art/bitwig-superpowers/releases/tag/superpowers-patchbay-6.0.1-dev.1) · [SHA-256 checksums](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-patchbay-6.0.1-dev.1/SHA256SUMS-6.0.1-dev.1.txt) · [Feature tour](https://kalifrn.com/superpowers/)

### Patchbay Launcher catalog

All 25 inner ZIPs per platform are also published as individual release assets. Add a
**Mods** source for repository `kalifrn6-art/bitwig-superpowers` and use the filter for your OS:

| Platform | Source filter |
|---|---|
| macOS | `*.macos.zip` |
| Windows (experimental) | `*.windows.zip` |
| Linux (experimental) | `*.linux.zip` |

Assets use `<mod-id>-6.0.1-dev.1.<platform>.zip`. The Preferences framework is
`preferences-composition-framework-1.0.0-platform.<platform>.zip`. Select all three frameworks
(**Actions and Menus**, **Inspector**, **Preferences**) explicitly, and use only one platform filter.

### Previous releases

**Beta 6.0.0 standalone installers (exactly Bitwig 6.1.7)** — the last installer-based release:
[macOS DMG](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-beta-6.0.0/Bitwig-Superpowers-macOS-AppleSilicon-Beta-6.0.0.dmg) ·
[Windows EXE](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-beta-6.0.0/Superpowers-Windows-x64-Beta-6.0.0.exe) ·
[Linux GZ](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-beta-6.0.0/Superpowers-Linux-x64-Beta-6.0.0.tar.gz) ·
[Release notes](RELEASE-6.0.0.md). For Bitwig 6.1.5 keep [Beta 5.0.2](https://github.com/kalifrn6-art/bitwig-superpowers/releases/tag/superpowers-beta-5.0.2);
for 6.1.3/6.1.4 keep [Beta 5](https://github.com/kalifrn6-art/bitwig-superpowers/releases/tag/superpowers-beta-5); for 6.1.1/6.1.2 keep Beta 4.3.

**Fixed in 5.0.2**

- **Projects that would not open** ("Unknown enum value with id 7 for enum quantize_grid_subdivision",
  [#19](https://github.com/kalifrn6-art/bitwig-superpowers/issues/19)): projects saved with a 5T / 7T
  grid failed to load. The cause was the Cmd+3 straight / triplet toggle, which is now **removed**;
  the grid works exactly like stock Bitwig again. Your projects were never damaged.
- **Shortcuts you can change:** Collapse / Expand Device and Collapse / Expand Track are now listed in
  Settings > Shortcuts. Remap or remove their keys there; the defaults (`-`, `+` / `=`, Left, Right)
  no longer override your choice.

**New in Beta 5** (also in 5.0.2)

- **Capture MIDI:** keeps the last 30 seconds you played; each capture uses up the buffer, so the next one never repeats notes.
- **Freeze:** one progress window for the whole queue, no repeated missing-plug-in prompts, clips keep their shape with hatched tails, Unfreeze waits until plug-ins reload, 24-bit renders.
- **Export with Group, Return and Master effects:** a new option in Export Audio.
- **Ramp:** Start / End velocity under the Velocity lane of the piano roll.
- **Piano roll:** selection follows moved notes, Cmd+E splits at the grid and keeps the pieces selected, Duplicate copies the full length. (Beta 5 also had Cmd+3 straight / triplet, removed in 5.0.2.)
- **Detect Event Key:** right-click an audio clip; its key is added to the clip name.
- **Device Keys:** `-` collapses the selected device, `+` / `=` expands it.
- **Groups:** lighter group summaries, a compact height toggle, Left / Right fold and unfold tracks, visible Shift ranges.
- **Linux** support (Bitwig 6.1.5).

**Something not working? Use Send Report.** Every installer has it (Linux:
`python3 superpowers_linux.py report`). It saves a zip with your logs on the
Desktop, with your user name and folders removed, and opens a prefilled GitHub
issue. Drag the zip in and submit. Nothing is sent automatically.

The installers check your exact Bitwig version and stop on an unknown or modified
Bitwig JAR instead of guessing. The Mac app is ad-hoc signed, not Developer ID
signed or notarized; the Windows EXE is not code-signed.

## Before installing

Save your projects and fully quit Bitwig Studio, its audio engine, and plug-in
hosts. Keep the installer for access to its restore tools. The installer verifies
the target and creates a verified backup
before replacing anything.

The optional Audio Tools setup downloads pinned Python packages and optional
models over outbound HTTPS. If the Microsoft Visual C++ x64 runtime is missing,
the Windows installer downloads Microsoft's signed installer and shows its normal
license UI. No inbound firewall rule is required.

## Safety and support

If these tools help your music, consider supporting the project. Your support
helps me maintain and improve Superpowers. Support is always optional.
[Support Superpowers through Stripe](https://buy.stripe.com/9B64gA1b04jzaJbgyi1Jm00)

Use beta software on backed-up projects. Nothing is uploaded automatically. To
report a problem, open a GitHub issue with your operating system, exact Bitwig
version, installer version, steps to reproduce, and sanitized logs. Never upload
your Bitwig JAR, license data, private projects, credentials, or personal paths.

Bitwig Studio is a product of Bitwig GmbH. This project is independent and is not
affiliated with or endorsed by Bitwig GmbH.
