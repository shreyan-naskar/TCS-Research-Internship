# TCS Research Internship

Research and implementation work completed as part of a TCS Research Internship focused on sign-language recognition and supporting video-processing workflows.

## Repository Structure

| Path                  | Description                                                                                     |
| --------------------- | ----------------------------------------------------------------------------------------------- |
| `literature-survey/`  | Literature review material related to sign-language recognition research                        |
| `video-segmentation/` | Notebook-based pipeline for preparing sign-language video clips through OCR-guided segmentation |

## Literature Survey

The `literature-survey/` directory contains:

| File                            | Description                                                                                                                        |
| ------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| `SLR.pdf`                       | Internal survey presentation on sign-language recognition topics                                                                   |
| `papers/s10209-024-01133-y.pdf` | Research paper on the impact of face swapping and data augmentation on sign-language recognition                                   |
| `papers/sensors-26-00524.pdf`   | Research paper on pose-based static sign-language recognition using deep learning for Turkish, Arabic, and American Sign Languages |

This material supports background study of data augmentation, pose-based recognition, and recent sign-language recognition approaches.

## Video Segmentation

The `video-segmentation/` directory contains a preprocessing workflow for sign-language videos. The main notebook scans each source video with OCR, detects the first frame containing the word `EXPLANATION`, and saves only the frames before that title card.

### Contents

| Path                     | Description                                    |
| ------------------------ | ---------------------------------------------- |
| `segment-SL-video.ipynb` | Main notebook for OCR-based video segmentation |
| `req.txt`                | Python dependencies required by the notebook   |
| `DATA/`                  | Input videos used by the notebook              |
| `SEGMENTED/`             | Output videos generated after segmentation     |

### Workflow

For each supported video in `DATA/`, the notebook:

1. Reads frames sequentially with OpenCV.
2. Preprocesses frames for OCR using grayscale conversion, optional upscaling, blur, and thresholding.
3. Uses RapidOCR to identify text in each frame.
4. Finds the first frame containing the normalized target word `EXPLANATION`.
5. Writes all preceding frames to a matching file in `SEGMENTED/`.

Supported input formats are `.mp4`, `.mov`, `.avi`, `.mkv`, and `.webm`.

## Setup

Install the dependencies for the video-segmentation workflow from inside the repository root:

```bash
pip install -r video-segmentation/req.txt
```

## Running the Video Segmentation Notebook

1. Place source videos in `video-segmentation/DATA/`.
2. Open `video-segmentation/segment-SL-video.ipynb`.
3. Run the notebook cells from top to bottom.
4. Review generated clips in `video-segmentation/SEGMENTED/`.

The notebook exposes configurable constants for the OCR target word, scan interval, and fallback behavior when the target word is not found.
