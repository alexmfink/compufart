# CompuFart

CompuFart is a fart sound synthesizer that generates sound by physically modeling wind passing through an asshole. This version is programmed in [Cmajor](https://cmajor.dev/).

## How to Use

You can use the provided fart synthesizer in your DAW or with a handful of tools provide by Sound Stacks. Alternatively, you can use the physical model in your own Cmajor patch!

### Using the Provided Synthesizer

To use the CompuFart Synthesizer, you need to run the Cmajor patch `CompurFartSynth.cmajorpatch`. This can be done in a DAW or other audio plug-in host by loading the patch inside of Sound Stacks' patch-hosting [plug-in](https://cmajor.dev/docs/GettingStarted#loading-patches-in-your-daw-with-the-cmajor-vstau-plugin). You can also run patches in VScode with the [Cmajor VScode extension](https://cmajor.dev/docs/GettingStarted#using-cmajor-in-vscode), or use one of the other methods provided by Sound Stacks.

### Building your own Fart Engine

The quickest way to use the physical model is to use the `processor` named `Terrance` (the phsyical model) along with the input and output interface `processor`s, `TerranceInputInterface` and `TerranceOutputInterface`. The interface `processor`s provide a quick way to get meaningful and useful parameters and audio into and out of the model. The model should oscillate when sufficient pressure is provided to the artificial sphincter.

The provided mono synth, `CompuFartSynth` shows one possible way to construct a digital instrument with the fart engine.

## How Does it Work

coming soon

