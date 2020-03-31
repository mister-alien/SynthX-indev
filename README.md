# SynthX-indev
## Purpose:
This repository will serve as the staging area for a new polyphonic analog modelling synth intended for DIY Embedded Systems.
It should enable synths of a variety of tiers to be created and configured, from "slapped onto an arduino" to custom-designed Reference design board. As a design goal, we will eventually provide refence implementation for a HW synth, let's call it the recommended setup, and the budget-concious Arduino implementation. Anything in between may require the imagination.
The core will be a configurable portable architecture, capable of being compiled on various grades of hardware. Currently considered for this are:  
* AVR8 / Arduino hardware
* STM32

Would we consider any other hardware? Well, yes, maybe this portable architecture concept is garbage and I'll lock myself into a single platform early on but that is a goal!

## SynthSpecs (Desired)
This is a list of what is aimed to be implemented. When stable work is started this will be converted to a checklist..
* Basic Waveform generator to be used for LFO & Audio Oscillator
* Envelope Generator, ADSR
* Noise Generator
* 12 / 24dB Filters, LP, HF, BP, ?
* MIDI
* Effects..
* Sequencer

## HW Details
There are currently a lot of unresolved design decisions to be made regarding architecture. Since the code is to be written in a portable fashion, anything that is platform specific should be modular and interface with the synthesizer core in a standardized manner.
* RTOS or not ? 
* Desired sampling rate (44.1kHz ideal... programmable  ?)
* Support for external DAC modules
