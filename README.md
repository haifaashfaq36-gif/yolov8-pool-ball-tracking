### 5. Project Documentation (README.md)
```markdown
# 🎱 Billiard Ball Tracking & Collision Detection

A self-contained Computer Vision pipeline designed to track pool balls and detect collisions in video feeds using YOLOv8 and geometric spatial analysis.

## 🚀 Project Overview
This project automates the detection of 'impact events' between billiard balls. It handles everything from raw video ingestion to the production of a frame-annotated technical demonstration.

## 🛠️ Technical Stack
*   **Language:** Python 3.x
*   **Model:** YOLOv8s (Ultralytics)
*   **Inference:** COCO Class 32 (Sports Ball)
*   **Video Engineering:** FFmpeg (Codec Normalization H.264/YUV420p)
*   **Image Processing:** OpenCV (Computer Vision)

## 🧠 Key Features
1.  **Normalization Pipeline:** Uses FFmpeg to ensure input videos are compatible with OpenCV's capture properties regardless of original codec.
2.  **Adaptive Thresholding:** Collision detection is not hard-coded. The system calculates a dynamic threshold based on 1.15x the average diameter of the tracked objects to account for camera perspective and scale.
3.  **Temporal Cooldown State Machine:** Implemented a 15-frame cooldown timer to prevent 'double-counting' of a single collision event.
4.  **Automated Logging:** Real-time terminal logs for every detected event with corresponding frame indices.

## 📊 Results
*   **Video Length:** 501 Frames
*   **Target:** 2-Ball Pool Game
*   **Accuracy:** Successfully detected 1 collision at Frame 415.
*   **Output:** `final_submission.mp4` with visual overlays (Bounding Boxes, Centroids, and Collision Banners).

## 📥 How to Use
1. Install dependencies: `pip install ultralytics yt-dlp opencv-python`
2. Update the `VIDEO_URL` in the script.
3. Run the pipeline to generate the `final_submission.mp4` file.
```

