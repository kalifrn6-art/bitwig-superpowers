# Superpowers Beta 6.0.0 — Bitwig 6.1.7

New and updated native workflows, alongside the tools from Beta 5.0.2.

## New

- MIDI Comp: build a performance from sections of MIDI takes and keep editing the notes.
- Glissando in MIDI Tools, plus updated visual helpers for Stacks, Strum and Glissando.
- Browser Rank and sorting for finding frequently used items.
- Clean Waveforms with improved waveform detail when zooming.
- Settings → Mods to choose which Superpowers features to use.

## Updated

- Freeze keeps the MIDI-note representation, snowflake indicator and hatched tails. Queue handling stops transport before renders, allows plug-ins to settle and checks engine recovery after the queue.
- Capture MIDI supports adding captured notes to an existing clip while playing. Separate clips retain their existing behavior; merge them manually when needed.
- Updated for the separately built macOS, Windows and Linux versions of Bitwig 6.1.7.

Export with FX, Ramp, the existing MIDI and Audio Tools, Detect Event Key, piano-roll editing improvements, group tools and device shortcuts remain included. The retired Cmd+3 straight/triplet toggle remains removed.

## Compatibility and validation

**This release supports exactly Bitwig Studio 6.1.7.** macOS 13+ Apple Silicon, Windows 10/11 x64, or Linux x64. Installers require your own valid Bitwig installation and license; they do not include Bitwig Studio or vendor JARs.

macOS Freeze and Capture behavior has been confirmed by the user. All three installers passed payload checksum verification, exact reconstruction of their candidate, bytecode/reference checks and verification that the modified-JAR integrity check is disabled. Windows started in an isolated CrossOver test; this is not native Windows validation. **Windows and Linux interactive validation is pending.** Offline checks do not prove every project, plug-in or workflow. Optional Audio Tools require their runtime; Linux Audio Tools setup remains pending.

Save and back up projects, then fully quit Bitwig and its engine before installing. The installer verifies the exact input and preserves a backup. Use Restore Original to revert, or Send Report for a sanitized support bundle. macOS is ad-hoc signed, not notarized; the Windows EXE is not code-signed.

## Superpowers for Patchbay (beta 6.0.0-dev.2)

Platform bundles (`Superpowers-Patchbay-6.0.0-dev.2-{macos,windows,linux}.zip`) are included for unmodified **Bitwig Studio 6.1.7** with **Patchbay 0.36.0-dev.16**. Each outer ZIP contains 21 Superpowers mods and 3 required frameworks (22 selected functions; Clean Waveforms is excluded).

1. Extract the outer platform ZIP, leaving the 24 ZIPs inside `mods/` compressed.
2. In Patchbay, select your unmodified Bitwig 6.1.7 installation under Settings, then use **Mods → Add Mod…** to import all 24 ZIPs for your operating system. Do not mix platform ZIP sets.
3. Enable the desired mods and click Load.

The macOS source selection was tested by the author; symbol-map cleanup and the experimental Windows and Linux bundles passed offline preparation, reflection/direct-reference verification, and real Patchbay launcher import/update/digest-rejection checks. **Windows and Linux Patchbay bundles are experimental and have not been tested interactively on those operating systems.**

For Bitwig 6.1.5, keep Beta 5.0.2; for 6.1.3/6.1.4, keep Beta 5. These installers are not an automatic compatibility promise for later Bitwig versions.

[Feature tour and downloads](https://kalifrn.com/superpowers/) · [Support Superpowers](https://buy.stripe.com/9B64gA1b04jzaJbgyi1Jm00)

SHA-256 checksums are attached in SHA256SUMS-6.0.0.txt. Showcase videos are animated UI recreations, not screen recordings.
