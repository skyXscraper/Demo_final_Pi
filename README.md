rtracker_ocr.py              full pipeline: Hailo detect + IoU track + OCR (--roi added)
detector.py                  module: HailoDetector (.hef) + TextOnlyDetector fallback
ocr.py                       module: PP-OCR recognizer + ply/range format check
ocr_paddle_video.py          OCR only (RapidOCR CPU, no Hailo, no tracking)
bin_light_controller.py      ESP32 relay/LED over UART — imported by ocr_paddle_video.py
models/rolls.hef             roll/ply/range detection on Hailo-8L
models/ppocr_rec.onnx        required by ocr.py (charset is in the ONNX metadata, no dict file)
models/ppocr_det.onnx        only for the no-Hailo text-only mode (--model models/ppocr_det.onnx)
requirements.txt             keeps the apt/pip install line for rebuilds
