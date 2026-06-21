# Imagined speech EEG dataset — long words condition (Nguyen et al. 2017)

## Overview

This dataset comprises EEG recordings from 6 healthy participants performing imagined speech tasks involving two conditions: cooperate and independent word imagery. The study employed a motor imagery paradigm with auditory and visual cues, yielding 3,600 preprocessed trials (1,800 per class) recorded at 256 Hz from 64 channels. Data were analyzed using Riemannian manifold methods and relevance vector machines for brain-computer interface applications, achieving mean classification accuracy of 66.2±4.8%.

## Dataset Summary

| Property | Value |
|---|---|
| Subjects | 6 |
| Channels | 64 |
| Classes | 2 |
| Trial length | 5 s |
| Sampling frequency | 256 Hz |
| Sessions | 1 |
| Total trials | 1200 |
| Paradigm | MotorImagery |

## Data Collection Methods

EEG data were acquired using a BrainProducts ActiCHamp system at 256 Hz sampling rate from 64 channels (60 EEG, 4 EOG) using standard 10-20 montage. Participants performed imagined speech tasks cued by auditory beeps (5 beeps at 1.4s rhythm) and visual cues. Preprocessing included bandpass filtering (8-70 Hz, 5th order Butterworth), 60 Hz notch filtering, and adaptive EOG artifact removal. Each 5-second trial was split into 3 overlapping 2-second epochs.

## How to Access via MOABB

Install MOABB and load this dataset directly:

```python
from moabb.datasets import Nguyen2017_L
from moabb.paradigms import MotorImagery
paradigm = MotorImagery()

dataset = Nguyen2017_L()
X, y, metadata = paradigm.get_data(dataset)
```

For more details see the [MOABB documentation](https://moabb.neurotechx.com/) and the
[MOABB dataset page](https://moabb.neurotechx.com/docs/generated/moabb.datasets.Nguyen2017_L.html).

## Citation

If you use this dataset please cite the primary publication:

> DOI: [10.1088/1741-2552/aa8235](https://doi.org/10.1088/1741-2552/aa8235)

## NEMAR / MOABB Benchmark Collection

This BIDS-formatted dataset was converted from the original data using the
[MOABB](https://moabb.neurotechx.com/) pipeline and re-hosted on
[NEMAR](https://nemar.org/) as part of the MOABB benchmark collection.
The original data and license terms apply — see `dataset_description.json` for details.
