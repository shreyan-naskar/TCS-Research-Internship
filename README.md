# TCS Research Internship

Research and implementation work completed as part of a TCS Research Internship focused on sign-language recognition and supporting video-processing workflows.

## Repository Structure

| Path                  | Description                                                                                     |
| --------------------- | ----------------------------------------------------------------------------------------------- |
| `ISLR/`               | Notebook work for Indian Sign Language Recognition experiments                                  |
| `literature-survey/`  | Literature review material related to sign-language recognition and sequence-modeling research  |
| `video-segmentation/` | Notebook-based pipeline for preparing sign-language video clips through OCR-guided segmentation |

## ISLR

The `ISLR/` directory contains:

| File         | Description                                                        |
| ------------ | ------------------------------------------------------------------ |
| `main.ipynb` | Main notebook for Indian Sign Language Recognition experimentation |
| `README.md`  | Local documentation for the ISLR notebook workflow                 |

## Literature Survey

The `literature-survey/` directory contains:

| File                            | Description                                                                                                                        |
| ------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| `SLR.pdf`                       | Internal survey presentation on sign-language recognition topics                                                                   |
| `SSM, MAMBA, VMamba.pdf`        | Notes or survey material covering state-space models, Mamba, and VMamba                                                            |
| `papers/s10209-024-01133-y.pdf` | Research paper on the impact of face swapping and data augmentation on sign-language recognition                                   |
| `papers/sensors-26-00524.pdf`   | Research paper on pose-based static sign-language recognition using deep learning for Turkish, Arabic, and American Sign Languages |

This material supports background study of data augmentation, pose-based recognition, sequence modeling, and recent sign-language recognition approaches.

## Video Segmentation

The `video-segmentation/` directory contains a preprocessing workflow for sign-language videos. The main notebook scans each source video with OCR, detects the first frame containing the word `EXPLANATION`, and saves only the frames before that title card.

### Contents

| Path                     | Description                                    |
| ------------------------ | ---------------------------------------------- |
| `segment-SL-video.ipynb` | Main notebook for OCR-based video segmentation |
| `req.txt`                | Python dependencies required by the notebook   |
| `DATA/`                  | Input videos used by the notebook              |
| `SEGMENTED/`             | Output videos generated after segmentation     |
| `README.md`              | Local documentation for the segmentation flow  |
