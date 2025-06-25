# YogaVision: Yoga Pose Classification System
This project uses MediaPipe Pose for pose estimation and an MLP Classifier to recognize different yoga poses from videos. The system processes video files, extracts 3D body keypoints (x, y, z), trains a classifier, and visualizes predictions with annotated video output.

📁 Folder Structure
bash
Copy
Edit
/content/
├── 1.mp4 ... 20.mp4        # Training videos (named 1.mp4 to 20.mp4)
├── test_video.mp4          # Test video for classification
├── annotated_output.mp4    # Output video with visualizations
└── yoga_pose_classifier.ipynb
🧠 Poses Supported
Each video is mapped to one of the following yoga poses:

Video Range	Pose Name
1-4	Cobra
5-8	Lotus
9-12	Mountain
13-16	Triangle
17-20	Tree

⚙️ Features
✅ Extracts 33 body landmarks per frame
✅ Filters invalid (NaN/Inf) frames
✅ Scales features using StandardScaler
✅ Trains an MLPClassifier (with fallback to simpler model)
✅ Supports uploading and classifying test videos
✅ Annotates videos with predicted pose and confidence
✅ Generates plots for prediction summary and confidence

🚀 How to Use
Upload Training Videos
Upload videos named 1.mp4, 2.mp4, ..., 20.mp4 to /content/ (e.g., via Colab's sidebar or files.upload()).

Run the Notebook
Execute all cells. It will:

Extract keypoints

Train an MLP model

Prompt you to upload a test video

Upload Test Video
Upload a new .mp4 file when prompted. The system will:

Extract test video features

Predict the yoga pose per frame

Annotate and display the result

📊 Outputs
Training logs with data stats and accuracy

Predicted pose summary

Annotated video displaying predicted label & confidence

Plots:

Pose distribution histogram

Frame-wise confidence line plot

🧰 Dependencies
All required libraries are available in Google Colab:

mediapipe

opencv-python

numpy

matplotlib

sklearn

tqdm

IPython.display
