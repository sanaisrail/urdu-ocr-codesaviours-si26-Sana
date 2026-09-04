# Urdu OCR — Code Saviours SI-26

A fine-tuned TrOCR-based OCR model for extracting Urdu text from images.

## 1. Why This Project Matters

Optical Character Recognition (OCR) converts text from images into editable digital text.

Urdu OCR is challenging because Urdu is written from right to left, uses connected characters, contains complex ligatures, and has variations in fonts and writing styles.

Initial experiments with Tesseract OCR showed that it struggled to recognize Urdu text accurately. The output contained incorrect characters, missing words, incomplete sentences, and unreadable text.

This project explores a dedicated deep learning approach using a fine-tuned TrOCR model to improve Urdu text recognition from images.

Possible applications include digitizing Urdu books, newspapers, historical documents, educational material, and printed records.

## 2. How It Works

The project uses TrOCR, a transformer-based Optical Character Recognition model.

A pretrained TrOCR model was adapted for the Urdu OCR task through fine-tuning on a custom Urdu image-text dataset.

The basic workflow is:

1. The user uploads an image containing Urdu text.
2. The image is processed using the TrOCR processor.
3. The trained model analyzes the image.
4. The model predicts the Urdu text.
5. The predicted text is displayed in the application.

The dataset contains approximately 200 Urdu text images with variations in fonts, font sizes, backgrounds, image sizes, and text appearance.

## 3. Live Demo

### Hugging Face Space

The live demo allows users to upload an Urdu text image and view the text predicted by the OCR model.

[Open the Urdu OCR Live Demo](https://huggingface.co/spaces/sanaisrail/SI26-urdu-ocr-model)

### Hugging Face Model

[View the Trained Model](https://huggingface.co/sanaisrail/SI26-urdu-ocr-model)

## 4. Results

The final accuracy obtained during the Week 4 evaluation was 0.00%.

Although the result was low, the evaluation helped identify limitations of the current approach.

Possible reasons include:

- The dataset was relatively small, with approximately 200 images.
- Training and evaluation images may have been different.
- Urdu fonts and image styles varied.
- There was limited Urdu-specific training data.
- The model required further fine-tuning for Urdu text recognition.

The results showed that the current approach needs further improvement for reliable Urdu OCR.

Future improvements could include:

- Collecting a larger and better-labelled Urdu OCR dataset.
- Using an Urdu or multilingual pretrained OCR model.
- Adding more font and image variations.
- Improving image preprocessing.
- Performing more extensive fine-tuning.
- Evaluating the model using OCR-specific metrics such as Character Error Rate (CER) and Word Error Rate (WER).

## 5. How to Run Locally

### Step 1 — Clone the Repository

```bash
git clone https://github.com/sanaisrail/urdu-ocr-codesaviours-si26-Sana.git
cd urdu-ocr-codesaviours-si26-Sana
