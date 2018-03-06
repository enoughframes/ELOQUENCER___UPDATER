# Winter Modular Eloquencer V1.2.0 Firmware Update

Includes updater files for Linux, macOS and Windows.

Firmware Version 1.2.0 comes pre-installed on the 3rd batch eloquencer (March 2018). You only need to update if you have a 1st or 2nd batch eloquencer with version 1.0.4 or earlier. (batch can be identify with the first digit of the serial number beside the power connector).


Download the updater here: [ELOQUENCER___UPDATER-master.zip](https://github.com/enoughframes/ELOQUENCER___UPDATER/archive/master.zip)

If you have a first batch eloquencer and you have never updated, please refer to updater manual (link below) to do the calibration procedures. If you have a 2nd or 3rd batch unit these procedures are already done.

Make sure to read [elo_1.04_update_procedure.pdf](https://github.com/enoughframes/ELOQUENCER___UPDATER/blob/master/elo_1.04_update_procedure.pdf) carefully before updating.

## Release notes:
### New Features:
#### Quick pattern chain (aka Devine mode):
A quick way to create pattern chains. Being in pattern mode, two patterns (steps) can be pressed to create a new chain starting at the first and ending at the second (after the current pattern finishes it will start to play the chain in loop). The chain will be activated when you release the two buttons.

The way it jumps between patterns can be changed by holding the two buttons (first and last pattern) and rotating the encoder, The modes are forward, backward, random, coin toss (previous or next) and drunken (previous, current or next).

If you press a pattern outside the chain you will break the chain and will start to play that new pattern (after the current pattern ends), if you press a pattern inside the chain you will change the pattern to edit, if you long press inside the chain you will break the chain and start to play that pattern (after the current pattern ends).

With the pattern chain created it’s easy to edit patterns, steps can be edited using the step edition modes and the chain section (or pattern) can be changed using FUNC + encoder.


#### Stepped LFO:
It’s important to note that this is not a linear continuous LFO, this Stepped LFO can change the CV out value every 1/32 pattern.

Any of the tracks can be configured to work in Stepped LFO mode. When you use the CV out as LFO the gate output is still sending the existing gates in the track so you can still use the gate output independently of the LFO

There are 5 different types of Stepped LFO: SAW, RAMP, TRIANGLE, SQUARE and RANDOM. The LFO period can be defined in patterns and steps. Some types have a minimal duration of 2 steps (SAW, RAMP, TRIANGLE), while SQUARE has a minimal duration of 1 step and RANDOM has a minimal duration of 1/2 step. The maximum duration for all types is 32 patterns.

The LFO amplitude can be adjusted from 0 to 9V, and we can also set an offset from -9V to 9V. That doesn’t mean that the CV output can go below 0 Volts. Any value below 0 will be limited at 0V, any value above 9V will be limited to 9V.

#### Display:
It now shows a status screen at power up. It can be removed by pressing any key.


#### Options:
Tune interface improved, new tuning adjustments added, menu structure changed.

It’s not possible to upload the user tune if it doesn’t exists.


#### Reset input:
The reset input now accepts a PLAY-STOP signal. A high signal at the reset input is understood as PLAY, a LOW signal at the reset input is understood as STOP. This can be configured in OPTIONS>RST IN.


#### Live Rec:
Step buttons (piano notes) can be used to play notes in CV KEY REC or FREE PLAY modes when the sequencer is stopped.

#### CV IN:
New CV in assignment to reset the LFOs.
The track assignment is now shown in the first menu level of CV IN

#### Step buttons:
The step buttons interface has been improved to be instantly refreshed every time there’s a change of pattern, or every time a function button is pressed.

#### Short keys:
The change pattern short key (FUNC + encoder) has been improved for faster pattern changing.
The pattern change will now happen just after releasing the function button, without the need to confirm the action by pressing down de encoder a second time.


### Bugs:
#### Live Rec:
Recorded gates not closing in CV KEY REC mode.
Track buttons were not lit after changing the track in FREE PLAY and CV KEY REC modes


#### Ratcheting:
Some ratcheting types were duplicated on the ratcheting list


#### Transport:
When in External Clock mode (Slave) without a cable plugged in, and the clock in multiplier activated, the sequencer incorrectly started playing every certain period of time.

When Track Reset Config was deactivated and step mode was DIV/x the first step of a sequence was played twice.


#### CV out:
At slow tempos a CV glitch happened sometimes at the end of the pattern.


#### Copy:
After copying a single track it was not possible to deactivate ratcheting.


#### Mute:
Mute did not work with TIE.

When in External Clock mode (Slave), and no clock signal coming in, it was not possible to change the mutes if the previous tempo was below 60 BPM.


