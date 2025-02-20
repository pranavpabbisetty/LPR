# License Plate Recognition (LPR) with YOLO  

## Overview  
This project implements a License Plate Recognition (LPR) system using YOLO for object detection and EasyOCR for text extraction. The system detects vehicles, extracts license plate numbers, and tracks them across video frames. The results are stored in a CSV file and visualized with bounding boxes.  

## Features  
- **Vehicle Detection**: Uses YOLOv8 to detect cars and track them across frames.  
- **License Plate Detection**: Identifies license plates using a custom YOLO model.  
- **OCR Processing**: Extracts text from detected license plates using EasyOCR.  
- **Data Storage**: Saves detection results in a CSV file.  
- **Visualization**: Draws bounding boxes on video frames to highlight detected vehicles and license plates.  

## Installation  
1. Clone this repository:  
   ```sh
   git clone https://github.com/your-username/lpr-yolo.git
   cd lpr-yolo
   ```  
2. Install dependencies:  
   ```sh
   pip install -r requirements.txt
   ```  
3. Download and place the YOLO models:  
   - `yolov8n.pt` (pre-trained COCO model)  
   - `license_plate_detector.pt` (custom license plate detection model)  

## File Structure  
- `main.py`: Runs the LPR pipeline (vehicle detection, tracking, license plate recognition).  
- `util.py`: Helper functions for OCR, formatting, and result saving.  
- `visualize.py`: Creates a visualization of detected license plates in the video.  

## Usage  
1. Place the input video file as `sample.mp4` in the project directory.  
2. Run the main detection script:  
   ```sh
   python main.py
   ```  
   This generates `test.csv` with detected license plates.  
3. To visualize results:  
   ```sh
   python visualize.py
   ```  
   This outputs an annotated video `out.mp4`.  

## Output  
- A CSV file (`test.csv`) with detected vehicle and license plate data.  
- A processed video (`out.mp4`) with bounding boxes around detected cars and license plates.  

## Dependencies  
- Python  
- OpenCV  
- YOLOv8 (Ultralytics)  
- EasyOCR  
- NumPy  
- Pandas  

## Future Improvements  
- Improve OCR accuracy with more training data.  
- Enhance tracking with additional filtering techniques.  
- Implement real-time processing capabilities.  

