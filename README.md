Object Detection System using YOLOv8
SDAIA Academy - Computer Vision Systems Development
1. Project Overview
This project delivers a complete Computer Vision Object Detection system powered by the Ultralytics YOLOv8 architecture. The main objective is to establish an end-to-end detection pipeline that accepts image inputs, accurately identifies target objects, localises them with bounding boxes, and provides classification confidence scores.
2. Problem Description
Object detection is a fundamental challenge in computer vision with critical real-world applications in autonomous driving, smart surveillance, and automated inspection systems. This project addresses this challenge by configuring, fine-tuning, and evaluating an object detection workflow from raw data input to inference visualisations.
3. Dataset & Model Used
 Selected Model: YOLOv8 Nano (⁠yolov8n.pt⁠) pre-trained weights.
 Dataset: COCO8 dataset (8 sample images covering multiple object classes).
 Input Resolution: 640x640 pixels.
 Training Cycles: 10 Epochs.
4. Workflow / Architecture
The detection pipeline follows a sequential structure:
[ Input Images / Data ] ──> [ Preprocessing & Resizing ] ──> [ YOLOv8 Backbone & Feature Extraction ] ──> [ Feature Pyramid Network (FPN) ] ──> [ Bounding Box & Class Confidence Predictions ]
Environment Setup: Installation of the ⁠ultralytics⁠ package, PyTorch, OpenCV, and Matplotlib.
2. Model Initialization: Loading pre-trained weights for transfer learning.
3. Training Execution: Training the model on specified data splits for 10 epochs.
4. Evaluation: Visualising loss trends, precision-recall metrics, and test sample inference outputs.
5. Results & Evaluation
 Quantitative Evaluation: Training and validation loss curves (Box Loss, Class Loss, DFL Loss) along with mAP@50 and mAP@50-95 metrics were computed and saved in ⁠runs/detect/train/results.png⁠.
 Qualitative Output: Prediction bounding boxes and confidence score overlays were verified via validation batches (⁠val_batch0_pred.jpg⁠).
 Performance Overview: The model demonstrated accurate spatial localization on test cases within 10 training cycles.
6. Deployment & Optimization
 Real-World Application: The pipeline can be deployed on edge devices or camera streams for automated monitoring systems.
 Optimization Potential: Model weights can be exported to ONNX or TensorRT formats and quantized (FP16/INT8) to achieve real-time inference speeds on low-power hardware.
7. Technologies Used
 Language: Python 3.10+
 Framework: PyTorch & Ultralytics YOLOv8
 Environment: Google Colab / Jupyter Notebook
 Libraries: OpenCV, Matplotlib, NumPy, Pillow
8. How to Run the Project
1. Open the provided ⁠.ipynb⁠ file in Google Colab or a local Jupyter Notebook environment.
2. Ensure GPU acceleration is enabled (⁠Runtime⁠ -> ⁠Change runtime type⁠ -> ⁠T4 GPU⁠ in Google Colab).
3. Execute all cells sequentially from top to bottom.
4. Generated metrics and visual predictions will be stored in the ⁠runs/detect/train/⁠ directory.
9. Future Improvements
 Expand model training onto custom annotated datasets using Roboflow.
 Increase epoch duration and tune hyperparameters for higher detection precision.
 Implement a Web UI interface (e.g., Gradio or Streamlit) for user interactive image/video uploads.
10. Submission Details
 Academy: SDAIA Academy (أكاديمية سدايا)
 Program: Computer Vision Systems Development
 Student Name: Abdullah Alsabhan
 GitHub Repository: YOLOv8 Object Detection Repository
