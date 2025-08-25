# EV_2025
**Video OCR with EasyOCR**

This repository contains a Python script in a Google Colab notebook (easyocr.ipynb) for performing Optical Character Recognition (OCR) on video files. The script is specifically designed to detect and extract numerical data, such as a two-digit speed, from video frames using the EasyOCR and OpenCV libraries.

**Key Features**

Video Processing: The notebook uses the cv2 (OpenCV) library to read an input video file (scene11_front.mp4) and processes it frame by frame to identify and analyze text.

Text Recognition: It employs the easyocr library, with language set to English, to efficiently perform text recognition on each video frame.

Targeted Text Extraction: The script contains a specific logic to identify the text "SPEED" using a fuzzy matching function (is_similar) and then locates the closest two-digit number to the detected "SPEED" text.

Output Generation: The process generates two outputs:

Annotated Video: A new video file named output_video.mp4 is created, with the detected speed number and its bounding box highlighted on the corresponding frames.

JSON Data: A JSON file (bounding_boxes.json) is saved, containing detailed information for each frame where a number was detected. This includes the frame index, the recognized text, the confidence score of the recognition, and the bounding box coordinates.

**Dependencies**

The notebook requires the installation of the following Python libraries, which are set up in the initial cells:

easyocr

opencv-python

ultralytics (Although it's commented out in the imports, the installation is included in a separate cell)

**How to Use**

Open the Notebook: Launch the easyocr.ipynb file in a Google Colab environment.

Upload the Video File: Ensure your video file is named scene11_front.mp4 and upload it to the Colab instance. The script is configured to look for this specific filename.

Run All Cells: Execute the notebook cells in sequential order. This will handle the installation of dependencies, load the video, perform the OCR and analysis, and generate the output files.

Review Outputs: After execution, the output_video.mp4 and bounding_boxes.json files will be saved in your Colab environment, ready for download.
