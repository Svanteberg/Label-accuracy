# Modeling the effect of human accuracy on accuracy of neural networks

## Introduction

Categories in the medical sciences usually have some degree of uncertainty. This means that labeled data used for supervised training of neural network have an uncertainty with respect to what the categories are and the labeling. There usually are both an inter- and intrarater variability, so the labeling will vary from expert to expert, but each expert will also have some degree of individual labeling variability.

With the accuracy as performance measure for neural networks, it is impossible to discover inaccurate labeling and paradoxically this will cause a lowered accuracy that actually reflect a superior performance by the neural network compared to the human experts that have labeled the data.

Here this phenomenon is demonstrated and it is shown that the networks are robust to relatively high degree of mislabeled training data. This means that when dealing with data were the categories are fuzzy sets, accuracies below 100 percent may represent new knowledge or human error and alternative ways of evaluating the results must be used (a low accuracy may of course also mean that the network performs poorly).

Two different data sets are used for the demonstration. The first is the well known MNIST data set consisting of images of handwritten digits, 0 - 9, a categorization most would not question. The second is an arbitrary categorization with four categories of single channel EEG data.

### Modeling accuracy

In contrast to the real case, theoretically or using a data set with certain categories and labeling, it can be tested to artificially induce mislabeling and evaluate the effect with both mislabeled and correctly labeled data. This will give two accuracies, an apparent and a true accuracy. The first is the accuracy when testing with mislabeled data, this is the accuracy that is seen in the real case. The second, is the accuracy when testing with correctly labeled data and it is usually unmeasurable and hidden in the real case.

For instance, if 10 percent of the data is mislabeled and the neural network still correctly learns the categories, the apparent accuracy would be 90 percent but the true accuracy would be 100 percent.

<p align="center">
<img src="https://github.com/Svanteberg/Label-accuracy/blob/master/images/ideal model 0-10.png" width="40%">
</p>

## Materials & methods

### MNIST

(LeCun et al., Proceedings of the IEEE 1998, 86(11):2278-2324)

### EEG data

Data from the published data base created at the Temple University Hospital, Philadelphia (Obeid & Picone, Frontiers of neuroscience 2016, 10:1-5), was used. One single EEG channel of data from three different subjects were used. The sampling frequency was 256 Hz, the duration of extracted data per folder was 20 minutes and the signals were from the F8, A2 and T6 electrode for the respective folder. These contained a periodic discharge (PDI), a cardiac artefact (CA) and a periodic discharge (PDII), respectively. The signals were assessed visually and annotated which resulted in 1106, 1335 and 1133 potentials for the respective signal.

<p align="center">
<img src="https://github.com/Svanteberg/Label-accuracy/blob/master/images/examples of eeg categories.png" width="75%">
</p>

Four categories were defined: 1) periodic discharge I, 2) cardiac artefact, 3) periodic discharge II and 4) data free of 1 – 3.

Each example was 0.5 s, or 128 samples, in duration.

## Results

### MNIST

<p align="center">
<img src="https://github.com/Svanteberg/Label-accuracy/blob/master/images/mnist 0-10.png" width="75%">
</p>

### EEG data

<p align="center">
<img src="https://github.com/Svanteberg/Label-accuracy/blob/master/images/eeg_2-4.png" width="75%">
</p>
