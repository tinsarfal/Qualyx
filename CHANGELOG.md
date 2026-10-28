# Changelog

## 1.0.85

**Quest setup: enable Settings → Experimental → Positional time warp before playing with Headset timewarp.** Qualyx cannot enable or verify this system switch.

- Added an optional Steam downloader for Half-Life: Alyx, with Steam Guard, background progress, pause/resume, and recovery after restarting Qualyx. Use the Steam account that owns the game, choose an empty game folder, and allow about 70 GiB of free space.
- Fixed a controller-input timing race that could interrupt held movement. Improved delivery and recovery of short controller vibration effects.
- Fixed dominant-hand synchronization and control bindings so switching to left-handed play no longer repeatedly clears menu input. Confirmation on an affected headset is still pending.
- Added compatibility handling for the October 2026 Alyx game-file update, restoring supported menu layouts and styles when the exact affected resources are detected. Confirmation of the reported blank New Game dialog on an affected headset is still pending.
- Fixed a bHaptics SDK loading crash and improved handling of unavailable haptics services.
- Added experimental ProVolver / ForceTube recoil and reload feedback, with device selection and separate kick/rumble intensity controls. Off by default; can run alongside bHaptics.
- Updated the source GPU driver and its automatic selection on Quest 3 / 3S, with small-pass tuning, a lighting-flicker workaround, and corrected depth-writing passes when foveation is enabled. Reduced repeated warning-log writes.
- Added Rounded band and Rectangle foveation patterns, adjustable sharp-region size, and vertical positioning. The help explains the shared shading map and its extra sharp area in each eye.
- Added optional Dynamic 20–100% render resolution, which adjusts detail toward the selected frame-rate target. It reserves full-resolution memory.
- Made automatic RAM protection on Quest 3 / 3S less aggressive and added gradual recovery of texture detail when memory becomes available. Added Quest 2 map-loading memory cleanup.
- Moved Direct eye copy and Release texture scratch cache into Performance settings. Scratch-cache release now defaults on consistently in the controls, launch settings, and shared settings; saved choices are preserved. Other cache and memory experiments remain optional.
- Added brightness and contrast controls for the game image.
- Updated **Disable spotlight shadows** to retain nearby lights and the flashlight. Headset visual confirmation of this change is still pending.
- Made **Reflex sight enemy highlight** optional and off by default because it switches to a slower rendering path.
- Added an optional setting to hide Jeff's spores and particle effects. Coughing and damage still apply, so invisible clouds remain hazardous.
- Added an option to play Valve’s original startup intro. Added a Console page to the in-game Developer menu, with command entry and session history. Headset layout and command-entry checks are still pending.
- Improved texture-optimization validation and error reporting for damaged source archives.

Performance gains vary by scene and settings; no general percentage improvement over 1.0.84 is claimed. Automatic RAM protection does not guarantee prevention of memory crashes. Physical bHaptics/ProTube feedback, Quest 2/Pico gameplay, and long-session behavior still need acceptance testing. Authenticated downloading of the complete retail game remains untested.
