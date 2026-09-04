Urdu OCR Project | Code Saviours SI-26 | Sana

OCR (Optical Character Recognition) is a technology that converts text from images into editable digital text. Urdu OCR is more challenging than English OCR because Urdu is written from right to left, many letters change shape, and several characters look similar. Urdu OCR can be used to digitize old books and historical documents, as well as convert printed records into digital text for schools, businesses, and government offices.


Why We Need a Better Model

The results of Tesseract OCR on our Urdu dataset show that it struggles to recognize Urdu text accurately. Although image preprocessing improved the image quality, the OCR output still contained incorrect characters, missing words, incomplete sentences, and unreadable text. This is because Urdu is a cursive script with connected characters, complex ligatures, and different writing styles, making it difficult for a general-purpose OCR engine to handle.

These results demonstrate that Tesseract is not sufficient for accurate Urdu text recognition. Therefore, a dedicated OCR model trained specifically on Urdu text is required to achieve better accuracy and more reliable recognition.


 Urdu OCR:

Urdu OCR — A fine-tuned TrOCR model for extracting text from Urdu images.

 1. Project Title and Description

Urdu OCR is a deep learning project developed to recognize and extract Urdu text from images. The project uses TrOCR (Transformer-based Optical Character Recognition) and a Streamlit application to provide a simple interface for testing the model.

The project was developed by Sana Israil as part of the Code Saviours ML/AI Internship — Batch SI-26.

2. What Problem This Solves and Why It Matters

Recognizing Urdu text from images can be challenging because Urdu has connected characters, different writing styles, ligatures, and variations in fonts and image quality.

Many OCR systems are mainly designed for English and other widely supported languages. Because of this, they may not perform well when used directly on Urdu text.

This project explores the use of a fine-tuned TrOCR model for recognizing Urdu text from images.

One possible real-world use case is digitizing Urdu books, newspapers, historical documents, and educational material. An Urdu OCR system can convert these images into editable and searchable digital text.

 3. How It Works

OCR stands for Optical Character Recognition. It allows a computer to identify text from an image and convert it into digital text.

TrOCR is a transformer-based OCR model that takes an image as input and generates the corresponding text.

For this project, I used a pretrained TrOCR model and adapted it for the Urdu OCR task through fine-tuning.

Fine-tuning means taking an already trained model and training it further on data related to a specific task. In this case, the model was trained using a custom dataset containing Urdu text images.

The basic workflow is:

1. The user uploads an image containing Urdu text.
2. The image is processed using the TrOCR processor.
3. The trained model analyzes the image.
4. The model predicts the text.
5. The predicted Urdu text is displayed in the application.

The dataset contains approximately 200 Urdu text images. The images include different fonts, font sizes, backgrounds, and image dimensions.

4. Live Demo

Hugging Face Space:

The live demo allows users to upload an Urdu text image and view the text predicted by the OCR model.

Hugging Face Model:
https://huggingface.co/spaces/sanaisrail/SI26-urdu-ocr-model


 5. How to Run It Locally

Step 1 — Clone the Repository

git clone https://github.com/sanaisrail/urdu-ocr-codesaviours-si26-Sana.git

 Step 2 — Install Dependencies

Install the required libraries using:

pip install -r requirements.txt

The main libraries used in this project are:

 Python
 PyTorch
 Hugging Face Transformers
 TrOCR
 Streamlit
 Pillow
 Torchvision
 SentencePiece

Step 3 — Run the Application

Start the Streamlit application using:

streamlit run app.py

After running the application, open the local URL shown in the terminal.

Upload an image containing Urdu text and click the "Extract Urdu Text" button to see the predicted text.


6. Dataset Details

The dataset contains approximately 200 Urdu text images.

The project includes `dataset.csv` and `label_corrected.csv`, which were used for preparing the image-text pairs for model training.


The images were collected from online sources and Google searches and prepared for the Urdu OCR task.

The dataset contains different types of Urdu text and includes variations in:

 Fonts
 Font sizes
 Backgrounds
 Image sizes
 Text appearance

The purpose of using different types of images was to expose the model to different visual forms of Urdu text.

Dataset details:

| Detail | Description |
|---|---|
| Total Images | 200 |
| Language | Urdu |
| Image Type | Text images |
| Source | Internet / Google |
| Fonts | Different Urdu fonts |
| Font Sizes | Different sizes |
| Backgrounds | Different backgrounds |
| Image Sizes | Different image dimensions |
| Task | Urdu Optical Character Recognition |


7. Results

The final accuracy obtained during the Week 4 evaluation was 0.00%.

The result was low, but it helped identify some limitations of the current approach.

One possible reason is that the original TrOCR checkpoint used in the project was mainly designed for printed English text rather than Urdu. Urdu has a different writing system, connected characters, and different visual patterns.

Other possible reasons include:

 The dataset was relatively small, with approximately 200 images.
 Training and evaluation images may have been different.
 Urdu fonts and image styles varied.
 There was limited Urdu-specific training data.
 The model required more fine-tuning for the Urdu language.

The results showed that the current approach needs further improvement for reliable Urdu text recognition.

With more time, I would improve the project by collecting a larger and better-labelled Urdu OCR dataset, using an Urdu or multilingual pretrained OCR model, adding more font and image variations, improving image preprocessing, and performing more extensive fine-tuning.

I would also use OCR-specific evaluation metrics such as Character Error Rate (CER) and Word Error Rate (WER) to better evaluate the model's performance.


8. Credit

Sana 

Built during the Code Saviours ML/AI Internship — Batch SI-26.
