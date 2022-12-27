# markov-poly-chain

This project is a polyphonic sequence generator based on Markov chains written in [Purr Data](https://puredata.info/downloads/purr-data), a flavor of Miller Puckette's Pd. The workflow is explained in the Pd files through comments, but here is a brief explanation:

## Workflow

With a chosen monophonic MIDI file, the program stores all note pairs (a note and its subsequent note) and creates a transition matrix using the probabilities of the next note given a current note. There are four voices to the polyphonic sequence generator, and each voice is a separate markov chain. However each voice uses the same transition matrix. Sequences undergo a transition on a global metronome frequency that can be modified. There are also options to reset any voice at any time and add semitone offsets for each voice to create custom voicings.
