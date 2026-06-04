# Video Segmentation

Notebook-based preprocessing workflow for sign-language videos. The pipeline scans each source video with OCR, detects the first frame containing the target title word `EXPLANATION`, and saves only the frames before that title card.

## Contents

| Path                     | Description                                    |
| ------------------------ | ---------------------------------------------- |
| `segment-SL-video.ipynb` | Main notebook for OCR-based video segmentation |
| `req.txt`                | Python dependencies required by the notebook   |
| `DATA/`                  | Input videos used by the notebook              |
| `SEGMENTED/`             | Output videos generated after segmentation     |

## Setup

From the repository root, install the notebook dependencies:

```bash
pip install -r video-segmentation/req.txt
```

The dependency file includes OpenCV, RapidOCR with ONNX Runtime, tqdm, and NumPy.

## Workflow

For each supported source video in `DATA/`, the notebook:

1. Reads frames sequentially with OpenCV.
2. Preprocesses frames for OCR using grayscale conversion, optional upscaling, blur, and thresholding.
3. Uses RapidOCR to identify text in each frame.
4. Finds the first frame containing the normalized target word `EXPLANATION`.
5. Writes all preceding frames to a matching video file in `SEGMENTED/`.

Supported input formats are `.mp4`, `.mov`, `.avi`, `.mkv`, and `.webm`.

## Running

1. Place source videos in `DATA/`.
2. Open `segment-SL-video.ipynb`.
3. Run the notebook cells from top to bottom.
4. Review generated clips in `SEGMENTED/`.

The notebook exposes configurable constants for the OCR target word, scan interval, and fallback behavior when the target word is not found.
