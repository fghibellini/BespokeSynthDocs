
## instruments
         
<a name=circlesequencer></a><br>

### <b>circlesequencer</b>

<img src="images/circlesequencer.png"><br>

<div style="display:inline-block;margin-left:50px;">
polyrhythmic sequencer that displays a loop as a circle<br><br>
<b>length*</b>: number of steps in this ring<br>
                   
<b>note*</b>: pitch to use for this ring<br>
                   
<b>offset*</b>: timing offset for this ring<br>
                   
<br><br><br><br></div>

<a name=drumsequencer></a><br>

### <b>drumsequencer</b>

<img src="images/drumsequencer.png"><br>

<div style="display:inline-block;margin-left:50px;">
step sequencer intended for drums. hold shift when dragging on the grid to adjust step velocity.<br><br>
<b><</b>: shift whole pattern one step earlier<br>
                   
<b>></b>: shift whole pattern one step later<br>
                   
<b>column</b>: current column, to use for visualizing the step on a midi controller<br>
                   
<b>grid</b>: patch a grid in here from a "midicontroller" module<br>
                   
<b>measures</b>: length of the sequence in measures<br>
                   
<b>metastep</b>: patch a grid in here from a "midicontroller" module to control the "meta step". I forget what this does. oops.<br>
                   
<b>offset*</b>: shift row forward/backward in time. try making your snares a little early, your hats a little late, etc.<br>
                   
<b>offsets</b>: show "offsets" sliders<br>
                   
<b>preset</b>: select a pattern preset<br>
                   
<b>r amt</b>: the chance that each step will change when being randomized. low values will only change a small amount of the sequence, high values will replace more of the sequence.<br>
                   
<b>r den</b>: density of the randomizer output. the higher this is, the busier the random output will be.<br>
                   
<b>randomize</b>: randomize the sequence<br>
                   
<b>repeat</b>: repeat input notes at this rate<br>
                   
<b>rowpitch*</b>: output pitch for this row<br>
                   
<b>step</b>: length of each step<br>
                   
<b>str</b>: velocity to use when setting a step via a grid controller, if the checkbox next to this slider is checked<br>
                   
<b>use str</b>: if the "str" slider should be used for setting velocity<br>
                   
<b>velocity</b>: patch a grid in here from a "midicontroller" module to control the velocity<br>
                   
<b>yoff</b>: vertical offset for grid controller's view of the pattern<br>
                   <br>accepts: <font color=yellow>pulses</font> <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=fouronthefloor></a><br>

### <b>fouronthefloor</b>

<img src="images/fouronthefloor.png"><br>

<div style="display:inline-block;margin-left:50px;">
sends note 0 every beat, to trigger a kick drum<br><br>
<b>two</b>: sends note only every two beats<br>
                   
<br><br><br><br></div>

<a name=gridkeyboard></a><br>

### <b>gridkeyboard</b>

<img src="images/gridkeyboard.png"><br>

<div style="display:inline-block;margin-left:50px;">
grid-based keyboard, intended primarily for 64-pad grid controllers<br><br>
<b>arrangement</b>: what style of layout should we use?<br>
                   
<b>ch.latch</b>: latch chord button presses<br>
                   
<b>grid</b>: patch a grid in here from a "midicontroller" module<br>
                   
<b>latch</b>: latch key presses, so you press once to play a note, and press again to release a note<br>
                   
<b>layout</b>: keyboard style<br>
                   
<b>octave</b>: base octave<br>
                   
<b>p.root</b>: for chorder, make root note always play<br>
                   
<br><br><br><br></div>

<a name=keyboarddisplay></a><br>

### <b>keyboarddisplay</b>

<img src="images/keyboarddisplay.png"><br>

<div style="display:inline-block;margin-left:50px;">
displays input notes on a keyboard, and allows you to click the keyboard to create notes<br><br><br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=m185sequencer></a><br>

### <b>m185sequencer</b>

<img src="images/m185sequencer.png"><br>

<div style="display:inline-block;margin-left:50px;">
sequencer using the unique paradigm of the the m185 or intellijel metropolis<br><br>
<b>gate*</b>: behavior for each row: "repeat" plays every step, "once" plays just the first step, "hold" holds across all steps, "rest" plays no steps<br>
                   
<b>interval</b>: interval per step<br>
                   
<b>pitch*</b>: pitch to use for this row<br>
                   
<b>pulses*</b>: number of steps this row should last<br>
                   
<b>reset step</b>: resets counter to first step<br>
                   <br>accepts: <font color=yellow>pulses</font> <br>
<br><br><br><br></div>

<a name=midicontroller></a><br>

### <b>midicontroller</b>

<img src="images/midicontroller.png"><br>

<div style="display:inline-block;margin-left:50px;">
get midi input from external devices. to get a nice display in the "layout" view, create a .json file with the same name as your controller to describe your controller's layout, and place it in your "data/controllers" directory. look at the other files in that directory for examples.<br><br>
<b> x </b>: delete this connection<br>
                   
<b>add</b>: add a mapping manually<br>
                   
<b>bind (hold shift)</b>: when this is enabled, you can map a midi input to a UI control by hovering over a UI control, holding shift, and then using desired midi input<br>
                   
<b>blink</b>: when the targeted control is enabled, send alternating on/off messages, to blink the associated LED<br>
                   
<b>channel</b>: which channel to pay attention to<br>
                   
<b>control</b>: pitch or control to refer to<br>
                   
<b>controller</b>: midi device to use<br>
                   
<b>controltype</b>: how this control should modify the target.
 -slider: set the value interpolated between "midi off" and "midi on" to the slider's value
 -set: set the specified value directly when this button is pressed
 -release: set the specified value directly when this button is released
 -toggle: toggle the control's value to on/off when this button is pressed
 -direct: set the control to the literal midi input value<br>
                   
<b>copy</b>: duplicate this connection<br>
                   
<b>feedback</b>: which cc or note should we send the feedback to?<br>
                   
<b>increment</b>: when "controltype" is "set" or "release", the targeted control is incremented by this amount (and the "value" field is ignored). when "controltype" is "slider", the targeted control is changed by this amount in the direction the control was changed (this setting is useful for "infinite encoders")<br>
                   
<b>layout</b>: which layout file should we use for this controller? these can be created in your Documents/BespokeSynth/controllers folder.<br>
                   
<b>mappingdisplay</b>: which mapping view to see<br>
                   
<b>messagetype</b>: type of midi message<br>
                   
<b>midi off</b>: the lower end of the midi range. send this value when the targeted control is off. if "scale" is enabled, this also controls the lower end of the slider range, and you can set midi off to be higher than midi on to reverse a slider's direction.<br>
                   
<b>midi on</b>: the upper end of the midi range. send this value when the targeted control is on. if "scale" is enabled, this also controls the upper end of the slider range, and you can set midi off to be higher than midi on to reverse a slider's direction.<br>
                   
<b>monome</b>: which monome should we use?<br>
                   
<b>osc input port</b>: port to use for osccontroller input<br>
                   
<b>page</b>: select which page of midi controls to use. each page acts like an independent midi controller, so you can use pages to allow one midi controller to switch between controlling many things<br>
                   
<b>pageless</b>: should this connection work across all pages of the midicontroller?<br>
                   
<b>path</b>: path to the control that should be affected<br>
                   
<b>scale</b>: should the output of this midi slider be scaled between "midi off" and "midi on"?<br>
                   
<b>twoway</b>: should we send feedback to the controller? (to control the LEDs associated with the button/knob)<br>
                   
<b>value</b>: the value to set<br>
                   
<br><br><br><br></div>

<a name=notecanvas></a><br>

### <b>notecanvas</b>

<img src="images/notecanvas.png"><br>

<div style="display:inline-block;margin-left:50px;">
looping note roll<br><br>
<b>canvas</b>: canvas of notes. canvas controls:
-shift-click to add a note
-hold shift and drag a note to duplicate
-hold alt to drag a note without snapping
-hold ctrl while dragging to snap to an interval
-hold shift and scroll to zoom
-hold alt and grab empty space to move slide the canvas view
-hold ctrl and grab empty space to zoom the canvas view<br>
                   
<b>clear</b>: delete all elements<br>
                   
<b>delete</b>: delete highlighted elements<br>
                   
<b>drag mode</b>: direction that elements can be dragged<br>
                   
<b>free rec</b>: enable record mode, and extend canvas if we reach the end<br>
                   
<b>interval</b>: interval to quantize to<br>
                   
<b>measures</b>: loop length<br>
                   
<b>play</b>: play notes on canvas<br>
                   
<b>quantize</b>: quantize selected notes to interval<br>
                   
<b>rec</b>: record input notes to canvas<br>
                   
<b>scrollh</b>: horizontal scrollbar<br>
                   
<b>scrollv</b>: vertical scrollbar<br>
                   
<b>show chord intervals</b>: show brackets to indicate chord relationships<br>
                   
<b>timeline</b>: control loop points<br>
                   
<b>view rows</b>: number of visible rows<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notechain></a><br>

### <b>notechain</b>

<img src="images/notechain.png"><br>

<div style="display:inline-block;margin-left:50px;">
trigger a note, followed by a pulse to trigger another note after a delay<br><br>
<b>duration</b>: duration of note, in measures<br>
                   
<b>next</b>: interval until sending pulse<br>
                   
<b>pitch</b>: pitch to play<br>
                   
<b>trigger</b>: play note for this chain node<br>
                   
<b>velocity</b>: velocity for note<br>
                   <br>accepts: <font color=yellow>pulses</font> <br>
<br><br><br><br></div>

<a name=notecounter></a><br>

### <b>notecounter</b>

<img src="images/notecounter.png"><br>

<div style="display:inline-block;margin-left:50px;">
advance through pitches sequentially. useful for driving the "notesequencer" or "drumsequencer" modules.<br><br>
<b>div</b>: measure division, when using "div" as the interval<br>
                   
<b>interval</b>: rate to advance<br>
                   
<b>length</b>: length of the sequence<br>
                   
<b>random</b>: output random pitches within the range, rather than sequential<br>
                   
<b>start</b>: pitch at the start of the sequence<br>
                   
<b>sync</b>: if the output pitch should be synchronized to the global transport<br>
                   
<br><br><br><br></div>

<a name=notecreator></a><br>

### <b>notecreator</b>

<img src="images/notecreator.png"><br>

<div style="display:inline-block;margin-left:50px;">
create a one-off note<br><br>
<b>duration</b>: note length when "trigger" button is used<br>
                   
<b>on</b>: turn on to start note, turn off to end note<br>
                   
<b>pitch</b>: output note pitch<br>
                   
<b>trigger</b>: press to trigger note for specified duration<br>
                   
<b>velocity</b>: note velocity<br>
                   <br>accepts: <font color=yellow>pulses</font> <br>
<br><br><br><br></div>

<a name=notelooper></a><br>

### <b>notelooper</b>

<img src="images/notelooper.png"><br>

<div style="display:inline-block;margin-left:50px;">
note loop recorder with overdubbing and replacement functionality<br><br>
<b>canvas</b>: canvas of recorded notes<br>
                   
<b>clear</b>: clear pattern<br>
                   
<b>del/mute</b>: if "write" is enabled, erase notes as the playhead passes over them. otherwise, just mute them.<br>
                   
<b>load*</b>: restore pattern<br>
                   
<b>num bars</b>: set loop length in measures<br>
                   
<b>store*</b>: save pattern<br>
                   
<b>write</b>: should input should be recorded?<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notesequencer></a><br>

### <b>notesequencer</b>

<img src="images/notesequencer.png"><br>

<div style="display:inline-block;margin-left:50px;">
looping sequence of notes at an interval. pair with a "pulser" module for more interesting step control. hold "shift" to adjust step length.<br><br>
<b><</b>: shift the sequence to the left<br>
                   
<b>></b>: shift the sequence to the right<br>
                   
<b>clear</b>: clear all steps<br>
                   
<b>grid</b>: patch a grid in here from a "midicontroller" module<br>
                   
<b>interval</b>: note length<br>
                   
<b>len</b>: randomize the length of each step's note.<br>
                   
<b>len*</b>: length for this column<br>
                   
<b>length</b>: length that the sequence below should play. the overall grid length can be changed by adjusting "gridsteps" in the triangle menu.<br>
                   
<b>loop reset</b>: when sequence loops, reset to here instead. send a "downbeat"-style message from a pulser to restart the sequence from the first step.<br>
                   
<b>notemode</b>: which set of pitches should the rows represent?<br>
                   
<b>octave</b>: octave of the bottom pitch of this sequence<br>
                   
<b>pitch</b>: randomize pitches in the sequence. hold shift to constrain the randomization to only pick roots and fifths.<br>
                   
<b>rand len chance</b>: when clicking the random length button, what is the chance that a step gets changed?<br>
                   
<b>rand len range</b>: when clicking the random length button, how much will the length change?<br>
                   
<b>rand pitch chance</b>: when clicking the random pitch button, what is the chance that a step gets changed?<br>
                   
<b>rand pitch range</b>: when clicking the random pitch button, how far will the pitch change?<br>
                   
<b>rand vel chance</b>: when clicking the random velocity button, what is the chance that a step gets changed?<br>
                   
<b>rand vel density</b>: when clicking the random velocity button, what are the chances that a step should have a note?<br>
                   
<b>tone*</b>: pitch for this column<br>
                   
<b>vel</b>: randomize the velocity of each step's note.<br>
                   
<b>vel*</b>: velocity for this column<br>
                   
<b>x offset</b>: x offset of attached grid controller<br>
                   
<b>y offset</b>: y offset of attached grid controller<br>
                   <br>accepts: <font color=yellow>pulses</font> <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notesinger></a><br>

### <b>notesinger</b>

<img src="images/notesinger.png"><br>

<div style="display:inline-block;margin-left:50px;">
output a note based on a detected pitch<br><br>
<b>oct</b>: octave to adjust output pitch by<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=playsequencer></a><br>

### <b>playsequencer</b>

<img src="images/playsequencer.png"><br>

<div style="display:inline-block;margin-left:50px;">
drum sequencer that allows you to punch in to record and overdub steps, inspired by the pulsar-23 drum machine<br><br>
<b>grid</b>: patch a grid in here from a "midicontroller" module<br>
                   
<b>interval</b>: the step size<br>
                   
<b>link columns</b>: if the mute/delete control should be shared across the entire column<br>
                   
<b>load*</b>: load the sequence stored in this slot<br>
                   
<b>measures</b>: the loop length<br>
                   
<b>mute/delete*</b>: if write is disabled, mute this row. if write is enabled, clear the steps as the playhead passes them<br>
                   
<b>note repeat</b>: if held notes should repeat every step<br>
                   
<b>store*</b>: store the current sequence to this slot<br>
                   
<b>write</b>: if the current input should be written to the sequence. this will also delete steps if mute/delete is enabled for this row<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=polyrhythms></a><br>

### <b>polyrhythms</b>

<img src="images/polyrhythms.png"><br>

<div style="display:inline-block;margin-left:50px;">
looping sequence with lines on different divisions<br><br>
<b>length*</b>: number of steps for this line<br>
                   
<b>note*</b>: pitch to use for this line<br>
                   
<br><br><br><br></div>

<a name=randomnote></a><br>

### <b>randomnote</b>

<img src="images/randomnote.png"><br>

<div style="display:inline-block;margin-left:50px;">
play a note at a given interval with a random chance<br><br>
<b>interval</b>: the note length<br>
                   
<b>offset</b>: the amount of time to offset playback within the interval<br>
                   
<b>pitch</b>: the pitch to use<br>
                   
<b>probability</b>: the chance that a note will play each interval<br>
                   
<b>skip</b>: after a note plays, don't play a note the next n-1 times that it would have played<br>
                   
<b>velocity</b>: the velocity to use<br>
                   
<br><br><br><br></div>

<a name=slidersequencer></a><br>

### <b>slidersequencer</b>

<img src="images/slidersequencer.png"><br>

<div style="display:inline-block;margin-left:50px;">
trigger notes along a continuous timeline<br><br>
<b>division</b>: rate to progress<br>
                   
<b>note*</b>: pitch for this element<br>
                   
<b>playing*</b>: is this element playing?<br>
                   
<b>time*</b>: time to trigger this element<br>
                   
<b>vel*</b>: velocity of this element<br>
                   
<br><br><br><br></div>

## note effects
         
<a name=arpeggiator></a><br>

### <b>arpeggiator</b>

<img src="images/arpeggiator.png"><br>

<div style="display:inline-block;margin-left:50px;">
arpeggiates held notes. there are several vestigial features in this module that should be cleaned up.<br><br>
<b>interval</b>: arpeggiation rate<br>
                   
<b>octaves</b>: how many octaves to step through<br>
                   
<b>step</b>: direction and distance to step through arpeggiation. a value of zero is "pingpong".<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=capo></a><br>

### <b>capo</b>

<img src="images/capo.png"><br>

<div style="display:inline-block;margin-left:50px;">
shifts incoming notes by semitones<br><br>
<b>capo</b>: number of semitones to shift<br>
                   
<b>retrigger</b>: immediately replay current notes when changing the capo amount<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=chorddisplayer></a><br>

### <b>chorddisplayer</b>

<img src="images/chorddisplayer.png"><br>

<div style="display:inline-block;margin-left:50px;">
display which chord is playing, in the context of the current scale<br><br><br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=chorder></a><br>

### <b>chorder</b>

<img src="images/chorder.png"><br>

<div style="display:inline-block;margin-left:50px;">
takes an incoming pitch and plays additional notes to form chords<br><br>
<b>chord</b>: chord presets<br>
                   
<b>diatonic</b>: should the grid be chromatic, or locked to the scale only?<br>
                   
<b>inversion</b>: inversion presets<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=chordholder></a><br>

### <b>chordholder</b>

<img src="images/chordholder.png"><br>

<div style="display:inline-block;margin-left:50px;">
keeps any notes pressed at the same time sustaining, until new notes are pressed<br><br>
<b>pulse to play</b>: when enabled, input notes aren't played immediately, but instead wait for an input pulse before playing<br>
                   
<b>stop</b>: stop notes from playing<br>
                   <br>accepts: <font color=yellow>pulses</font> <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=gridnotedisplayer></a><br>

### <b>gridnotedisplayer</b>

<img src="images/gridnotedisplayer.png"><br>

<div style="display:inline-block;margin-left:50px;">
use with a gridkeyboard to display currently playing notes, to visualize chords, arpeggiation, etc.<br><br><br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=midicc></a><br>

### <b>midicc</b>

<img src="images/midicc.png"><br>

<div style="display:inline-block;margin-left:50px;">
outputs midi control change messages to route to a "midioutput" module<br><br>
<b>control</b>: CC control number<br>
                   
<b>value</b>: outputs a CC value when this changes<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=midioutput></a><br>

### <b>midioutput</b>

<img src="images/midioutput.png"><br>

<div style="display:inline-block;margin-left:50px;">
send midi to an external destination, such as hardware or other software<br><br>
<b>controller</b>: where to send midi to<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=modulationvizualizer></a><br>

### <b>modulationvizualizer</b>

<img src="images/modulationvizualizer.png"><br>

<div style="display:inline-block;margin-left:50px;">
display MPE modulation values for notes<br><br><br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=modwheel></a><br>

### <b>modwheel</b>

<img src="images/modwheel.png"><br>

<div style="display:inline-block;margin-left:50px;">
adds an expression value to a note<br><br>
<b>modwheel</b>: expression level<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=modwheeltopressure></a><br>

### <b>modwheeltopressure</b>

<img src="images/modwheeltopressure.png"><br>

<div style="display:inline-block;margin-left:50px;">
swaps expression input to midi pressure in the output<br><br><br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=modwheeltovibrato></a><br>

### <b>modwheeltovibrato</b>

<img src="images/modwheeltovibrato.png"><br>

<div style="display:inline-block;margin-left:50px;">
convert note mod wheel input rhythmic pitch bend<br><br>
<b>vibinterval</b>: rate of vibrato<br>
                   
<b>vibrato</b>: amount of pitch bend<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=mpetweaker></a><br>

### <b>mpetweaker</b>

<img src="images/mpetweaker.png"><br>

<div style="display:inline-block;margin-left:50px;">
adjust incoming MPE modulation values<br><br>
<b>modwheel mult</b>: amount to multiply incoming modwheel<br>
                   
<b>modwheel offset</b>: amount to offset incoming modwheel<br>
                   
<b>pitchbend mult</b>: amount to multiply incoming pitchbend<br>
                   
<b>pitchbend offset</b>: amount to offset incoming pitchbend<br>
                   
<b>pressure mult</b>: amount to multiply incoming pressure<br>
                   
<b>pressure offset</b>: amount to offset incoming pressure<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notechance></a><br>

### <b>notechance</b>

<img src="images/notechance.png"><br>

<div style="display:inline-block;margin-left:50px;">
randomly allow notes through<br><br>
<b>chance</b>: probability that a note is allowed<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notedelayer></a><br>

### <b>notedelayer</b>

<img src="images/notedelayer.png"><br>

<div style="display:inline-block;margin-left:50px;">
delay input notes by a specified amount<br><br>
<b>delay</b>: amount of time to delay, in measures<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notedisplayer></a><br>

### <b>notedisplayer</b>

<img src="images/notedisplayer.png"><br>

<div style="display:inline-block;margin-left:50px;">
show input note info<br><br><br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=noteduration></a><br>

### <b>noteduration</b>

<img src="images/noteduration.png"><br>

<div style="display:inline-block;margin-left:50px;">
sets the length a note will play, ignoring the note-off message<br><br>
<b>duration</b>: length of the note in measures<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notefilter></a><br>

### <b>notefilter</b>

<img src="images/notefilter.png"><br>

<div style="display:inline-block;margin-left:50px;">
only allow a certain pitches through<br><br><br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=noteflusher></a><br>

### <b>noteflusher</b>

<img src="images/noteflusher.png"><br>

<div style="display:inline-block;margin-left:50px;">
send a note-off for all notes<br><br>
<b>flush</b>: click to flush notes<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notegate></a><br>

### <b>notegate</b>

<img src="images/notegate.png"><br>

<div style="display:inline-block;margin-left:50px;">
allow or disallow notes to pass through<br><br>
<b>open</b>: if notes are allowed to pass<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notehocket></a><br>

### <b>notehocket</b>

<img src="images/notehocket.png"><br>

<div style="display:inline-block;margin-left:50px;">
sends notes to random destinations<br><br>
<b>weight *</b>: chance that note goes to this destination<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notehumanizer></a><br>

### <b>notehumanizer</b>

<img src="images/notehumanizer.png"><br>

<div style="display:inline-block;margin-left:50px;">
add randomness to timing and velocity<br><br>
<b>time</b>: amount of timing randomness, in milliseconds.<br>
                   
<b>velocity</b>: amount of velocity randomness<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notelatch></a><br>

### <b>notelatch</b>

<img src="images/notelatch.png"><br>

<div style="display:inline-block;margin-left:50px;">
use note on messages to toggle notes on and off<br><br><br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=noteoctaver></a><br>

### <b>noteoctaver</b>

<img src="images/noteoctaver.png"><br>

<div style="display:inline-block;margin-left:50px;">
transpose a note by octaves<br><br>
<b>octave</b>: number of octaves to raise or lower<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notepanalternator></a><br>

### <b>notepanalternator</b>

<img src="images/notepanalternator.png"><br>

<div style="display:inline-block;margin-left:50px;">
sets a note's pan, alternating between two values, for the internal synths that support panned notes<br><br>
<b>one</b>: pan position, .5 is centered<br>
                   
<b>two</b>: pan position, .5 is centered<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notepanner></a><br>

### <b>notepanner</b>

<img src="images/notepanner.png"><br>

<div style="display:inline-block;margin-left:50px;">
sets a note's pan, for the internal synths that support panned notes<br><br>
<b>pan</b>: pan position, .5 is centered<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notepanrandom></a><br>

### <b>notepanrandom</b>

<img src="images/notepanrandom.png"><br>

<div style="display:inline-block;margin-left:50px;">
sets a note's pan to random values, for the internal synths that support panned notes<br><br>
<b>center</b>: center pan position<br>
                   
<b>spread</b>: amount of randomness<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=noterangefilter></a><br>

### <b>noterangefilter</b>

<img src="images/noterangefilter.png"><br>

<div style="display:inline-block;margin-left:50px;">
only allows notes through within a certain pitch range<br><br>
<b>max</b>: maximum pitch allowed<br>
                   
<b>min</b>: minimum pitch allowed<br>
                   
<b>wrap</b>: instead of rejecting notes outside of this range, should we wrap them to the range instead?<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=noteratchet></a><br>

### <b>noteratchet</b>

<img src="images/noteratchet.png"><br>

<div style="display:inline-block;margin-left:50px;">
rapidly repeat an input note over a duration<br><br>
<b>duration</b>: total length of time repeats should last<br>
                   
<b>subdivision</b>: length of each repeat<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=noterouter></a><br>

### <b>noterouter</b>

<img src="images/noterouter.png"><br>

<div style="display:inline-block;margin-left:50px;">
allows you to control where notes are routed to using a UI control. to add destinations to the list, patch them as a target<br><br>
<b>route</b>: the noterouter's destination module<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notesorter></a><br>

### <b>notesorter</b>

<img src="images/notesorter.png"><br>

<div style="display:inline-block;margin-left:50px;">
separate notes by pitch. any unmapped pitches go through the standard outlet.<br><br>
<b>pitch *</b>: pitch to use for this outlet<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notestepper></a><br>

### <b>notestepper</b>

<img src="images/notestepper.png"><br>

<div style="display:inline-block;margin-left:50px;">
output notes through a round robin of patch cables, to create sequential variety<br><br>
<b>length</b>: length of the sequence<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notestream></a><br>

### <b>notestream</b>

<img src="images/notestream.png"><br>

<div style="display:inline-block;margin-left:50px;">
view a stream of notes as they're played<br><br>
<b>reset</b>: reset the pitch range<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notestrummer></a><br>

### <b>notestrummer</b>

<img src="images/notestrummer.png"><br>

<div style="display:inline-block;margin-left:50px;">
send a chord into this, and move a slider to strum each note of the chord<br><br>
<b>strum</b>: move the slider past each note to strum it<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notewrap></a><br>

### <b>notewrap</b>

<img src="images/notewrap.png"><br>

<div style="display:inline-block;margin-left:50px;">
wrap an input pitch to stay within a desired range<br><br>
<b>min</b>: bottom of pitch range<br>
                   
<b>range</b>: number of semitones before wrapping back down to min pitch<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=pitchbender></a><br>

### <b>pitchbender</b>

<img src="images/pitchbender.png"><br>

<div style="display:inline-block;margin-left:50px;">
add pitch bend to notes<br><br>
<b>bend</b>: bend amount, in semitones<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=pitchdive></a><br>

### <b>pitchdive</b>

<img src="images/pitchdive.png"><br>

<div style="display:inline-block;margin-left:50px;">
use pitchbend to settle into an input pitch from a starting offset<br><br>
<b>start</b>: semitone offset to start from<br>
                   
<b>time</b>: time in milliseconds to ramp from pitch offset into input pitch<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=pitchpanner></a><br>

### <b>pitchpanner</b>

<img src="images/pitchpanner.png"><br>

<div style="display:inline-block;margin-left:50px;">
add pan modulation to notes based upon input pitch, so low pitches are panned in one direction and high pitches are panned in another<br><br>
<b>left</b>: pitch that represents full left pan<br>
                   
<b>right</b>: pitch that represents full right pan<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=pitchremap></a><br>

### <b>pitchremap</b>

<img src="images/pitchremap.png"><br>

<div style="display:inline-block;margin-left:50px;">
remap input pitches to different output pitches<br><br>
<b>from*</b>: pitch to change<br>
                   
<b>to*</b>: desired pitch<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=pitchsetter></a><br>

### <b>pitchsetter</b>

<img src="images/pitchsetter.png"><br>

<div style="display:inline-block;margin-left:50px;">
set an incoming note to use a specified pitch<br><br>
<b>pitch</b>: the pitch to use<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=portamento></a><br>

### <b>portamento</b>

<img src="images/portamento.png"><br>

<div style="display:inline-block;margin-left:50px;">
only allows one note to play at a time, and uses pitch bend to glide between notes<br><br>
<b>glide</b>: time to glide, in milliseconds<br>
                   
<b>require held</b>: if enabled, only glide to a new note if an old note is held. otherwise, always glide, based upon the prior input note.<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=pressure></a><br>

### <b>pressure</b>

<img src="images/pressure.png"><br>

<div style="display:inline-block;margin-left:50px;">
add pressure modulation to notes<br><br>
<b>pressure</b>: pressure amount<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=pressuretomodwheel></a><br>

### <b>pressuretomodwheel</b>

<img src="images/pressuretomodwheel.png"><br>

<div style="display:inline-block;margin-left:50px;">
takes midi pressure modulation input and changes it to modwheel modulation<br><br><br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=pressuretovibrato></a><br>

### <b>pressuretovibrato</b>

<img src="images/pressuretovibrato.png"><br>

<div style="display:inline-block;margin-left:50px;">
takes midi pressure modulation input and changes it to vibrato, using pitch bend<br><br>
<b>vibinterval</b>: vibrato speed<br>
                   
<b>vibrato</b>: amount of vibrato<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=previousnote></a><br>

### <b>previousnote</b>

<img src="images/previousnote.png"><br>

<div style="display:inline-block;margin-left:50px;">
when receiving a note on, output the prior note on that we received<br><br><br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=quantizer></a><br>

### <b>quantizer</b>

<img src="images/quantizer.png"><br>

<div style="display:inline-block;margin-left:50px;">
delay inputs until the next quantization interval<br><br>
<b>quantize</b>: the quantization interval<br>
                   
<b>repeat</b>: when holding a note, should we repeat it every interval?<br>
                   <br>accepts: <font color=yellow>pulses</font> <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=scaledegree></a><br>

### <b>scaledegree</b>

<img src="images/scaledegree.png"><br>

<div style="display:inline-block;margin-left:50px;">
transpose input based on current scale<br><br>
<b>degree</b>: amount to transpose<br>
                   
<b>retrigger</b>: immediately replay current notes when changing the transpose amount<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=scaledetect></a><br>

### <b>scaledetect</b>

<img src="images/scaledetect.png"><br>

<div style="display:inline-block;margin-left:50px;">
detect which scales fit a collection of entered notes. the last played pitch is used as the root.<br><br>
<b>matches</b>: matching scales for this root<br>
                   
<b>reset</b>: reset the input collection of notes<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=sustainpedal></a><br>

### <b>sustainpedal</b>

<img src="images/sustainpedal.png"><br>

<div style="display:inline-block;margin-left:50px;">
keeps input notes sustaining<br><br>
<b>sustain</b>: should we hold the input notes?<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=transposefrom></a><br>

### <b>transposefrom</b>

<img src="images/transposefrom.png"><br>

<div style="display:inline-block;margin-left:50px;">
transpose input from a specified root to the root of the current scale. the primary usage of this would be to allow you to play a keyboard in C, but it gets transposed to the current scale.<br><br>
<b>retrigger</b>: immediately replay current notes when changing the transpose root or the scale<br>
                   
<b>root</b>: root to transpose from<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=unstablemodwheel></a><br>

### <b>unstablemodwheel</b>

<img src="images/unstablemodwheel.png"><br>

<div style="display:inline-block;margin-left:50px;">
mutate MPE slide with perlin noise<br><br>
<b>amount</b>: amount of mutation<br>
                   
<b>noise</b>: fast-later mutation rate<br>
                   
<b>warble</b>: slow-layer mutation rate<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=unstablepitch></a><br>

### <b>unstablepitch</b>

<img src="images/unstablepitch.png"><br>

<div style="display:inline-block;margin-left:50px;">
mutate MPE pitchbend with perlin noise<br><br>
<b>amount</b>: amount of mutation<br>
                   
<b>noise</b>: fast-later mutation rate<br>
                   
<b>warble</b>: slow-layer mutation rate<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=unstablepressure></a><br>

### <b>unstablepressure</b>

<img src="images/unstablepressure.png"><br>

<div style="display:inline-block;margin-left:50px;">
mutate MPE pressure with perlin noise<br><br>
<b>amount</b>: amount of mutation<br>
                   
<b>noise</b>: fast-later mutation rate<br>
                   
<b>warble</b>: slow-layer mutation rate<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=velocityscaler></a><br>

### <b>velocityscaler</b>

<img src="images/velocityscaler.png"><br>

<div style="display:inline-block;margin-left:50px;">
scale a note's velocity to be higher or lower<br><br>
<b>scale</b>: amount to multiply velocity by<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=velocitysetter></a><br>

### <b>velocitysetter</b>

<img src="images/velocitysetter.png"><br>

<div style="display:inline-block;margin-left:50px;">
set a note's velocity to this value<br><br>
<b>rand</b>: randomness to reduce output velocity by<br>
                   
<b>vel</b>: velocity to use<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=velocitystepsequencer></a><br>

### <b>velocitystepsequencer</b>

<img src="images/velocitystepsequencer.png"><br>

<div style="display:inline-block;margin-left:50px;">
adjusts the velocity of incoming notes based upon a sequence<br><br>
<b>downbeat</b>: should we reset the sequence every downbeat?<br>
                   
<b>interval</b>: speed to advance sequence<br>
                   
<b>len</b>: length of sequence<br>
                   
<b>vel*</b>: velocity for this step<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=vibrato></a><br>

### <b>vibrato</b>

<img src="images/vibrato.png"><br>

<div style="display:inline-block;margin-left:50px;">
add rhythmic oscillating pitch bend to notes<br><br>
<b>vibinterval</b>: speed of pitch bend oscillation<br>
                   
<b>vibrato</b>: amount of pitch bend to add<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=volcabeatscontrol></a><br>

### <b>volcabeatscontrol</b>

<img src="images/volcabeatscontrol.png"><br>

<div style="display:inline-block;margin-left:50px;">
outputs MIDI data to control various aspects of the KORG volca beats drum machine<br><br><br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=whitekeys></a><br>

### <b>whitekeys</b>

<img src="images/whitekeys.png"><br>

<div style="display:inline-block;margin-left:50px;">
remap the white keys that correspond to the C major scale to instead play the current global scale<br><br><br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

## synths
         
<a name=beats></a><br>

### <b>beats</b>

<img src="images/beats.png"><br>

<div style="display:inline-block;margin-left:50px;">
multi-loop player, for mixing sample layers together<br><br>
<b>bars*</b>: how many measures long are the samples in this slot?<br>
                   
<b>double*</b>: enable this to play at double speed<br>
                   
<b>filter*</b>: layer filter. negative values bring in a low pass, positive values bring in a high pass.<br>
                   
<b>pan*</b>: layer panorama<br>
                   
<b>selector*</b>: which sample should we play in this slot? drag samples onto here to add them to this slot.<br>
                   
<b>volume*</b>: layer volume<br>
                   
<br><br><br><br></div>

<a name=drumplayer></a><br>

### <b>drumplayer</b>

<img src="images/drumplayer.png"><br>

<div style="display:inline-block;margin-left:50px;">
sample player intended for drum playback<br><br>
<b>aud</b>: scroll to audition samples in the current pad's head category, or a directory last dropped onto a pad<br>
                   
<b>edit</b>: show pads for editing<br>
                   
<b>envelope *</b>: should we apply a volume envelope to the sample?<br>
                   
<b>envelopedisplay *A</b>: envelope attack<br>
                   
<b>envelopedisplay *D</b>: envelope decay<br>
                   
<b>envelopedisplay *R</b>: envelope release<br>
                   
<b>envelopedisplay *S</b>: envelope sustain<br>
                   
<b>grid</b>: patch a grid in here from a "midicontroller" module<br>
                   
<b>hitcategory*</b>: folder to choose from, when clicking the "random" button. these folders are found in the data/drums/hits/ directory<br>
                   
<b>linkid *</b>: if linkid is not -1, silence any other sample with a matching linkid (useful for linking open and closed hats)<br>
                   
<b>mono</b>: force output to mono<br>
                   
<b>pan *</b>: stereo pan position of sample<br>
                   
<b>quantize</b>: quantize input to this interval<br>
                   
<b>random *</b>: choose a random sample from the selected hitcategory<br>
                   
<b>repeat</b>: if quantizing, should held notes repeat at that interval?<br>
                   
<b>shuffle</b>: random is samples, speeds, and pans<br>
                   
<b>single out *</b>: should the sample have its own individual output?<br>
                   
<b>speed</b>: global sample speed multiplier<br>
                   
<b>speed *</b>: speed of sample<br>
                   
<b>speed rnd</b>: global sample speed randomization amount<br>
                   
<b>start *</b>: start offset percentage of sample<br>
                   
<b>test *</b>: play this sample<br>
                   
<b>view ms *</b>: envelope view length in milliseconds<br>
                   
<b>vol</b>: the output volume<br>
                   
<b>vol *</b>: volume of sample <br>
                   
<b>widen *</b>: stereo delay of sample to create width<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=drumsynth></a><br>

### <b>drumsynth</b>

<img src="images/drumsynth.png"><br>

<div style="display:inline-block;margin-left:50px;">
oscillator+noise drum synth<br><br>
<b>cutoffmax*</b>: filter start cutoff frequency<br>
                   
<b>cutoffmin*</b>: filter end cutoff frequency<br>
                   
<b>edit</b>: display parameters for each hit<br>
                   
<b>freqmax*</b>: oscillator start frequency<br>
                   
<b>freqmin*</b>: oscillator end frequency<br>
                   
<b>noise*</b>: noise volume<br>
                   
<b>q*</b>: filter resonance<br>
                   
<b>type*</b>: oscillator type<br>
                   
<b>vol</b>: the output volume<br>
                   
<b>vol*</b>: oscillator volume<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=fmsynth></a><br>

### <b>fmsynth</b>

<img src="images/fmsynth.png"><br>

<div style="display:inline-block;margin-left:50px;">
polyphonic fm synthesis<br><br>
<b>harmratio</b>: harmonic ratio of first-order modulator to input pitch<br>
                   
<b>harmratio2</b>: harmonic ratio of second-order modulator to input pitch<br>
                   
<b>mod</b>: amount to modulate first-order modulator<br>
                   
<b>mod2</b>: amount to modulate second-order modulator<br>
                   
<b>phase0</b>: phase offset for base oscillator<br>
                   
<b>phase1</b>: phase offset for first-order modulator<br>
                   
<b>phase2</b>: phase offset for second-order modulator<br>
                   
<b>tweak</b>: multiplier to harmonic ratio for first-order modulator<br>
                   
<b>tweak2</b>: multiplier to harmonic ratio for second-order modulator<br>
                   
<b>vol</b>: the output volume<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=karplusstrong></a><br>

### <b>karplusstrong</b>

<img src="images/karplusstrong.png"><br>

<div style="display:inline-block;margin-left:50px;">
polyphonic plucked string physical modeling synth<br><br>
<b>feedback</b>: amount of feedback for resonance<br>
                   
<b>filter</b>: amount to filter resonance<br>
                   
<b>invert</b>: should the feedback invert?<br>
                   
<b>lite cpu</b>: only recalculate some parameters once per buffer, to reduce CPU load. can make pitch bends and rapid modulation sound worse in some scenarios.<br>
                   
<b>pitchtone</b>: adjust how pitch influences filter amount. a value of zero gives even filtering across the entire pitch range, higher values filter high pitches less, low values filter low pitches less.<br>
                   
<b>source type</b>: audio to use for excitation<br>
                   
<b>vel2env</b>: how much velocity should affect excitation attack time<br>
                   
<b>vel2vol</b>: how much velocity should affect voice volume<br>
                   
<b>vol</b>: output volume<br>
                   
<b>x att</b>: fade in time for excitation audio<br>
                   
<b>x dec</b>: fade out time for excitation audio<br>
                   
<b>x freq</b>: frequency of excitation audio<br>
                   <br>accepts: <font color=orange>notes</font> <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=metronome></a><br>

### <b>metronome</b>

<img src="images/metronome.png"><br>

<div style="display:inline-block;margin-left:50px;">
beeps to the beat<br><br>
<b>vol</b>: metronome volume<br>
                   
<br><br><br><br></div>

<a name=oscillator></a><br>

### <b>oscillator</b>

<img src="images/oscillator.png"><br>

<div style="display:inline-block;margin-left:50px;">
polyphonic enveloped oscillator. modulations (with MPE support): modwheel closes filter further (if filter is enabled), pressure decreases detune amount<br><br>
<b>adsr len</b>: view length of ADSR controls<br>
                   
<b>detune</b>: when unison is 1, detunes oscillator by this amount. when unison is 2, one oscillator is tuned normally and the other is detuned by this amount. when unison is >2, oscillators are randomly detuned within this range.<br>
                   
<b>envA</b>: volume envelope attack<br>
                   
<b>envD</b>: volume envelope decay<br>
                   
<b>envR</b>: volume envelope release<br>
                   
<b>envS</b>: volume envelope sustain<br>
                   
<b>envfilterA</b>: filter envelope attack<br>
                   
<b>envfilterD</b>: filter envelope decay<br>
                   
<b>envfilterR</b>: filter envelope release<br>
                   
<b>envfilterS</b>: filter envelope sustain<br>
                   
<b>fmax</b>: frequency cutoff of lowpass filter at the max of the envelope. set this slider to the max to disable the filter<br>
                   
<b>fmin</b>: frequency cutoff of lowpass filter at the min of the envelope<br>
                   
<b>lite cpu</b>: only recalculate some parameters once per buffer, to reduce CPU load. can make pitch bends and rapid modulation sound worse in some scenarios.<br>
                   
<b>mult</b>: multiply frequency of incoming pitch<br>
                   
<b>osc</b>: oscillator type<br>
                   
<b>phase</b>: phase offset of oscillator, and phase offset between unison voices. useful to patch into with a very fast modulator, to achieve phase modulation.<br>
                   
<b>pw</b>: pulse width (or shape for non-square waves)<br>
                   
<b>q</b>: resonance of lowpass filter<br>
                   
<b>shuffle</b>: stretches and squeezes every other cycle of the waveform<br>
                   
<b>soften</b>: soften edges of square and saw waveforms<br>
                   
<b>sync</b>: turns on "sync" mode, to reset the phase at syncf's frequency<br>
                   
<b>syncf</b>: frequency to reset the phase, when "sync" is enabled<br>
                   
<b>unison</b>: how many oscillators to play for one note<br>
                   
<b>vel2env</b>: how much should the input velocity affect the speed of the volume and filter envelopes?<br>
                   
<b>vel2vol</b>: how much should the input velocity affect the output volume?<br>
                   
<b>vol</b>: this oscillator's volume<br>
                   
<b>width</b>: controls how voices are panned with unison is greater than 1<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=samplecanvas></a><br>

### <b>samplecanvas</b>

<img src="images/samplecanvas.png"><br>

<div style="display:inline-block;margin-left:50px;">
sample arranging view<br><br>
<b>canvas</b>: canvas of samples. drag and drop samples onto here. canvas controls:
-hold shift and drag a sample to duplicate
-hold alt to drag a sample without snapping
-hold ctrl while dragging to snap to an interval
-hold shift and scroll to zoom
-hold alt and grab empty space to move slide the canvas view
-hold ctrl and grab empty space to zoom the canvas view<br>
                   
<b>clear</b>: delete all elements<br>
                   
<b>delete</b>: delete highlighted elements<br>
                   
<b>drag mode</b>: direction that elements can be dragged<br>
                   
<b>interval</b>: grid subdivision interval<br>
                   
<b>measures</b>: length of canvas in measures<br>
                   
<b>scrollh</b>: horizontal scrollbar<br>
                   
<b>scrollv</b>: vertical scrollbar<br>
                   
<b>timeline</b>: control loop points<br>
                   
<b>view rows</b>: number of visible rows<br>
                   
<br><br><br><br></div>

<a name=sampleplayer></a><br>

### <b>sampleplayer</b>

<img src="images/sampleplayer.png"><br>

<div style="display:inline-block;margin-left:50px;">
sample playback with triggerable cue points, clip extraction, and youtube search/download functionality. resize this module larger to access additional features. if you have a youtube URL in your clipboard, a button will appear to allow you to download the audio.<br><br>
<b>16</b>: auto-slice 16 slices<br>
                   
<b>32</b>: auto-slice 32 slices<br>
                   
<b>4</b>: auto-slice 4 slices<br>
                   
<b>8</b>: auto-slice 8 slices<br>
                   
<b>append to rec</b>: when recording, append to the previous recording, rather than clearing the sample first<br>
                   
<b>attack</b>: speed at which gate blends open<br>
                   
<b>click sets cue</b>: when true, clicking on the waveform will set the start position of the current cue<br>
                   
<b>cue len</b>: length in seconds of the current cue. a value of zero will play to the end of the sample.<br>
                   
<b>cue speed</b>: playback speed of the current cue<br>
                   
<b>cue start</b>: start point in seconds of the current cue<br>
                   
<b>cuepoint</b>: sets the current cue to edit<br>
                   
<b>grabhovered</b>: grab a sample of this cue to drop onto another module<br>
                   
<b>load</b>: show a file chooser to load a sample<br>
                   
<b>loop</b>: wrap playhead to beginning when it reaches end<br>
                   
<b>pause</b>: pause playing and leave playhead where it is<br>
                   
<b>play</b>: start playing from the current playhead<br>
                   
<b>play cue</b>: play the current cue<br>
                   
<b>playhovered</b>: play this cue<br>
                   
<b>record</b>: record audio input into our sample buffer. clears the current sample.<br>
                   
<b>record as clips</b>: when recording, only record when there is enough input to open the gate, and mark up each recorded segment with cue points<br>
                   
<b>release</b>: speed at which gate blends closed<br>
                   
<b>save</b>: save this sample to a file<br>
                   
<b>searchresult*</b>: click to download this youtube search result. downloading long videos may take a while.<br>
                   
<b>select played</b>: when true, any cue point played via incoming notes will become the current cue<br>
                   
<b>show grid</b>: show a quarter note grid (when zoomed in far enough)<br>
                   
<b>speed</b>: current playback speed<br>
                   
<b>stop</b>: stop playing and reset playhead<br>
                   
<b>threshold</b>: volume threshold to open up the gate for recording<br>
                   
<b>trim</b>: discard all audio outside the current zoom range<br>
                   
<b>volume</b>: output gain<br>
                   
<b>youtube</b>: download the audio of the youtube URL currently on your clipboard<br>
                   
<b>yt:</b>: search youtube for this string<br>
                   <br>accepts: <font color=orange>notes</font> <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=sampler></a><br>

### <b>sampler</b>

<img src="images/sampler.png"><br>

<div style="display:inline-block;margin-left:50px;">
very basic polyphonic pitched sample player and recorder. send audio in, and use note input to play the recorded audio.<br><br>
<b>env</b>: volume envelope<br>
                   
<b>envA</b>: volume envelope attack<br>
                   
<b>envD</b>: volume envelope decay<br>
                   
<b>envR</b>: volume envelope release<br>
                   
<b>envS</b>: volume envelope sustain<br>
                   
<b>passthrough</b>: should input audio pass through as we're recording?<br>
                   
<b>pitch</b>: should we attempt pitch-correct the audio?<br>
                   
<b>rec</b>: enable to clear the current recording, and record new audio once the input threshold is reached<br>
                   
<b>thresh</b>: when recording is enabled, exceed this threshold with input audio to begin recording<br>
                   
<b>vol</b>: output volume<br>
                   <br>accepts: <font color=orange>notes</font> <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=seaofgrain></a><br>

### <b>seaofgrain</b>

<img src="images/seaofgrain.png"><br>

<div style="display:inline-block;margin-left:50px;">
granular synth, playable with sliders or MPE input<br><br>
<b>display length</b>: amount of sample to view<br>
                   
<b>gain *</b>: volume of this voice<br>
                   
<b>keyboard base pitch</b>: midi pitch that represents the start of the sample<br>
                   
<b>keyboard num pitches</b>: amount of pitches to assign across the sample<br>
                   
<b>len ms *</b>: length of each grain in milliseconds<br>
                   
<b>load</b>: load a sample file<br>
                   
<b>octaves *</b>: should we add octaves and fifths?<br>
                   
<b>offset</b>: where to start view of the sample<br>
                   
<b>overlap *</b>: number of overlapping grains<br>
                   
<b>pan *</b>: stereo panorama of grain placement<br>
                   
<b>pos *</b>: position of this voice within the sample<br>
                   
<b>pos r *</b>: randomization of grain start point<br>
                   
<b>record</b>: record input as the granular buffer, to use seaofgrain a live granular delay<br>
                   
<b>spacing r*</b>: randomization of time between grains<br>
                   
<b>speed *</b>: speed of grain playback<br>
                   
<b>speed r *</b>: randomization of grain speed<br>
                   
<b>volume</b>: output volume<br>
                   
<b>width *</b>: stereo width of grain placement<br>
                   <br>accepts: <font color=orange>notes</font> <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=signalgenerator></a><br>

### <b>signalgenerator</b>

<img src="images/signalgenerator.png"><br>

<div style="display:inline-block;margin-left:50px;">
basic oscillator signal<br><br>
<b>detune</b>: amount to detune from specified frequency<br>
                   
<b>freq</b>: signal frequency<br>
                   
<b>freq mode</b>: what mode should we use for input notes? "instant" changes to the input note's frequency instantly, "ramp" ramps to the frequency over time, and "slider" allows you to use a slider to interpolate between the last two input notes<br>
                   
<b>mult</b>: multiplier for frequency<br>
                   
<b>osc</b>: oscillator type<br>
                   
<b>phase</b>: phase offset<br>
                   
<b>pw</b>: pulse width (or shape for non-square waves)<br>
                   
<b>ramp</b>: amount of time to ramp to input frequency<br>
                   
<b>shuffle</b>: stretches and squeezes every other cycle of the waveform<br>
                   
<b>slider</b>: slider to interpolate between last two input pitches<br>
                   
<b>soften</b>: soften edges of square and saw waveforms<br>
                   
<b>sync</b>: turns on "sync" mode, to reset the phase at syncf's frequency<br>
                   
<b>syncf</b>: frequency to reset the phase, when "sync" is enabled<br>
                   
<b>vol</b>: output volume<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

## audio effects
         
<a name=audiometer></a><br>

### <b>audiometer</b>

<img src="images/audiometer.png"><br>

<div style="display:inline-block;margin-left:50px;">
sets a slider to an audio level's volume. useful to map a midi display value to.<br><br>
<b>level</b>: the input audio level. hook this up to an LED-display midi control to see the value displayed on your controller.<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=audiorouter></a><br>

### <b>audiorouter</b>

<img src="images/audiorouter.png"><br>

<div style="display:inline-block;margin-left:50px;">
selector for switching where audio is routed to. connect to targets to add them to the list.<br><br>
<b>route</b>: audio destination<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=dcoffset></a><br>

### <b>dcoffset</b>

<img src="images/dcoffset.png"><br>

<div style="display:inline-block;margin-left:50px;">
add a constant offset to an audio signal<br><br>
<b>offset</b>: amount of offset to add<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=effectchain></a><br>

### <b>effectchain</b>

<img src="images/effectchain.png"><br>

<div style="display:inline-block;margin-left:50px;">
container to hold a list of effects, applied in series. the effects can be easily reordered with the < and > buttons, and deleted with the x button. hold shift to expose a x button for all effects.<br><br>
<b><</b>: move this effect to earlier in the chain<br>
                   
<b>></b>: move this effect to later in the chain<br>
                   
<b>effect</b>: select which effect to add<br>
                   
<b>exit effect</b>: on push2, back effect control out to the main effectchain controls<br>
                   
<b>mix*</b>: wet/dry slider for this effect<br>
                   
<b>spawn</b>: spawn the currently highlighted effect<br>
                   
<b>volume</b>: output gain<br>
                   
<b>x</b>: delete this effect<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=eq></a><br>

### <b>eq</b>

<img src="images/eq.png"><br>

<div style="display:inline-block;margin-left:50px;">
multi-band equalizer, to adjust output levels at frequency ranges<br><br>
<b>enabled*</b>: enable this band?<br>
                   
<b>f*</b>: frequency cutoff for this band<br>
                   
<b>g*</b>: gain for this band<br>
                   
<b>q*</b>: resonance for this band<br>
                   
<b>type*</b>: what type of filter should this band use<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=feedback></a><br>

### <b>feedback</b>

<img src="images/feedback.png"><br>

<div style="display:inline-block;margin-left:50px;">
feed delayed audio back into earlier in the signal chain. use the "feedback out" connector for sending the audio back up the chain, and the primary output connector for sending the resulting audio forward. using feedback can often lead to extreme and difficult-to-control results!<br><br>
<b>limit</b>: clip the feedback audio to this range, to avoid issues with feedback blowing out too intensely.<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=fftvocoder></a><br>

### <b>fftvocoder</b>

<img src="images/fftvocoder.png"><br>

<div style="display:inline-block;margin-left:50px;">
FFT-based vocoder<br><br>
<b>carrier</b>: carrier signal gain<br>
                   
<b>cut</b>: how many bass partials to remove<br>
                   
<b>dry/wet</b>: how much original input vs vocoded signal to output<br>
                   
<b>fric thresh</b>: fricative detection sensitivity, to switch between using the carrier signal and white noise for vocoding<br>
                   
<b>input</b>: input signal gain<br>
                   
<b>phase off</b>: how much we should offset the phase of the carrier signal's partials<br>
                   
<b>volume</b>: output gain<br>
                   
<b>whisper</b>: how much the carrier signal partial's phases should be randomized, which affects how whispery the output sound is<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=freqdelay></a><br>

### <b>freqdelay</b>

<img src="images/freqdelay.png"><br>

<div style="display:inline-block;margin-left:50px;">
delay effect with delay length based upon input notes<br><br>
<b>dry/wet</b>: how much of the effect to apply<br>
                   <br>accepts: <font color=orange>notes</font> <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=gain></a><br>

### <b>gain</b>

<img src="images/gain.png"><br>

<div style="display:inline-block;margin-left:50px;">
adjusts volume of audio signal<br><br>
<b>gain</b>: amount to adjust signal. a value of 1 will cause no change to the signal.<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=input></a><br>

### <b>input</b>

<img src="images/input.png"><br>

<div style="display:inline-block;margin-left:50px;">
get audio from input source, like a microphone<br><br>
<b>ch</b>: which channel (or channels, if you want stereo) to use<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=inverter></a><br>

### <b>inverter</b>

<img src="images/inverter.png"><br>

<div style="display:inline-block;margin-left:50px;">
multiply a signal by -1. enables some pretty interesting effects when used with sends, to subtract out parts of signals when recombined.<br><br><br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=lissajous></a><br>

### <b>lissajous</b>

<img src="images/lissajous.png"><br>

<div style="display:inline-block;margin-left:50px;">
draw input audio as a lissajous curve. turn off "autocorrelation" in the module's triangle menu to use stereo channels to show stereo width.<br><br>
<b>scale</b>: visual scale of lissajous image<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=looper></a><br>

### <b>looper</b>

<img src="images/looper.png"><br>

<div style="display:inline-block;margin-left:50px;">
loop input audio. use with a "looperrecorder" for full functionality.<br><br>
<b> m </b>: take the contents of this looper and merge it into another. click this button on the merge source, then on the merge target.<br>
                   
<b>.5x</b>: make loop play at half speed<br>
                   
<b>2x</b>: make loop play at double speed<br>
                   
<b>auto</b>: should pitch shift auto-adjust as the transport tempo adjusts?<br>
                   
<b>b</b>: bake current volume into waveform<br>
                   
<b>capture</b>: when the next loop begins, record input for the duration of the loop<br>
                   
<b>clear</b>: clear the loop audio<br>
                   
<b>commit</b>: commit the current looperrecorder buffer to this loop<br>
                   
<b>copy</b>: take the contents of this looper and copy it onto another. click this button on the copy source, then on the copy target.<br>
                   
<b>decay</b>: amount to lower volume each loop<br>
                   
<b>fourtet</b>: use a textural trick I saw four tet illustrate in a video once: slice the audio into chunks, and for each chunk it at double speed followed by playing it in reverse at double speed. this slider adjusts the mix between the original audio and this "fourtetified" audio.<br>
                   
<b>fourtetslices</b>: chunk size to use for "fourtet" effect<br>
                   
<b>mute</b>: silence this looper<br>
                   
<b>num bars</b>: loop length in measures<br>
                   
<b>offset</b>: amount to offset looper's playhead from transport position<br>
                   
<b>pitch</b>: amount to pitch shift looper output<br>
                   
<b>resample for tempo</b>: this button appears when the current global tempo no longer matches the tempo that the buffer was recorded at. click this to resample the buffer to match the new tempo.<br>
                   
<b>save</b>: save this loop to a wav file<br>
                   
<b>scr</b>: allow loop to be scrached by adjusting "scrspd"<br>
                   
<b>scrspd</b>: playback speed, used with "scr" is enabled. modulate quickly for a vinyl-like scratching effect.<br>
                   
<b>set</b>: shift the contents of the looper so the current offset is the start of the buffer<br>
                   
<b>swap</b>: swap the contents of this looper and with another. click this button on two loopers to swap them.<br>
                   
<b>undo</b>: undo last loop commit<br>
                   
<b>volume</b>: output volume<br>
                   
<b>write</b>: write input audio to loop buffer<br>
                   <br>accepts: <font color=orange>notes</font> <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=looperrecorder></a><br>

### <b>looperrecorder</b>

<img src="images/looperrecorder.png"><br>

<div style="display:inline-block;margin-left:50px;">
command center to manage recording into multiple loopers, and allow retroactive loop capture (i.e., always-on recording)<br><br>
<b>.5tempo</b>: halve global transport tempo, while keeping connected loopers sounding the same<br>
                   
<b>1</b>: capture the last measure to the currently-targeted looper<br>
                   
<b>2</b>: capture the last 2 measures to the currently-targeted looper<br>
                   
<b>2xtempo</b>: double global transport tempo, while keeping connected loopers sounding the same<br>
                   
<b>4</b>: capture the last 4 measures to the currently-targeted looper<br>
                   
<b>8</b>: capture the last 8 measures to the currently-targeted looper<br>
                   
<b>cancel free rec</b>: if "free rec" is enabled, cancel recording without setting the loop length<br>
                   
<b>clear</b>: clear the recorded buffer<br>
                   
<b>free rec</b>: enable to start recording a loop with no predetermined length. disable to end recording, adjust global transport to match the loop length, and switch the recorder's mode to "loop"<br>
                   
<b>length</b>: length in measures to use when connected loopers use the "commit" button<br>
                   
<b>mode</b>: recorder mode: use "record" to record input and allow it to be committed to buffers when you're ready to loop, use "overdub" to record input and play the loop at our specified length, and use "loop" to play the current loop without adding input<br>
                   
<b>orig speed</b>: reset looper to tempo that loops were recorded at<br>
                   
<b>resample</b>: resample all connected loopers to new tempo<br>
                   
<b>resample & set key</b>: snap tempo to nearest value that matches a key (based upon the current key and the tempo change), resample all connected loopers to that new tempo, and change global scale to the new key<br>
                   
<b>snap to pitch</b>: snap tempo to nearest value that matches a key<br>
                   
<b>target</b>: looper to commit audio to when using the on-buffer capture buttons to the left<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=looperrewriter></a><br>

### <b>looperrewriter</b>

<img src="images/looperrewriter.png"><br>

<div style="display:inline-block;margin-left:50px;">
rewrites the contents of a looper with received input, to help you resample your own loops. attach the grey dot to a "looper" module.

the ideal way to use this module is to hook the "looper" directly up to a "send", hook the leftmost outlet of the "send" up to your effects processing (like an "effectchain"), hook the effect processing up to this "rewriter", and then also connect the rightmost outlet of the "send" up to this "rewriter"<br><br>
<b> go </b>: rewrite the connected looper, and if that looper is connected to a send, set that send to output only to the right outlet<br>
                   
<b>new loop</b>: start recording a dynamic loop length. press "go" when you want to rewrite it to the looper. this will also change bespoke's global tempo to match this new loop, so it's quite powerful and scary! click it again to cancel.<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=multitapdelay></a><br>

### <b>multitapdelay</b>

<img src="images/multitapdelay.png"><br>

<div style="display:inline-block;margin-left:50px;">
delay with multiple tap points<br><br>
<b>delay *</b>: tap delay time, in milliseconds<br>
                   
<b>display length</b>: length of buffer display, in seconds<br>
                   
<b>dry</b>: how much dry signal to allow through<br>
                   
<b>feedback *</b>: how much delayed audio from this tap should feed back in to the input<br>
                   
<b>gain *</b>: tap delay amount<br>
                   
<b>pan *</b>: stereo pan for this tap<br>
                   <br>accepts: <font color=orange>notes</font> <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=output></a><br>

### <b>output</b>

<img src="images/output.png"><br>

<div style="display:inline-block;margin-left:50px;">
route audio in here to send it to an output channel (your speakers or audio interface)<br><br>
<b>ch</b>: channel (or channels, if you want stereo) to send audio to<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=panner></a><br>

### <b>panner</b>

<img src="images/panner.png"><br>

<div style="display:inline-block;margin-left:50px;">
pan audio left and right. also, converts a mono input to a stereo output.<br><br>
<b>pan</b>: amount to send signal to the left and right channels. a value of .5 is centered.<br>
                   
<b>widen</b>: delay a channel by this many samples. results in a pan-like effect where the sound seems to come from from a direction.<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=ringmodulator></a><br>

### <b>ringmodulator</b>

<img src="images/ringmodulator.png"><br>

<div style="display:inline-block;margin-left:50px;">
modulate a signal's amplitude at a frequency<br><br>
<b>dry/wet</b>: how much of the original audio to use vs modulated audio<br>
                   
<b>freq</b>: frequency to use. can also be set by patching a note input into this module.<br>
                   
<b>glide</b>: how long an input note should take to glide to the desired frequency<br>
                   
<b>volume</b>: volume output<br>
                   <br>accepts: <font color=orange>notes</font> <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=samplergrid></a><br>

### <b>samplergrid</b>

<img src="images/samplergrid.png"><br>

<div style="display:inline-block;margin-left:50px;">
record input onto pads, and play back the pads. intended to be used with an 64-pad grid controller.<br><br>
<b>clear</b>: when enabled, clears any pressed grid squares<br>
                   
<b>duplicate</b>: what enabled, duplicates last pressed sample onto any pressed grid squares<br>
                   
<b>edit</b>: enable controls to adjust recorded sample for last pressed grid square<br>
                   
<b>end</b>: sample end<br>
                   
<b>grid</b>: patch a grid in here from a "midicontroller" module<br>
                   
<b>passthrough</b>: should the incoming audio pass through to the output?<br>
                   
<b>start</b>: sample start<br>
                   
<b>vol</b>: the output volume<br>
                   <br>accepts: <font color=orange>notes</font> <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=send></a><br>

### <b>send</b>

<img src="images/send.png"><br>

<div style="display:inline-block;margin-left:50px;">
duplicate a signal and send it to a second destination<br><br>
<b>amount</b>: amount to send out the right-side cable<br>
                   
<b>crossfade</b>: when true, output of the left-side cable is reduced as "amount" increases<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=signalclamp></a><br>

### <b>signalclamp</b>

<img src="images/signalclamp.png"><br>

<div style="display:inline-block;margin-left:50px;">
clamps an audio signal's value within a range<br><br>
<b>max</b>: maximum output value<br>
                   
<b>min</b>: minimum output value<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=spectrum></a><br>

### <b>spectrum</b>

<img src="images/spectrum.png"><br>

<div style="display:inline-block;margin-left:50px;">
display audio signal's spectral data<br><br><br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=splitter></a><br>

### <b>splitter</b>

<img src="images/splitter.png"><br>

<div style="display:inline-block;margin-left:50px;">
splits a stereo signal into two mono signals, or duplicates a mono signal<br><br><br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=stutter></a><br>

### <b>stutter</b>

<img src="images/stutter.png"><br>

<div style="display:inline-block;margin-left:50px;">
captures and stutters input<br><br>
<b>16th</b>: 16th note stutter<br>
                   
<b>32nd</b>: 32nd note stutter<br>
                   
<b>64th</b>: 64th note stutter<br>
                   
<b>8th</b>: 8th note stutter<br>
                   
<b>dotted eighth</b>: stutter on a dotted eighth interval<br>
                   
<b>double speed</b>: stutter at double speed, high pitched<br>
                   
<b>free</b>: stutter with the settings specified by the following sliders<br>
                   
<b>free length</b>: length in seconds for "free" stutter mode<br>
                   
<b>free speed</b>: rate for "free" stutter mode<br>
                   
<b>grid</b>: patch a grid in here from a "midicontroller" module<br>
                   
<b>half note</b>: half note stutter<br>
                   
<b>half speed</b>: stutter at half speed, low pitched<br>
                   
<b>quarter</b>: quarter note stutter<br>
                   
<b>ramp in</b>: stutter with speed climbing up from zero to one<br>
                   
<b>ramp out</b>: stutter with speed quickly falling to zero<br>
                   
<b>reverse</b>: reversed half note stutter<br>
                   
<b>triplets</b>: stutter on a triplet interval<br>
                   
<b>tumble down</b>: decelerating stutter<br>
                   
<b>tumble up</b>: accelerating stutter<br>
                   <br>accepts: <font color=orange>notes</font> <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=vocoder></a><br>

### <b>vocoder</b>

<img src="images/vocoder.png"><br>

<div style="display:inline-block;margin-left:50px;">
frequency band-based vocoder. this must be paired with a "vocodercarrier" module. voice should be routed into this module, and a synth should be patched into the vocodercarrier.<br><br>
<b>bands</b>: how many frequency bands to use<br>
                   
<b>carrier</b>: carrier signal gain<br>
                   
<b>f base</b>: frequency for lowest band<br>
                   
<b>f range</b>: frequency range to highest band<br>
                   
<b>input</b>: input signal gain<br>
                   
<b>max band</b>: volume limit for each frequency band<br>
                   
<b>mix</b>: how much original input vs vocoded signal to output<br>
                   
<b>q</b>: resonance of the bands<br>
                   
<b>ring</b>: how long it should take the bands to "cool down"<br>
                   
<b>spacing</b>: how frequency bands should be spaced<br>
                   
<b>volume</b>: output gain<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=vocodercarrier></a><br>

### <b>vocodercarrier</b>

<img src="images/vocodercarrier.png"><br>

<div style="display:inline-block;margin-left:50px;">
connect to "vocoder" or "fftvocoder" modules. send the synth audio into this module, and the voice audio into the vocoder module.<br><br><br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=waveformviewer></a><br>

### <b>waveformviewer</b>

<img src="images/waveformviewer.png"><br>

<div style="display:inline-block;margin-left:50px;">
waveform display<br><br>
<b>draw gain</b>: adjust waveform display scale<br>
                   
<b>freq</b>: frequency to sync display to. gets automatically set if you patch a note input into this module<br>
                   
<b>length</b>: number of samples to capture<br>
                   <br>accepts: <font color=orange>notes</font> <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=waveshaper></a><br>

### <b>waveshaper</b>

<img src="images/waveshaper.png"><br>

<div style="display:inline-block;margin-left:50px;">
waveshaping with expressions<br><br>
<b>a</b>: variable to use in expressions<br>
                   
<b>b</b>: variable to use in expressions<br>
                   
<b>c</b>: variable to use in expressions<br>
                   
<b>d</b>: variable to use in expressions<br>
                   
<b>e</b>: variable to use in expressions<br>
                   
<b>rescale</b>: rescales input before feeding it into expression<br>
                   
<b>y=</b>: waveshaping expression. try something like "x+sin(x*pi*a)". available variables: a,b,c,d,e = the slider + sin(s below. t = time. x1,x2,y1,y2 = biquad state storage.<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

## modulators
         
<a name=accum></a><br>

### <b>accum</b>

<img src="images/accum.png"><br>

<div style="display:inline-block;margin-left:50px;">
accumulate a value over time<br><br>
<b>value</b>: output value<br>
                   
<b>velocity</b>: amount to accumulate<br>
                   
<br><br><br><br></div>

<a name=add></a><br>

### <b>add</b>

<img src="images/add.png"><br>

<div style="display:inline-block;margin-left:50px;">
outputs the result of value 1 plus value 2. value 1 and value 2 are intended to be patch targets for modulators.<br><br>
<b>value 1</b>: value to sum<br>
                   
<b>value 2</b>: value to sum<br>
                   
<br><br><br><br></div>

<a name=addcentered></a><br>

### <b>addcentered</b>

<img src="images/addcentered.png"><br>

<div style="display:inline-block;margin-left:50px;">
outputs the result of value 1 plus value 2, multiplied by range 2. optimized for using to modulation value 1 by range 2 at a frequency. value 1 or value 2 are intended to be patch targets for modulators.<br><br>
<b>range 2</b>: modulation amount<br>
                   
<b>value 1</b>: center value<br>
                   
<b>value 2</b>: modulation value<br>
                   
<br><br><br><br></div>

<a name=audiotocv></a><br>

### <b>audiotocv</b>

<img src="images/audiotocv.png"><br>

<div style="display:inline-block;margin-left:50px;">
use an audio signal to modulate a control. allow for audio-rate modulation, to achieve effects such as FM.<br><br>
<b>gain</b>: multiply incoming audio<br>
                   
<b>max</b>: maximum output value<br>
                   
<b>min</b>: minimum output value<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=controlsequencer></a><br>

### <b>controlsequencer</b>

<img src="images/controlsequencer.png"><br>

<div style="display:inline-block;margin-left:50px;">
modulate a control step-wise at an interval<br><br>
<b>interval</b>: rate to advance<br>
                   
<b>length</b>: length of the sequence<br>
                   
<b>random</b>: randomize sequence values<br>
                   
<br><br><br><br></div>

<a name=curve></a><br>

### <b>curve</b>

<img src="images/curve.png"><br>

<div style="display:inline-block;margin-left:50px;">
remap an input over its range with a curve. double-click on the curve to add points, right click on points to remove them, drag on lines to bend them.<br><br>
<b>input</b>: input value (intended as a modulation target)<br>
                   
<br><br><br><br></div>

<a name=curvelooper></a><br>

### <b>curvelooper</b>

<img src="images/curvelooper.png"><br>

<div style="display:inline-block;margin-left:50px;">
modulate a value over time with a looping curve<br><br>
<b>length</b>: length of the loop<br>
                   
<b>randomize</b>: create a random curve<br>
                   
<br><br><br><br></div>

<a name=envelope></a><br>

### <b>envelope</b>

<img src="images/envelope.png"><br>

<div style="display:inline-block;margin-left:50px;">
modulate a value with a triggered envelope<br><br>
<b>adsr</b>: envelope view<br>
                   
<b>adsrA</b>: envelope attack<br>
                   
<b>adsrD</b>: envelope decay<br>
                   
<b>adsrR</b>: envelope release<br>
                   
<b>adsrS</b>: envelope sustain<br>
                   
<b>advanced</b>: switch to advanced envelope editor (allows for a more complicated envelope than just an ADSR). double-click on an advanced envelope line to add stages, right click on points to remove them, drag on lines to bend them.<br>
                   
<b>has sustain</b>: should this envelope have a sustain stage?<br>
                   
<b>high</b>: output high value<br>
                   
<b>length</b>: length of envelope display<br>
                   
<b>low</b>: output low value<br>
                   
<b>max sustain</b>: what's the maximum length of the sustain, in milliseconds? a value of -1 indicates no maximum<br>
                   
<b>sustain stage</b>: which step of the envelope should have the sustain?<br>
                   
<b>use velocity</b>: should envelope output be scaled by input velocity?<br>
                   <br>accepts: <font color=yellow>pulses</font> <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=expression></a><br>

### <b>expression</b>

<img src="images/expression.png"><br>

<div style="display:inline-block;margin-left:50px;">
shape modulation with a text-based mathematical expression<br><br>
<b>a</b>: variable to use in expressions<br>
                   
<b>b</b>: variable to use in expressions<br>
                   
<b>c</b>: variable to use in expressions<br>
                   
<b>d</b>: variable to use in expressions<br>
                   
<b>e</b>: variable to use in expressions<br>
                   
<b>input</b>: input to use as x variable<br>
                   
<b>y=</b>: expression to modify input. try something like "x+sin(x*pi*a)". available variables: a,b,c,d,e = the slider + sin(s below. t = time. x1,x2,y1,y2 = biquad state storage.<br>
                   
<br><br><br><br></div>

<a name=fubble></a><br>

### <b>fubble</b>

<img src="images/fubble.png"><br>

<div style="display:inline-block;margin-left:50px;">
draw on an X/Y pad and replay the drawing to modulate values. based on a concept proposed by olivia jack<br><br>
<b>clear</b>: clear the drawing<br>
                   
<b>length</b>: the interval to quantize to<br>
                   
<b>mutate amount</b>: amount to affect drawing by perlin noise field<br>
                   
<b>mutate noise</b>: rate to move through perlin noise field<br>
                   
<b>mutate warp</b>: scale of perlin noise field<br>
                   
<b>quantize</b>: should we quantize playback to a specified rhythmic interval?<br>
                   
<b>reseed</b>: jump to a different location in the perlin noise field<br>
                   
<b>speed</b>: speed up or slow down playback<br>
                   
<br><br><br><br></div>

<a name=gravity></a><br>

### <b>gravity</b>

<img src="images/gravity.png"><br>

<div style="display:inline-block;margin-left:50px;">
make a modulation value rise and fall with physics<br><br>
<b>drag</b>: the resistance force to apply opposite the velocity<br>
                   
<b>gravity</b>: the gravitational force to apply downwards<br>
                   
<b>kick</b>: click to apply kick force (or, pulse this module for the same result)<br>
                   
<b>kick amt</b>: the amount of upward force to apply when kicking<br>
                   <br>accepts: <font color=yellow>pulses</font> <br>
<br><br><br><br></div>

<a name=gridsliders></a><br>

### <b>gridsliders</b>

<img src="images/gridsliders.png"><br>

<div style="display:inline-block;margin-left:50px;">
use a grid controller to control multiple sliders<br><br>
<b>direction</b>: should the grid display the sliders vertically, or horizontally?<br>
                   
<b>grid</b>: patch a grid in here from a "midicontroller" module<br>
                   
<br><br><br><br></div>

<a name=leveltocv></a><br>

### <b>leveltocv</b>

<img src="images/leveltocv.png"><br>

<div style="display:inline-block;margin-left:50px;">
output a modulation value based on the level of incoming audio<br><br>
<b>attack</b>: rise to the input level at this rate<br>
                   
<b>gain</b>: multiply the input audio by this value<br>
                   
<b>max</b>: output when level is one<br>
                   
<b>min</b>: output when level is zero<br>
                   
<b>release</b>: decay from the input level at this rate<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=macroslider></a><br>

### <b>macroslider</b>

<img src="images/macroslider.png"><br>

<div style="display:inline-block;margin-left:50px;">
take a value and send scaled versions of that value to multiple destinations<br><br>
<b>end*</b>: the output value at the top of the input's range<br>
                   
<b>input</b>: the input value. intended to be a modulation patch target.<br>
                   
<b>start*</b>: the output value at the bottom of the input's range<br>
                   
<br><br><br><br></div>

<a name=modwheeltocv></a><br>

### <b>modwheeltocv</b>

<img src="images/modwheeltocv.png"><br>

<div style="display:inline-block;margin-left:50px;">
take a note's modwheel value and convert it to a modulation value<br><br>
<b>max</b>: output for modwheel value 127<br>
                   
<b>min</b>: output for modwheel value 0<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=mult></a><br>

### <b>mult</b>

<img src="images/mult.png"><br>

<div style="display:inline-block;margin-left:50px;">
outputs the result of value 1 multiplier by value 2. value 1 and value 2 are intended to be patch targets for modulators.<br><br>
<br><br><br><br></div>

<a name=notetofreq></a><br>

### <b>notetofreq</b>

<img src="images/notetofreq.png"><br>

<div style="display:inline-block;margin-left:50px;">
takes an input note, and outputs that note's frequency in hertz<br><br><br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=notetoms></a><br>

### <b>notetoms</b>

<img src="images/notetoms.png"><br>

<div style="display:inline-block;margin-left:50px;">
takes an input note, and outputs the period of that note's frequency in milliseconds. useful for setting delay lines to create specific pitches.<br><br><br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=pitchtocv></a><br>

### <b>pitchtocv</b>

<img src="images/pitchtocv.png"><br>

<div style="display:inline-block;margin-left:50px;">
take a note's pitch and convert it to a modulation value<br><br>
<b>max</b>: output for pitch 127<br>
                   
<b>min</b>: output for pitch 0<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=pitchtospeed></a><br>

### <b>pitchtospeed</b>

<img src="images/pitchtospeed.png"><br>

<div style="display:inline-block;margin-left:50px;">
convert an input pitch to a speed ratio. you could use this to control a sample's playback speed and make it playable with a keyboard.<br><br>
<b>ref freq</b>: the output is the input frequency divided by this number<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=pressuretocv></a><br>

### <b>pressuretocv</b>

<img src="images/pressuretocv.png"><br>

<div style="display:inline-block;margin-left:50px;">
take a note's pressure and convert it to a modulation value<br><br>
<b>max</b>: output for pressure 127<br>
                   
<b>min</b>: output for pressure 0<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=ramper></a><br>

### <b>ramper</b>

<img src="images/ramper.png"><br>

<div style="display:inline-block;margin-left:50px;">
blend a control to a specified value over a specified time<br><br>
<b>length</b>: length of time to blend over<br>
                   
<b>start</b>: begin blending (or, send a pulse to this module for the same result)<br>
                   
<b>target</b>: the value to arrive at when the ramp is over<br>
                   <br>accepts: <font color=yellow>pulses</font> <br>
<br><br><br><br></div>

<a name=smoother></a><br>

### <b>smoother</b>

<img src="images/smoother.png"><br>

<div style="display:inline-block;margin-left:50px;">
outputs a smoothed value of the input<br><br>
<b>input</b>: set a value to smooth, patch a modulator into here<br>
                   
<b>smooth</b>: amount of smoothing to apply<br>
                   
<br><br><br><br></div>

<a name=subtract></a><br>

### <b>subtract</b>

<img src="images/subtract.png"><br>

<div style="display:inline-block;margin-left:50px;">
outputs the result of value 2 subtracted from value 1. value 1 and value 2 are intended to be patch targets for modulators.<br><br>
<br><br><br><br></div>

<a name=valuesetter></a><br>

### <b>valuesetter</b>

<img src="images/valuesetter.png"><br>

<div style="display:inline-block;margin-left:50px;">
set a specified value on a targeted control<br><br>
<b>set</b>: click here to send the value (or, send a pulse to this module for the same result)<br>
                   
<b>value</b>: value to set<br>
                   <br>accepts: <font color=yellow>pulses</font> <br>
<br><br><br><br></div>

<a name=velocitytocv></a><br>

### <b>velocitytocv</b>

<img src="images/velocitytocv.png"><br>

<div style="display:inline-block;margin-left:50px;">
take a note's velocity and convert it to a modulation value<br><br>
<b>max</b>: output for velocity 127<br>
                   
<b>min</b>: output for velocity 0<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=vinylcontrol></a><br>

### <b>vinylcontrol</b>

<img src="images/vinylcontrol.png"><br>

<div style="display:inline-block;margin-left:50px;">
modulator which outputs a speed value based upon control vinyl input audio. provide it with a stereo signal from control vinyl (like you'd use to control serato) patched in from an "input" module.<br><br>
<b>control</b>: enable/disable transport control. when you enable it, it will use the current speed as the reference speed (so, the output will output a value of 1 until you change the vinyl's speed)<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

## pulse
         
<a name=audiotopulse></a><br>

### <b>audiotopulse</b>

<img src="images/audiotopulse.png"><br>

<div style="display:inline-block;margin-left:50px;">
sends a pulse when the audio level surpasses a specified threshold<br><br>
<b>release</b>: the cooldown time for the audio signal before a pulse can be triggered again<br>
                   
<b>threshold</b>: send a pulse when the signal hits this threshold<br>
                   <br>accepts: <font color=cyan>audio</font> <br>
<br><br><br><br></div>

<a name=notetopulse></a><br>

### <b>notetopulse</b>

<img src="images/notetopulse.png"><br>

<div style="display:inline-block;margin-left:50px;">
trigger a pulse whenever a note is received<br><br><br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=pulsebutton></a><br>

### <b>pulsebutton</b>

<img src="images/pulsebutton.png"><br>

<div style="display:inline-block;margin-left:50px;">
trigger a pulse with a button press<br><br>
<b>pulse</b>: trigger a pulse<br>
                   
<br><br><br><br></div>

<a name=pulsechance></a><br>

### <b>pulsechance</b>

<img src="images/pulsechance.png"><br>

<div style="display:inline-block;margin-left:50px;">
randomly allow pulses through, based on chance<br><br>
<b>chance</b>: chance that pulses are allowed through<br>
                   <br>accepts: <font color=yellow>pulses</font> <br>
<br><br><br><br></div>

<a name=pulsedelayer></a><br>

### <b>pulsedelayer</b>

<img src="images/pulsedelayer.png"><br>

<div style="display:inline-block;margin-left:50px;">
delay pulses<br><br>
<b>delay</b>: time to delay, in fractions of a measure<br>
                   <br>accepts: <font color=yellow>pulses</font> <br>
<br><br><br><br></div>

<a name=pulsegate></a><br>

### <b>pulsegate</b>

<img src="images/pulsegate.png"><br>

<div style="display:inline-block;margin-left:50px;">
control if pulses are allowed through<br><br>
<b>allow</b>: can pulses pass through?<br>
                   <br>accepts: <font color=yellow>pulses</font> <br>
<br><br><br><br></div>

<a name=pulsehocket></a><br>

### <b>pulsehocket</b>

<img src="images/pulsehocket.png"><br>

<div style="display:inline-block;margin-left:50px;">
sends pulses to randomized destinations<br><br>
<b>weight *</b>: chance that pulse goes to this destination<br>
                   <br>accepts: <font color=yellow>pulses</font> <br>
<br><br><br><br></div>

<a name=pulser></a><br>

### <b>pulser</b>

<img src="images/pulser.png"><br>

<div style="display:inline-block;margin-left:50px;">
send pulse messages at an interval<br><br>
<b>div</b>: measure division, when using "div" as the interval<br>
                   
<b>interval</b>: rate to send pulses<br>
                   
<b>offset</b>: pulse time offset, in fractions of a measure<br>
                   
<b>random</b>: tell pulsed modules to randomize their position<br>
                   
<b>reset</b>: length of sequence before sending reset pulse<br>
                   
<b>t</b>: pulse interval in milliseconds<br>
                   
<b>timemode</b>: when to send downbeat pulses, or set to "free" for pulses not locked to the transport<br>
                   
<br><br><br><br></div>

<a name=pulsesequence></a><br>

### <b>pulsesequence</b>

<img src="images/pulsesequence.png"><br>

<div style="display:inline-block;margin-left:50px;">
defines a looping sequence of pulses<br><br>
<b><</b>: shift sequence to the left<br>
                   
<b>></b>: shift sequence to the right<br>
                   
<b>interval</b>: length of each step within the sequence<br>
                   
<b>length</b>: length of the sequence<br>
                   <br>accepts: <font color=yellow>pulses</font> <br>
<br><br><br><br></div>

<a name=pulsetrain></a><br>

### <b>pulsetrain</b>

<img src="images/pulsetrain.png"><br>

<div style="display:inline-block;margin-left:50px;">
defines a list of pulses to execute, once pulsed<br><br>
<b>interval</b>: length of each step within the sequence<br>
                   
<b>length</b>: length of the sequence<br>
                   <br>accepts: <font color=yellow>pulses</font> <br>
<br><br><br><br></div>

## effect chain
         
<a name=basiceq></a><br>

### <b>basiceq</b>

<img src="images/basiceq.png"><br>

<div style="display:inline-block;margin-left:50px;">
simple multiband EQ<br><br>
<b>even</b>: reset EQ<br>
                   
<br><br><br><br></div>

<a name=biquad></a><br>

### <b>biquad</b>

<img src="images/biquad.png"><br>

<div style="display:inline-block;margin-left:50px;">
filter using biquad formula<br><br>
<b>F</b>: frequency cutoff<br>
                   
<b>G</b>: gain<br>
                   
<b>Q</b>: resonance<br>
                   
<b>type</b>: filter type<br>
                   
<br><br><br><br></div>

<a name=bitcrush></a><br>

### <b>bitcrush</b>

<img src="images/bitcrush.png"><br>

<div style="display:inline-block;margin-left:50px;">
reduce sample resolution and sample rate for lo-fi effects<br><br>
<b>crush</b>: sample resolution reduction<br>
                   
<b>downsamp</b>: sample rate reduction<br>
                   
<br><br><br><br></div>

<a name=butterworth></a><br>

### <b>butterworth</b>

<img src="images/butterworth.png"><br>

<div style="display:inline-block;margin-left:50px;">
filter using the butterworth formula<br><br>
<b>F</b>: frequency cutoff<br>
                   
<b>Q</b>: resonance<br>
                   
<br><br><br><br></div>

<a name=compressor></a><br>

### <b>compressor</b>

<img src="images/compressor.png"><br>

<div style="display:inline-block;margin-left:50px;">
try to keep volume at a certain level<br><br>
<b>attack</b>: speed to apply gain reduction<br>
                   
<b>lookahead</b>: how much time to "look ahead" to adjust the compression envelope. this necessarily introduces a delay into your output, which could be compensated for by running sequencers slightly early.<br>
                   
<b>mix</b>: amount of compression. lower this value for a "parallel compression" effect. you should use this mix slider instead of the effectchain's mix slider, to compensate for lookahead.<br>
                   
<b>output</b>: makeup gain, to increase volume<br>
                   
<b>ratio</b>: how much gain reduction to apply when the single passes the threshold<br>
                   
<b>release</b>: speed to remove gain reduction<br>
                   
<b>threshold</b>: threshold where gain should start to be reduced<br>
                   
<br><br><br><br></div>

<a name=dcremover></a><br>

### <b>dcremover</b>

<img src="images/dcremover.png"><br>

<div style="display:inline-block;margin-left:50px;">
high pass filter with a 10hz cutoff to remove DC offset, to keep signal from drifting away from zero<br><br>
<br><br><br><br></div>

<a name=delay></a><br>

### <b>delay</b>

<img src="images/delay.png"><br>

<div style="display:inline-block;margin-left:50px;">
echoing delay<br><br>
<b>amount</b>: amount of delay that returns<br>
                   
<b>delay</b>: delay in milliseconds<br>
                   
<b>dry</b>: should the dry signal pass through, or just the delayed signal?<br>
                   
<b>feedback</b>: should the output audio feed back into the delay?<br>
                   
<b>input</b>: should we accept input into the delay?<br>
                   
<b>interval</b>: sets delay length to a musical duration<br>
                   
<b>invert</b>: should the delayed audio have its signal inverted? this can give a different sound, and also cancel out DC offset to prevent it from accumulating with feedback.<br>
                   
<b>short</b>: shortcut to shrink the range of the delay slider, to allow for audible-rate delays and comb filter sounds<br>
                   
<br><br><br><br></div>

<a name=distortion></a><br>

### <b>distortion</b>

<img src="images/distortion.png"><br>

<div style="display:inline-block;margin-left:50px;">
waveshaping distortion<br><br>
<b>center input</b>: remove dc offset from input signal to distort in a more controlled way<br>
                   
<b>clip</b>: cutoff point of distortion, lower values result in more extreme distortion<br>
                   
<b>fuzz</b>: push input signal off-center to distort asymmetrically<br>
                   
<b>preamp</b>: signal gain before feeding into distortion<br>
                   
<b>type</b>: style of distortion to apply<br>
                   
<br><br><br><br></div>

<a name=freeverb></a><br>

### <b>freeverb</b>

<img src="images/freeverb.png"><br>

<div style="display:inline-block;margin-left:50px;">
reverb using the "freeverb" algorithm<br><br>
<b>damp</b>: high frequency attenuation; a value of zero means all frequencies decay at the same rate, while higher settings will result in a faster decay of the high frequency range<br>
                   
<b>dry</b>: amount of untouched signal<br>
                   
<b>room size</b>: controls the length of the reverb, a higher value means longer reverb<br>
                   
<b>wet</b>: amount of reverb signal<br>
                   
<b>width</b>: stereo width of reverb<br>
                   
<br><br><br><br></div>

<a name=gainstage></a><br>

### <b>gainstage</b>

<img src="images/gainstage.png"><br>

<div style="display:inline-block;margin-left:50px;">
control volume within an effectchain<br><br>
<b>gain</b>: volume multiplier<br>
                   
<br><br><br><br></div>

<a name=gate></a><br>

### <b>gate</b>

<img src="images/gate.png"><br>

<div style="display:inline-block;margin-left:50px;">
only allow signal in when it's above a certain threshold. useful to eliminate line noise, or just as an effect.<br><br>
<b>attack</b>: speed at which gate blends open<br>
                   
<b>release</b>: speed at which gate blends closed<br>
                   
<b>threshold</b>: volume threshold to open up the gate<br>
                   
<br><br><br><br></div>

<a name=granulator></a><br>

### <b>granulator</b>

<img src="images/granulator.png"><br>

<div style="display:inline-block;margin-left:50px;">
granulate live input<br><br>
<b>autocapture</b>: freeze input at this interval<br>
                   
<b>dry</b>: amount of dry signal to allow through<br>
                   
<b>frz</b>: freeze the current recorded buffer<br>
                   
<b>g oct</b>: should we add octaves and fifths?<br>
                   
<b>len ms</b>: length of each grain in milliseconds<br>
                   
<b>overlap</b>: number of overlapping grains<br>
                   
<b>pos</b>: playback position within the buffer<br>
                   
<b>pos r</b>: randomization of grain start point<br>
                   
<b>spa r</b>: randomization of time between grains<br>
                   
<b>spd r</b>: randomization of grain speed<br>
                   
<b>speed</b>: speed of grain playback<br>
                   
<b>width</b>: stereo width of grain placement<br>
                   
<br><br><br><br></div>

<a name=muter></a><br>

### <b>muter</b>

<img src="images/muter.png"><br>

<div style="display:inline-block;margin-left:50px;">
mute an incoming signal<br><br>
<b>ms</b>: ramp time to mute/unmute signal<br>
                   
<b>pass</b>: when true, the signal is allowed through<br>
                   
<br><br><br><br></div>

<a name=noisify></a><br>

### <b>noisify</b>

<img src="images/noisify.png"><br>

<div style="display:inline-block;margin-left:50px;">
multiply input signal by white noise<br><br>
<b>amount</b>: amount of noise to apply<br>
                   
<b>width</b>: how frequently a new noise sample should be chosen<br>
                   
<br><br><br><br></div>

<a name=pitchshift></a><br>

### <b>pitchshift</b>

<img src="images/pitchshift.png"><br>

<div style="display:inline-block;margin-left:50px;">
shifts a signal's pitch<br><br>
<b>ratio</b>: amount to pitchshift by (a value of 1 indicates no shift)<br>
                   
<b>ratioselector</b>: shortcuts to useful pitch ratios<br>
                   
<br><br><br><br></div>

<a name=pumper></a><br>

### <b>pumper</b>

<img src="images/pumper.png"><br>

<div style="display:inline-block;margin-left:50px;">
dip the volume of a signal rhythmically, to emulate a "pumping sidechain" effect<br><br>
<b>amount</b>: amount to lower volume<br>
                   
<b>attack</b>: how sharply the volume drops<br>
                   
<b>curve</b>: how the volume returns<br>
                   
<b>interval</b>: the rate to pump<br>
                   
<b>length</b>: length of pump<br>
                   
<br><br><br><br></div>

<a name=tremolo></a><br>

### <b>tremolo</b>

<img src="images/tremolo.png"><br>

<div style="display:inline-block;margin-left:50px;">
modulate signal's volume rhythmically<br><br>
<b>amount</b>: amount to lower volume<br>
                   
<b>duty</b>: pulse width of LFO<br>
                   
<b>interval</b>: speed of LFO<br>
                   
<b>offset</b>: offsets LFO phase<br>
                   
<b>osc</b>: LFO oscillator type<br>
                   
<br><br><br><br></div>

## other
         
<a name=comment></a><br>

### <b>comment</b>

<img src="images/comment.png"><br>

<div style="display:inline-block;margin-left:50px;">
a box to display some text, to explain a section of a patch<br><br>
<b>comment</b>: type text here<br>
                   
<br><br><br><br></div>

<a name=eventcanvas></a><br>

### <b>eventcanvas</b>

<img src="images/eventcanvas.png"><br>

<div style="display:inline-block;margin-left:50px;">
schedule values to set over time<br><br>
<b>canvas</b>: canvas of events. canvas controls:
-shift-click to add an event
-hold shift and drag an event to duplicate
-hold alt to drag an event without snapping
-hold ctrl while dragging to snap to an interval
-hold shift and scroll to zoom
-hold alt and grab empty space to move slide the canvas view
-hold ctrl and grab empty space to zoom the canvas view<br>
                   
<b>clear</b>: delete all elements<br>
                   
<b>delete</b>: delete highlighted elements<br>
                   
<b>drag mode</b>: direction that elements can be dragged<br>
                   
<b>interval</b>: grid for snapping events to<br>
                   
<b>measures</b>: length of loop<br>
                   
<b>quantize</b>: quantizes events to grid<br>
                   
<b>record</b>: record connected values as they change<br>
                   
<b>scrollh</b>: horizontal scrollbar<br>
                   
<b>timeline</b>: control loop points<br>
                   
<b>view rows</b>: number of visible rows<br>
                   
<br><br><br><br></div>

<a name=globalcontrols></a><br>

### <b>globalcontrols</b>

<img src="images/globalcontrols.png"><br>

<div style="display:inline-block;margin-left:50px;">
interface controls, intended to allow you to use midi controllers to navigate the canvas. controlling these sliders directly with the mouse is not recommended.<br><br>
<b>lissajous b</b>: amount of blue in background lissajous curve<br>
                   
<b>lissajous g</b>: amount of green in background lissajous curve<br>
                   
<b>lissajous r</b>: amount of red in background lissajous curve<br>
                   
<b>scroll x</b>: emulate horizontal mouse scrolling<br>
                   
<b>scroll y</b>: emulate vertical mouse scrolling<br>
                   
<b>x pos</b>: horizontal panning position<br>
                   
<b>y pos</b>: vertical panning position<br>
                   
<b>zoom</b>: zoom level<br>
                   
<br><br><br><br></div>

<a name=grid></a><br>

### <b>grid</b>

<img src="images/grid.png"><br>

<div style="display:inline-block;margin-left:50px;">
generic grid, to be used by "script" module, to assist in writing scripts that use grid-based midi controllers<br><br>
<b>grid</b>: patch a grid in here, from a "midicontroller" module<br>
                   
<b>momentary</b>: should clicks be treated as momentary inputs?<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=groupcontrol></a><br>

### <b>groupcontrol</b>

<img src="images/groupcontrol.png"><br>

<div style="display:inline-block;margin-left:50px;">
connect to several checkboxes, and control them all with one checkbox<br><br>
<b>group enabled</b>: controls the connected checkboxes<br>
                   
<br><br><br><br></div>

<a name=loopergranulator></a><br>

### <b>loopergranulator</b>

<img src="images/loopergranulator.png"><br>

<div style="display:inline-block;margin-left:50px;">
use with a "looper" module to play the contents with granular synthesis<br><br>
<b>freeze</b>: stop advancing looper time<br>
                   
<b>len ms</b>: length of each grain in milliseconds<br>
                   
<b>loop pos</b>: playback position within loop<br>
                   
<b>octaves</b>: should we add octaves and fifths?<br>
                   
<b>on</b>: use granular synthesis for looper playback<br>
                   
<b>overlap</b>: number of overlapping grains<br>
                   
<b>pos rand</b>: randomization of grain start point<br>
                   
<b>spacing rand</b>: randomization of time between grains<br>
                   
<b>speed</b>: speed of grain playback<br>
                   
<b>speed rand</b>: randomization of grain speed<br>
                   
<b>width</b>: stereo width of grain placement<br>
                   
<br><br><br><br></div>

<a name=multitrackrecorder></a><br>

### <b>multitrackrecorder</b>

<img src="images/multitrackrecorder.png"><br>

<div style="display:inline-block;margin-left:50px;">
record several synchronized tracks of audio, to write to disk for mixing in an external DAW<br><br>
<b>add track</b>: add an additional track<br>
                   
<b>bounce</b>: write the tracks to your recordings directory<br>
                   
<b>clear</b>: clear the audio in the tracks<br>
                   
<b>record</b>: record input to the tracks<br>
                   
<br><br><br><br></div>

<a name=oscoutput></a><br>

### <b>oscoutput</b>

<img src="images/oscoutput.png"><br>

<div style="display:inline-block;margin-left:50px;">
send OSC messages when slider values change or when notes are received<br><br>
<b>label*</b>: label to send slider value. the message will be sent in the format /bespoke/[label] [value]<br>
                   
<b>note out address</b>: label to send input notes. the message will be sent in the format /bespoke/[label] [pitch] [velocity]<br>
                   
<b>osc out address</b>: destination to send OSC messages to<br>
                   
<b>osc out port</b>: port to send OSC messages to<br>
                   
<b>slider*</b>: sends a value to the address. try patching a modulator into this, such as a leveltocv module to send audio levels.<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=prefab></a><br>

### <b>prefab</b>

<img src="images/prefab.png"><br>

<div style="display:inline-block;margin-left:50px;">
create a collection of modules that can be loaded from the "prefabs" menu. drag and drop modules onto here to add them to the prefab. drag the grey cable to any modules you want to remove from the prefab.<br><br>
<b>disband</b>: free all modules from this prefab<br>
                   
<b>load</b>: load a .pfb<br>
                   
<b>save</b>: save as a .pfb file<br>
                   
<br><br><br><br></div>

<a name=presets></a><br>

### <b>presets</b>

<img src="images/presets.png"><br>

<div style="display:inline-block;margin-left:50px;">
save and restore sets of values. connect the grey circle to modules to affect all controls on that module. connect the purple circle to a control to affect only that control. shift-click on the grid to store a preset to that square, and click on a grid square to load that preset.<br><br>
<b>blend ms</b>: time to blend preset values over<br>
                   
<b>preset</b>: jump to a preset<br>
                   
<br><br><br><br></div>

<a name=push2control></a><br>

### <b>push2control</b>

<img src="images/push2control.png"><br>

<div style="display:inline-block;margin-left:50px;">
use an ableton push 2 to control bespoke's interface<br><br>
<br><br><br><br></div>

<a name=radiosequencer></a><br>

### <b>radiosequencer</b>

<img src="images/radiosequencer.png"><br>

<div style="display:inline-block;margin-left:50px;">
sequence to only enable one value at a time. patch it to the "enabled" checkbox on several modules to only enable one module at a time. works well in conjunction with "groupcontrol" module.<br><br>
<b>grid</b>: patch a grid in here from a "midicontroller" module<br>
                   
<b>interval</b>: rate to advance<br>
                   
<b>length</b>: length of sequence<br>
                   
<br><br><br><br></div>

<a name=samplebrowser></a><br>

### <b>samplebrowser</b>

<img src="images/samplebrowser.png"><br>

<div style="display:inline-block;margin-left:50px;">
browse your system for samples. drag samples from here to your desired targets (sampleplayer, drumplayer, seaofgrain, etc)<br><br>
<b> < </b>: previous page<br>
                   
<b> > </b>: next page<br>
                   
<br><br><br><br></div>

<a name=scale></a><br>

### <b>scale</b>

<img src="images/scale.png"><br>

<div style="display:inline-block;margin-left:50px;">
controls the global scale used by various modules<br><br>
<b>intonation</b>: which method to use to tune the scale<br>
                   
<b>note</b>: the pitch that maps to the frequency defined in "tuning"<br>
                   
<b>root</b>: root note of the scale<br>
                   
<b>scale</b>: which set of notes to use<br>
                   
<b>tet</b>: how many semitones make up an octave<br>
                   
<b>tuning</b>: what frequency does the pitch defined in "note" represent?<br>
                   
<br><br><br><br></div>

<a name=script></a><br>

### <b>script</b>

<img src="images/script.png"><br>

<div style="display:inline-block;margin-left:50px;">
python scripting for livecoding notes and module control<br><br>
<b>?</b>: show scripting reference<br>
                   
<b>a</b>: variable for the script to use, can be modulation by other sources<br>
                   
<b>b</b>: variable for the script to use, can be modulation by other sources<br>
                   
<b>c</b>: variable for the script to use, can be modulation by other sources<br>
                   
<b>code</b>: write code here. press ctrl-R to execute the code, or ctrl-shift-R to just execute the current block.<br>
                   
<b>d</b>: variable for the script to use, can be modulation by other sources<br>
                   
<b>load</b>: load selected script<br>
                   
<b>loadscript</b>: choose a script from here, then press "load"<br>
                   
<b>run</b>: click here to execute the code, or press ctrl-R<br>
                   
<b>save as</b>: save the current script<br>
                   
<b>stop</b>: cancel any events scheduled by this script<br>
                   <br>accepts: <font color=yellow>pulses</font> <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=scriptstatus></a><br>

### <b>scriptstatus</b>

<img src="images/scriptstatus.png"><br>

<div style="display:inline-block;margin-left:50px;">
shows everything in the current python scope, for debugging<br><br>
<b>reset all</b>: resets scope variables<br>
                   
<br><br><br><br></div>

<a name=selector></a><br>

### <b>selector</b>

<img src="images/selector.png"><br>

<div style="display:inline-block;margin-left:50px;">
radio button control to only enable one value at a time. patch it to the "enabled" checkbox on several modules to only enable one module at a time. works well in conjunction with "groupcontrol" module.<br><br>
<b>selector</b>: which value should be set to 1<br>
                   <br>accepts: <font color=orange>notes</font> <br>
<br><br><br><br></div>

<a name=timerdisplay></a><br>

### <b>timerdisplay</b>

<img src="images/timerdisplay.png"><br>

<div style="display:inline-block;margin-left:50px;">
displays a timer to indicate how long a patch has been running<br><br>
<b>reset</b>: reset timer to zero<br>
                   
<br><br><br><br></div>

<a name=transport></a><br>

### <b>transport</b>

<img src="images/transport.png"><br>

<div style="display:inline-block;margin-left:50px;">
controls tempo and current time position<br><br>
<b> + </b>: increase tempo by one<br>
                   
<b> - </b>: decrease tempo by one<br>
                   
<b> < </b>: nudge current time backward<br>
                   
<b> > </b>: nudge current time forward<br>
                   
<b>reset</b>: reset timeline to zero<br>
                   
<b>swing</b>: where the halfway point of musical time within the swing interval should fall. a value of .5 represents no swing.<br>
                   
<b>swing interval</b>: interval over which to apply swing<br>
                   
<b>tempo</b>: global tempo, in beats per minute<br>
                   
<b>timesigbottom</b>: time signature bottom value<br>
                   
<b>timesigtop</b>: time signature top value<br>
                   
<br><br><br><br></div>

<a name=valuestream></a><br>

### <b>valuestream</b>

<img src="images/valuestream.png"><br>

<div style="display:inline-block;margin-left:50px;">
displays a control's value over time<br><br>
<b>speed</b>: how quickly display should scroll<br>
                   
<br><br><br><br></div>

<a name=vstplugin></a><br>

### <b>vstplugin</b>

<img src="images/vstplugin.png"><br>

<div style="display:inline-block;margin-left:50px;">
a VST plugin instance<br><br>
<b>open</b>: show the plugin window<br>
                   
<b>preset</b>: choose from saved VST presets<br>
                   
<b>program change</b>: send a program change message to the VST instance<br>
                   
<b>save as</b>: save the current VST settings as a preset to load again later<br>
                   
<b>show parameter</b>: select parameters to display them, so they can be adjusted from within bespoke's interface. if a VST has more than 20 parameters, this list will initially be empty. in that case, to make a parameter appear in this list, wiggle it within the VST's interface.<br>
                   
<b>vol</b>: adjust the output volume<br>
                   
<br><br><br><br></div>
