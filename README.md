# YOLOv8 to TensorFlow.js

A small script that converts a pretrained YOLOv8 object detection model into the TensorFlow.js format, so the model can run in a browser.

## What is in this repo

| File | Purpose |
|---|---|
| `yolov8n.pt` | Pretrained YOLOv8 nano model weights |
| `convert.py` | Loads `yolov8n.pt` with Ultralytics and exports it with `model.export(format="tfjs", dynamic=True)` |

This repo contains only the conversion step. It has no web app code.

## Run

```bash
pip install ultralytics
python convert.py
```

The export creates a TensorFlow.js model folder that you can load with `@tensorflow/tfjs` in a web page.
