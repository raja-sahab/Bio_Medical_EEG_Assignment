# EEG Data Analysis using EEGLAB
This repository contains the code and instructions for EEG data analysis using EEGLAB. The data used in this analysis is not included in the repository and needs to be downloaded separately.

## Requirements
MATLAB
EEGLAB toolbox

## Installation
* Clone this repository to your local machine.
* Download the EEG data (.set and .fdt) files from Teams and save them to the cloned repository.
* Open MATLAB and add the path to the EEGLAB toolbox.
* Launch EEGLAB by typing eeglab in the MATLAB command window.

## Data Analysis
* Load the EEG data (.set) in EEGLAB using the GUI.
* Perform the following preprocessing steps using the GUI:
** Downsampling to 250 Hz: Tools -> Change Sampling Rate -> 250Hz
** Filtering [1-80Hz] + Notch filter 50 Hz: Tools -> Filter the data -> Basic FIR filter -> Set high and low values (here: 1-80)
** Epoching with time locking event type: G interval: [-1 3]: Tools -> Extract Epochs
* Visual inspection for channels and epochs: Channel Data (scroll)
** Remove bad epochs from the plot: Tools -> Reject Continuous Data by Eye
** Select bad channels and remove them using the GUI
* Run Independent Component Analyses (ICA) using the GUI.
** Tools -> ICA decompose data by ICA (it takes a while)
** Plot -> Component maps -> 2D
* Manually check the components and mark the “bad” ones. Reject Data using ICA -> Reject Components by Map. 
