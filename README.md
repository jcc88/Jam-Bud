# JamBuddy
Applying Machine Learning to music creation with the help of Google's Magenta. JamBuddy aims to take Magenta from a proof-of-concept to a more tangible and useful tool. For now, we focus on doing a demo of Magenta interacting and engaging with the musician.   

## Requirements for demo
Logic Pro X, a synth/controller and a CPU/GPU.

## Installation
Set up the [Magenta Development Environment](https://github.com/tensorflow/magenta). 
We are using the ['call and response'](https://github.com/tensorflow/magenta/tree/master/magenta/interfaces/midi) interface. And once all dependencies are correctly installed. We can begin jamming.


## Demo
Make sure the environment in Logic Pro X is set up correctly. Now open a terminal, and from the magenta workspace you can enter the following script:

bazel run //magenta/interfaces/midi:magenta_midi -- magenta_midi \
--input_port="IAC Driver IAC Bus 2"   \
--output_port="IAC Driver IAC Bus 4" \
--passthrough=false \
--qpm=90 \
--allow_overlap=true \
--enable_metronome=true \
--log=DEBUG  \
--bundle_files=/path/to/drum_kit_rnn.mag  \
--playback_offset=-0.035 

## Training


## Tweaking the interface
