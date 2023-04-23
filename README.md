# CompuFart

CompuFart is a fart sound synthesizer that generates sound by physically modeling wind passing through an asshole. This version is programmed in [Cmajor](https://cmajor.dev/).

## How to Use

You can use the provided fart synthesizer in your DAW or with a handful of tools provided by Sound Stacks. Alternatively, you can use the physical model in your own Cmajor patch!

### Using the Provided Synthesizer

To use the CompuFart Synthesizer, you need to run the Cmajor patch `CompurFartSynth.cmajorpatch`. This can be done in a DAW or other audio plug-in host by loading the patch inside of Sound Stacks' patch-hosting [plug-in](https://cmajor.dev/docs/GettingStarted#loading-patches-in-your-daw-with-the-cmajor-vstau-plugin). You can also run patches in VScode with the [Cmajor VScode extension](https://cmajor.dev/docs/GettingStarted#using-cmajor-in-vscode), or use one of the other methods provided by Sound Stacks.

#### Synthesizer Controls

The CompuFart model works by applying pressure to an artifical sphincter that has some physical parameters that affect pitch and timbre. To easily play this model as an instrument, the provided synthesizer provides some controls in a typical MIDI-controlled monophonic digital instrument paradigm. (Note that the pitch of the model is not currently tuned.)

When no notes are pressed, any new Note On will trigger a pressure envelope and pitch envelope that should cause the model to oscillate with some transient variation provided by the envelopes. Any new Note Ons received while other notes are on will not re-trigger these envelopes, but it will cause a pitch glide/portamento with a time specified by the `Pitch Glide` parameter. 

Pressure may be further controlled via a mod wheel if the `Mod Wheel` parameter is turned on, with mod wheel values scaling the pressure applied by the envelope like an "envelope amount" parameter. This allows pressure to be arbitrarily automated or controlled with your DAW or a MIDI controller. To control pressure in this manner, you may wish to set the pressure envelope like an instantaneous gate, with the `Pressure Sustain` set to maximum and all pressure envelope times set to the minimum value. (Note that the `Strain` and `Strain Intensity` further modify the pressure.)

Similar to controlling pressure with the mod wheel, MIDI pitch bend may be used to arbitrarily automate or control pitch. The amount of pitch bend applied can be controlled with the `Pitch Bend Range` parameter. To only control pitch with pitch bend and not use the built-in pitch envelope, set the `Pitch Env Amount` to 0.

The timbre of farts may be controlled with the `Pinch`, `Cheek`, `Strain`, and `Strain Intensity` parameters. These parameters affect some physical variables in the model.

A simple reverb is provided with Toilet Bowl and Church Pew presets. You may also turn it off and use your own reverb. It is generally recommended to apply reverb or other post-processing to enrichen the sound.

### Building your own Fart Engine

The quickest way to use the physical model is to use the `processor` named `Terrance` (the phsyical model) along with the input and output interface `processor`s, `TerranceInputInterface` and `TerranceOutputInterface`. The interface `processor`s provide a quick way to get meaningful and useful parameters and audio into and out of the model. The model should oscillate when sufficient pressure is provided to the artificial sphincter.

The provided mono synth, `CompuFartSynth` shows one possible way to construct a digital instrument with the fart engine.

## Notes

* The model is not currently (pitch) tuned. However, using typical pitch control inputs (keyboard, bend) should provide relative pitch control.
* There is currently no guarantee of compatibility or consistency between different versions of the model, synth, or other patches and code. If you wish to preserve a particular sound, it is recommended that you record it and make note of the parameter values and the version and git commit SHA. Of course, you can also fork the code.

## How Does it Work

(Coming Soon)

