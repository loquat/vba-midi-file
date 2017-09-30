# vba-midi
A set of classes, functions, and methods for reading and writing MIDI files from Excel written in VBA.

A Factory module is provided for the creation of most MIDI related objects. Most MIDI objects are immutable.

To parse a MIDI file, call the Midi.ParseMidiFile function which will return a collection of tracks each containing MetaEvent, ChannelEvent, or SystemExclusiveEvent objects. Valid MIDI files are assumed.

Creating a MIDI file is left to the implementor to ensure validity and requires the creation of a TrackCollection object of TrackChunks. The TrackCollection is then passed to the Factory.CreateStandardMidiFile function to create a StandardMidiFile object.
StandardMidiFile objects contain a Write method which will write the object to disk as a MIDI file when invoked.

The examples.bas module currently provides an example of usage for the Midi.ParseMidiFile function, called ExampleReadMidiFileIntoDataStructure.
