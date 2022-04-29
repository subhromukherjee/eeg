# EEG
EEG data from hands movement
This repository contains the code for emotion recognition using wavelet transform and svm classifiers' rbf kernel.

Abstract:
This paper aims to propose hand movement prediction using electroencephalography (EEG) techniques.​ ​An electroencephalogram (EEG) is a machine that detects electrical activity in a human brain using small metal discs (electrodes) attached to the scalp. The brain cells communicate via electrical impulses and are active all the time, even when we are asleep. This activity shows up as wavy lines on an EEG recording.

About Dataset
Acquisition Data:
For the capture of brain impulses, an EMOTIV EPOC + 14 Channel electroencephalogram from EMOTIV was used. This equipment has 128 Hz sampling frequency with 16-bit analog analog converter with 14 electrode channels: AF3, F7, F3, FC5, T7, P7, O1, O2, P8, T8, FC6, F4, F8 and AF4.

For the purpose of controlling the virtual object, a twenty five minute data collection protocol was created with different cycles that address different situations while the user tries to control the object. Different situations have been proposed as part of the protocol so that the machine learning component can generalize brainwave behavior with respect to object control commands regardless of the situation.

During each of the acquisition cycles, the participant was exposed to the images depicting voluntary motor actions, namely: a right arrow that would represent motor action in the right direction, a left arrow that would represent motor action from the left direction and a circle that would represent no motor action. ̃

The only exception is the situation in which the participant is with his eyes closed, where a beep is given to the participant to open the eye only at specific times to view the images.

Pre-processing:
The data collected in the different situations mentioned above need to be pre-processed for later use in the machine learning component. For to better understand pre-processing, both the data source and the format and characteristics are discussed below.

The 128-Hz, 14-channel EEG equipment provides a 16-bit 128x14 matrix at each reading. As the brainwaves of interest are in the range of 0 to 30 Hz (Table 1), this information collected is passed by the Fast Fourier Transform (FFT) algorithm in the frequency range 0 to 30 Hz. , resulting in a 30x14 matrix in the frequency domain.

After the transformation of the data collected for the frequency domain, the weighted and arithmetic mean of each wave was performed, so that the resulting matrix has the dimensions 14x4x2. Thus, each instant of data collected is represented by the weighted and arithmetic mean for each of the 14 device channels and the 4 wave classifications.
Kaggle dataset link : https://www.kaggle.com/datasets/fabriciotorquato/eeg-data-from-hands-movement
