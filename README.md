Adapted from https://github.com/wxs/subjective-functions

# Added features:
option -w allows to set weights for each individual layer/octave pair (in increasing layer order, then octave)
option -si allows to load seed image from file

README from original authors :

# Subjective functions
## Multi-scale neural texture synthesis

By using a Gaussian pyramid and extracting Gatys-style "style" descriptors
using the Gramian of intermediate VGG layers for each spatial scale in the
pyramid, we can create much higher-resolution images, with structure at
multiple image scales, not necessarily aligned with the receptive field of the
layers of Gatys.
More information at [the research page](http://wxs.ca/research/multiscale-neural-synthesis/).

## Quickstart

Install the pre-requisites

    pip3 install -r requirements.txt

Run locally (this will likely be very slow as it runs on your GPU)

    KERAS_BACKEND=tensorflow python3 synthesize.py -s bark.jpg

Look for output files inside the "outputs" directory that will be created by this command.

## Configuration

Most immediately useful flags:

    -s - Path to source texture image
    --output-width, --output-height, output dimensions in pixels


To see all the other flags run

    python3 synthesize.py -h
