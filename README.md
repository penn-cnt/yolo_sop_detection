# Detecting Seizure Onset Patterns as Temporal Objects

**A Generalizable YOLO-Based Framework for iEEG Time Series Event Detection**

> **Status: Work in Progress — Manuscript in Preparation**
> Code, data, and model weights will be released upon publication.

---

## Overview

This project adapts the YOLO (You Only Look Once) object detection framework from computer vision to one-dimensional intracranial EEG (iEEG) time series. The goal is automated, high-throughput, multi-class detection of seizure onset patterns (SOPs) directly from raw iEEG recordings — treating EEG pattern events as temporal objects with onset, offset, and class label.

## Motivation

Seizure onset patterns are clinically significant biomarkers in the evaluation of drug-resistant epilepsy patients undergoing surgical workup:

- They help localize the seizure onset zone (SOZ)
- Specific patterns (e.g., low-voltage fast activity) are associated with favorable surgical outcomes
- Manual annotation by experts is time-consuming and does not scale to large datasets

Existing automated approaches struggle with the variability inherent in SOPs: events span vastly different time scales (sub-second to tens of seconds) and fall into multiple distinct pattern classes.

## Approach

We reformulate EEG pattern detection as a **temporal object detection** problem. A 1D implementation of the YOLO architecture processes multi-channel iEEG signals and simultaneously predicts temporal bounding boxes and class labels for multiple pattern types.

The model follows the standard YOLO pipeline adapted to the temporal domain:

| Component | Role |
|-----------|------|
| Backbone | Feature extraction from 1D iEEG signal |
| Neck (FPN/PAN) | Multi-scale feature fusion |
| Head | Temporal bounding box regression + class prediction |

![Model Architecture](Artboard%201model.png)

Expert-annotated iEEG recordings serve as ground truth, produced via a dedicated seizure annotation interface.

## Author

Zhongchuan Xu, Carlos A. Aguila, Odile Feys, Dan Zhou, Honda Wu, William K.S. Ojemann,  Nishant Sinha,  Erin C. Conrad, Brian Litt

## Citation

*Preprint and paper link to be added upon publication.*

## Contact

For inquiries about this work, please reach out via GitHub Issues once the repository is fully public.
