# Winter Modular Eloquencer V1.3.1 Firmware Update

Includes updater files for Linux, macOS and Windows.

Firmware Version 1.3.1 comes pre-installed on the 5th batch eloquencer (June 2019). You only need to update if you have a Firmware version 1.3.0 or earlier. 

Download the updater here: [ELOQUENCER___UPDATER-master.zip](https://github.com/enoughframes/ELOQUENCER___UPDATER/archive/master.zip)

If you have a first batch eloquencer and you have never updated, please refer to updater manual (link below) to do the calibration procedures. If you have a 2nd or 3rd batch unit these procedures are already done.

Make sure to read [elo_1_3_0_update_procedure.pdf](https://github.com/enoughframes/ELOQUENCER___UPDATER/blob/master/elo_1.3.0_update_procedure.pdf) carefully before updating.

ELOQUENCER FW v 1.3.1 Release notes
- Eloquencer discards MIDI clocks while being stopped. (allows good sync when receiving clock from MIDI devices that are always sending MIDI clock) 

ELOQUENCER FW v 1.3.0 Release notes
### New EME (Eloquencer MIDI Expansion) functionalities
## Solved bugs:
- CV output voltage was changing before the gate raised.
- 'Quick pattern chain' mode: Short pressing inside the chain was breaking the chain in banks B, C and D.
- Incorrect LED behavior when changing bank while in pattern mode
- Duplicate pattern, copy/paste pattern and copy/paste track were not copying the division and repetition amount correctly.
- Encoder direction in track shift mode was incorrect.
- While in 'Step Mode > random' some of the gates were not correctly triggered.
- CV IN 1 and 2 couldn't be simultaneously assigned to CV add or CV Q
- CV IN 1 and 2 couldn't be simultaneously assigned to track shift
- In some cases the CV value was changed at the end of a tie.
- Ties were not being extended correctly in “song mode” or “quick pattern chain mode”
- CV variation probability wasn't working in 'Step mode > rep/x'
- Pattern chains weren’t starting at the first pattern when the ‘master track’ was set to anything different than 'int'
- Pressing stop outside the pattern mode while 'quick pattern chain' was active, caused the LED step buttons to show the pattern information.
- Ratcheting in the first step was getting stacked when the Eloquencer clock was set to external (Tempo:EXT) and the master clock was stopped
## New features:
- Track length behavior modified, when a track length is set, the transport jumps directly to the first step.
- Internal and external clock improved to achieve more stability.
- Shuffle can now be applied whit tempo set to external (Tempo:EXT)
- After power up, before touching any button the gates are now closed (low) (in previous version the gates were open (high) until a button was pressed)
- LIVE REC mode can now record longer notes (TIEs)
- Added ranges to the 'Random mode'
- Configurable LED matrix dimming
- Added confirmation message when loading or saving projects.
- Two more reset settings in configurations (PlayH/StopL and Play/stop trigger)
- Each individual pattern can now be set to start from the first step when triggered (independently from the 'Track reset config’)
- New setting to allow resetting the whole chain/part/song when an external clock reset is received (instead of just resetting the currently
playing pattern)
- New global setting to change the default set of gate lengths
- Pre-listen while stopped. The active steps can be heard by pressing the desired step button in CV step edition mode. (for example to be able to write chords through several channels).
- Added 7 new user scales.
- New “DJ nudge” functionality in Tempo mode. Use steps 13 to 16 to adjust the tempo sync to synchronize with non-clocked sources.

