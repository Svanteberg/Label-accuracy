# Modeling the effect of label accuracy on prediction accuracy of neural networks

## Introduction

Categories in the medical sciences usually have some degree of uncertainty. This means that labeled data used for supervised training of neural network have an uncertainty with respect to what the categories are and the labeling. With the accuracy as performance measure, it is impossible to discover inaccurate labeling and paradoxically this will cause a lowered accuracy that actually reflect a superior performance by the neural network compared to human experts.

Here this phenomenon is demonstrated and it is shown that the networks are robust to relatively high degree of mislabeled training data. This means that when dealing with data were the categories are fuzzy sets, accuracies < 100 % may represent new knowledge and alternative ways of evaluating the results must be used (a low accuracy may of course also mean that the network performs poorly).

Two different data sets are used for the demonstration. The first is the well known MNIST data set consisting of images of handwritten digits, 0 - 9, a categorization most would not question. The second is an arbitrary categorization of four categories of single channel EEG data.

### Modeling accuracy

<p align="center">
<img src="https://github.com/Svanteberg/Label-accuracy/blob/master/images/ideal model 0-10.png" width="40%">
</p>

## Materials & methods

### MNIST

(LeCun et al., Proceedings of the IEEE 1998, 86(11):2278-2324)

### EEG data

Data from the published data base created at the Temple University Hospital, Philadelphia (Obeid & Picone, Frontiers of neuroscience 2016, 10:1-5), was used. One single EEG channel of data from three different folders were used. The sampling frequency was 256 Hz, the duration of extracted data per folder was 20 minutes and the signals were from the F8, A2 and T6 electrode for the respective folder. These contained a periodic discharge (PDI), a cardiac artefact (CA) and a periodic discharge (PDII), respectively. The signals were assessed visually and annotated which resulted in 1106, 1335 and 1133 potentials for the respective signal.

<p align="center">
<img src="https://github.com/Svanteberg/Label-accuracy/blob/master/images/examples of eeg categories.png" width="75%">
</p>

Four categories were defined: 1) periodic discharge I, 2) cardiac artefact, 3) periodic discharge II and 4) data free of 1 – 3.

## Results

### MNIST

<p align="center">
<img src="https://github.com/Svanteberg/Label-accuracy/blob/master/images/mnist 0-10.png" width="75%">
</p>

### EEG data

<p align="center">
<img src="https://github.com/Svanteberg/Label-accuracy/blob/master/images/eeg_2-4.png" width="75%">
</p>
