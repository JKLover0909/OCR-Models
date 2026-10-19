# CLAUDE.md

## Overview
Benchmark comparing three OCR engines — Tesseract (`pytesseract`), PaddleOCR and EasyOCR — on speed and accuracy using a sample image.

## Layout
- `Compare.ipynb` — side-by-side comparison of all three engines (timing + output).
- `tesseract/testTesseract.ipynb`, `PaddleOCR/testPaddleOCR.ipynb`, `EasyOCR/testEasyOCR.ipynb` — per-engine test notebooks.
- `Data/2.jpg` — sample test image.

## Commands
- Install: `pip install pytesseract paddleocr paddlepaddle easyocr pillow matplotlib opencv-python` (Tesseract binary must be installed separately).
- Run: `jupyter notebook Compare.ipynb`

## Rules
- Notebooks contain machine-specific absolute paths (e.g. an `R:\...` image path); use paths relative to the repo (`Data/2.jpg`) when editing.
- Do not commit downloaded model weights or caches (`.EasyOCR/`, `.paddleocr/`, gitignored).
- Keep the test image set in `Data/` unchanged so timings stay comparable.
