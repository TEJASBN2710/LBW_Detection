# 🏏 LBW Detection Using Computer Vision

This project is a computer vision-based system that simulates **LBW (Leg Before Wicket) detection** in cricket.  
It analyzes a cricket video, tracks the ball trajectory, detects the batsman and pitch, and predicts whether the ball would hit the stumps (LBW decision).

---

## ✨ Features
- ✅ Real-time **ball tracking** using HSV color detection  
- ✅ **Batsman detection** using RGB thresholding + Canny edge detection  
- ✅ **Pitch mapping** with LBW zone marking  
- ✅ **Trajectory prediction** to check if the ball hits the stumps  
- ✅ Works on cricket video input (`lbw.mp4`)  

---

## 📂 Project Structure
```
lbw-detection/
│── main.py             # Main pipeline for LBW detection
│── ball_detect.py      # Handles ball detection & tracking
│── batsman.py          # Detects batsman using tuned RGB & Canny thresholds
│── pitch.py            # Defines pitch & LBW zone
│── lbw.mp4             # Sample cricket video
│── requirements.txt    # Project dependencies
```

---

## ⚙️ Workflow
1. **Pitch Detection (`pitch.py`)**  
   - Defines the pitch area and LBW valid zone  
   - Marks the stumps and wicket region  

2. **Batsman Detection (`batsman.py`)**  
   - Detects the batsman silhouette using RGB thresholds  
   - Uses edge detection to refine boundaries  

3. **Ball Detection (`ball_detect.py`)**  
   - Tracks the cricket ball using HSV color ranges  
   - Stores ball trajectory frame by frame  

4. **LBW Decision Logic (`main.py`)**  
   - Reads video frames from `lbw.mp4`  
   - Detects ball + batsman + pitch  
   - Predicts if the ball would hit the stumps  
   - Outputs: **"LBW OUT"** ⚠️ or **"NOT OUT"** ✅  

---

## ▶️ Usage
```bash
# Run the main script
python main.py
```

- The script will open the sample cricket video (`lbw.mp4`)  
- It will show ball trajectory, batsman position, and pitch zone  
- LBW result will be displayed on the video window  

---

## 🚀 Technologies Used
- **Python**  
- **OpenCV** → Image & video processing  
- **cvzone** → Color detection utilities  
- **NumPy** → Trajectory calculations  

---

## 📌 Future Improvements
- Train a **machine learning model** for more robust ball tracking  
- Add **3D trajectory prediction** like Hawk-Eye  
- Support **real-time live camera feed** for on-ground LBW detection  
- Improve batsman detection with **pose estimation (MediaPipe / OpenPose)**  

---

## 🙌 Acknowledgements
This project was built for educational purposes to demonstrate how computer vision can be applied in sports analytics, specifically cricket LBW detection.

---

📸 Inspired by **Hawk-Eye technology** used in professional cricket.
