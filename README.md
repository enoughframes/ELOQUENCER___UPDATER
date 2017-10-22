# Winter Modular Eloquencer V1.0.4 Firmware Update

Includes updater files for Linux, macOS and Windows.

Firmware Version 1.0.4 comes pre-installed on the 2nd batch eloquencer (september 2017). You only need to update if you have a 1st batch eloquencer with version 1.0.1 or earlier.

Download the updater here: [ELOQUENCER___UPDATER-master.zip](https://github.com/enoughframes/ELOQUENCER___UPDATER/archive/master.zip)

Make sure to read [elo_1.04_update_procedure.pdf](https://github.com/enoughframes/ELOQUENCER___UPDATER/blob/master/elo_1.04_update_procedure.pdfom) carefully before updating.

## Release notes
### Solved Bugs:
#### Transport:
When in External Clock mode (Slave), the sequencer wasn't being sent to the first pattern
step when receiving a reset from another sequencer or clock.
#### Project:
The lights that indicate which slots are occupied were not working properly in all the cases
#### Step Mode:
In some cases the tracks were being referred as “track 1, track 2…” and not as “track A,
track B...” which was confusing. Now all track names use letters instead of numbers in all
areas of the interface.

When using “Div step mode” the divided track could lose sync after switching between stop
and play.

The division “/2” was missing in the clock out configuration.

###Delete track:
When deleting a track, the corresponding track button was not highlighted during some parts
of the process..
###Master Track:
Pattern length was incorrectly set to 0 after power on, when the master track was set to “int”
and pattern length was 64 steps in a saved project.
###Scale:
Diminished scale was not correct
###Options:
The cv gate link information text was not correct
In some cases the encoder direction was not correctly saved in the global configuration
###Track Shift:
Ties didn´t move when track shifting
###Freeze-Revert:
When doing a revert without a previous freeze the current pattern was deleted.
###Tie:
When the last step of a pattern with a tie was removed, the gate was not going low.
###Clock Out:
The Clock Out Pulse Width did not actually change the Clock Out Pulse Width.
###Global:
When moving from random mode to another function the light on the step edit buttons was
not turned off.

The function button sometimes got stuck in red or green color.

Going to specific modes with specific button sequences could block step buttons
When loading a project with the sequencer running some tracks didn't start from the first
step.

Some not available operations in some modes could take the interface to a dead end. For
example function+clock and then function+paste.
###Song Mode:
Some very specific combinations of part sequences and track lengths made the sequencer
not start from the beginning.

Loading a project while in song mode could lead the sequencer to get stuck in a pattern.
The 10th step button was not working in song mode.
###Live Rec:
While in free play mode the selected track should be temporarily muted to allow free playing
over the recorded notes, but the track was not being unmuted after leaving the mode.
###CV in:
In some cases the CV IN polarity was not saved with the project.
###Duplicate:
When duplicating, the “step_mode_div” was not properly copied.
##New Features:
###Step edit:
When using the track button to move all the CV values in CV Mode, the relation between
notes is maintained. In other words : you can transpose.

The relation between values is maintained too for the rest of the step edit modes (Gate, Gate
length, and Ratcheting).

You can now edit multiple steps in the Step Edit Modes (CV, Gate, Gate length, and
Ratcheting) by pressing a group of steps and moving the encoder (Multistep edition).

The coarse mode (pushing the encoder) in CV Step edition now jumps one octave at a time.

The font size of the current step note in CV step edition is now bigger to improve readability
###Live rec:
Live recording while song mode is on. You can now record longer than one bar melodies.
Just arrange a sequence of patterns in a part or in a song and “live record” through them
with the «GATE REC» and «CV KEY REC» functionalities.

You can now delete the step values in tracks when using «GATE REC», by holding the
corresponding track button.

###Shortcuts:
You can now access different shortcuts while pressing the FUNC button.
* FUNC + TRACK: fill in track
* FUNC + RATCHET + TRACK: Mute track
* FUNC + ROTATE ENCODER: Change “pattern to play” if song mode is not active, Change
“pattern to edit” if song mone is active."

###CV Inputs:
The CV inputs can now be tuned to work in V/oct. (No additional hardware needed).
However, these CV inputs were not originally intended for this purpose and some
unexpected behaviour can happen in some occasions like some notes jumping to the
contiguous semitone.

CV in track assign is now activated at the exact moment you press the track buttons. Before
this fix you needed to press the encoder before and after selection for them to be activated
which was not optimal and could be confusing at times.

###Scale:
Up to 8 Scale groups can be set up now in the Scale Menu. We can set up a root note and a
scale setting in each one of them. Each pattern can be linked to one of those groups in the
pattern section. This means we can use up to 8 different combinations of scales and root
notes in a one project or song.

New Scales: Wholetones, Pentatonic Major and Minor.
###Transport:
Change: When the sequencer is powered on, it doesn’t automatically start until you press
the play button.
###Aux Output:
Can be configured as “HIGH - PLAY , LOW - STOP” to control certain modules that expect
this behaviour.
###Tempo:
You can now enter the tempo information via “tap tempo”.
Tempo menu structure improved.
###Ratcheting:
Ratcheting divisions are now proportional to the track division step mode.
###Song mode:
Deleting parts is now possible in “create part” and “play part” modes.
###Random mode:
New improved menu structure.

We can now randomize note values within a range (by octaves or semitones).
###Project:
Current project step button is now highlighted in a different color.
###Global:
Internal / External mode it is now saved as a global variable, it’s not saved with the project
anymore. Now loading a new project will not change your external/internal clock setting.
