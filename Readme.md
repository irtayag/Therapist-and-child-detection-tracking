**Therapist and Child Tracking Using YOLOv8 and DeepSORT**

This project performs real-time person detection and tracking using the YOLOv8 model for object detection and DeepSORT for tracking. The system is designed to track individuals in a video and annotate them with unique IDs, useful for applications such as monitoring and analyzing behavior in Autism Spectrum Disorder (ASD) therapy sessions.

\#\# Prerequisites

\- Python 3.x  
\- A video file for processing (e.g., \`Group Therapy for Autism Spectrum Disorder.mp4\`)  
\- Necessary Python libraries (see instructions below)

\#\# Setup Instructions

1\. \*\*Clone or Download the Project\*\*    
   Clone this repository or download and extract the project files.

2\. \*\*Install Dependencies\*\*    
   Install the required Python libraries by running:  
     
   \`\`\`bash  
   pip install \-r requirements.txt

3\. Download YOLOv8 Model Weights  
Download the YOLOv8 model weights (`yolov8n.pt`). You can obtain them from the YOLOv8 repository or use the `ultralytics` package to download them:  
python  
`from ultralytics import YOLO`  
`model=YOLO('yolov8n.pt')`

Ensure the weights file is located where the script can access it.

4.Prepare Your Video  
Place your video file (e.g., `Group Therapy for Autism Spectrum Disorder.mp4`) in the `/content/videos/` directory. If your video is located elsewhere, modify the video path in the script:  
python  
`cap=cv2.VideoCapture('/path/to/your/video.mp4')`

## **Running the Script**

To run the person detection and tracking, execute the following command:

\`\`\`bash  
python inference.py

### **Script Description**

* **Object Detection**: Uses YOLOv8 to detect persons in the video.  
* **Tracking**: Applies DeepSORT to track detected persons and assign unique IDs.  
* **Output**: Saves annotated frames with bounding boxes and unique IDs to an output video file.

## **Code Overview**

The `inference.py` script processes videos as follows:

1. **Initialize Models**: YOLOv8 for object detection and DeepSORT for tracking.  
2. **Process Video**: Reads the video frame by frame, performs object detection, updates tracking information, and draws bounding boxes with unique IDs.  
3. **Save Output**: Writes annotated frames to an output video file.  
 


