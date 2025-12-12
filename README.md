# Audio Classification with CNN and Hybrid QNN

This repository contains a Google Colab notebook for experimenting with
audio classification on the UrbanSound8K dataset using:

- a classical CNN model
- a hybrid CNN + Quantum Neural Network (QNN)

The notebook focuses on model architecture, training logic, and
classical–quantum integration rather than fast reproducibility.

## What’s inside
- Audio preprocessing (resampling, log-Mel spectrograms)
- Baseline CNN audio classifier
- Hybrid CNN–QNN model using PennyLane
- Training, validation, and checkpointing logic
- Support for resuming long training runs

## Notes
- Training can take a long time
- Model weights are not included
- The notebook is intended mainly for experimentation and personal reference

## Usage
Open the notebook in Google Colab and run the cells selectively.
