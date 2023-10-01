# Music Generator - TensorFlow Keras LSTM
Welcome to the Music Generator, a neural network powered by TensorFlow and Keras that specializes in MIDI file processing, audio classification, time series analysis, and music generation. This sophisticated tool employs Long Short-Term Memory (LSTM) networks to analyze MIDI files, interpret notes (including chords), durations, and offsets, and subsequently generate new MIDI compositions based on these musical elements. These tasks are achieved through an elaborate training process, where the model learns to categorize and understand various notes, chords, durations, and offsets found in input MIDI files.

## Purpose
This project originated from a collaboration with a friend who frequently arranges music for a cappella groups. The primary objective was to assist her in exploring new musical possibilities by inputting her arrangements and assessing the unique compositions this model could generate. Our training dataset comprises 41 of her MIDI-based arrangements, condensed into a single track to simplify chord grouping. After 100 epochs of training, we achieved remarkable results, reducing the total loss from an initial 10.8136 to an impressive 0.9185. This overall loss can be further broken down into the following components:
- Notes/Chords Loss: 0.5928
- Offset Loss: 0.1223
- Duration Loss: 0.2034

## Usage
This Music Generator can be executed in two primary modes: training with your own MIDI files or generating music using pre-trained weights and data. The specific configuration for each mode is detailed in the "Input Variables" section at the top of the MusicGeneratorFinal.ipynb file.

### Definitions
- Note: single pitch
- Chord: multiple pitches at once (will be used interchangeably with note throughout)
- Offset: time between one note/chord and the next
- Duration: length of note/chord

## How to Run
Before proceeding, make the necessary adjustments only in the "Input Variables" section of the code:
1. Update "folder_midi" to specify the folder location containing your MIDI files for analysis.
2. Set "num_notes_to_generate" to indicate the number of notes you wish to generate in your new composition.
3. Specify "file_midi_output" and "folder_midi_output" to determine the location and filename for the generated MIDI output.
4. Set "pretrained" to either True or False depending on whether you have previously trained the model. Refer to the subsequent sections for guidance on configuring your choice.

### Training
If you intend to use this tool with new MIDI files to explore your own musical creations, follow these steps:
1. Adjust "folder_data" and "folder_weights" to specify the locations where you want to save your data and weights files.
2. Modify "num_epochs" to specify the desired number of training epochs. Keep in mind that longer training times may be required for higher accuracy. Running with GPUs is recommended for acceleration.

### Pre-Trained
If you have already trained the model and wish to generate new MIDIs without retraining, proceed as follows:
1. Update "file_notes," "file_durations," and "file_offsets" with the file paths to your notes, durations, and offsets files.
2. Specify "file_weights" with the file path to your pre-trained weights file in HDF5 format. It is recommended to use the weights file with the lowest loss for the best results.

After configuring the above settings, execute the code to generate your new MIDI composition. Please exercise caution when specifying file locations, as existing files will be overwritten during the process. Also, any write folder locations not already existing should be created in the section after Input Variables.
