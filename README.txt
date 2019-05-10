      ~~~~~~~~~~~~~~~~~~%                           %~~~~~~~~~~~~~~~~~~
                   -----%           TINY.pd         %-----
                     ---%                           %---
                      ==%                           %==
                        *%                         %*


TINY is an 8 voice-per-oscillator, dual oscillator digital
synthesizer, equipped with an additional noise oscillator,
a bypass-able lo-pass filter, hi-pass filter, and reverb.


******************************************************************************



Requirements:

Pure Data <https://puredata.info/downloads/pure-data>
freeverb <https://puredata.info/downloads/freeverb>




******************************************************************************



Usage:

the file TINY.pd is the parent patch which contains the rest of the modules.

Usage for each module
###
midi in: pretty self explanatory, handles midi in from the pure data module
   ~notein for up to 8 notes at a time corresponding with the 8 independent voices
   in each oscillator
###
oscillator: takes midi input and produces a pitch equivalent to that note in
   either a sin, square, saw, or triangle wave.
on/off - turns on/off the oscillator
sin/square/saw/triangle - switches between wave types
a/d/s/r - each respective slider adjusts the attack, decay, sustain, and release
   for reach voice
duration - multiplies the length of the sound scaling the adsr envelope
oct - adds / subtracts octaves from the pitch of the voices
semi - adds /subtracts semitones from the pitch of the voices
cent - adds / subtracts cents from pitch of the voices (1/100 semitone)
tone spread - each of the 8 independent voices in each oscillator has 8
   dependent voices of its own. this adjusts the spread of the pitch of the
   dependent voices around the central pitch of equivalent of the midi note
   taken as input.
spread strength - scales the spread of the sound
###
white noise: noise oscillator that produces white noise. some improvements
to this module would be to scale the noise with an adsr envelope.
on/off - turns on/off the oscillator
level - adjust the volume of the noise
###
lowpass filter
bypass - X indicates the filter is bypassed
LP - frequency slider
###
hi-pass filter
bypass - X indicates the filter is bypassed
HP - frequency slider
###
reverb: a GUI wrapper for the ~freeverb module
bypass- X indicates the reverb is bypassed
size - reverb room size
damp - dampening
width - stereo spreading
dry / wet - mixes dry and wet signal. slider all the way down = dry, all the
   way up = wet.
freeze - X indicates reverb freeze mode is on
###
master volume: master volume slider ###






contributing:
please feel free to download and use this instrument for any purpose. any
contributions to the project are also very welcome.
some improvements and expansions I have planned for whenever I have the time
 * patch save function
 * a/d/s/r for noise oscillator
 * a better GUI lol
 






©2019 spencer saxey /////////// <me@spencersaxey.com>
