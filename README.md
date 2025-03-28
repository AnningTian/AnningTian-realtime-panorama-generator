# realtime-panorama-generator

A real-time panorama generation tool using OpenCV and SIFT.  
This project allows you to capture a sequence of frames from your webcam and stitch them together into a panoramic image.

---

## 📸 Features

- Capture frames from a live camera feed
- Stitch multiple frames into a panorama using **SIFT** + **homography**
- Automatic cropping for cleaner results
- Interactive keyboard control
- Real-time FPS display
- Save the resulting panorama as a JPG image

---

## 🛠 Requirements

- Python 3.6+
- OpenCV (`cv2`)
- NumPy

Install dependencies:

```bash
pip install opencv-python numpy
```

---

## 🚀 How to Run

```bash
python panorama_generator.py
```

Make sure your webcam is connected and accessible.

---

## 🎮 Controls

| Key | Action                   |
|-----|--------------------------|
| `s` | Start capturing frames   |
| `a` | Stop capturing & stitch  |
| `q` | Exit (in some versions)  |

---

## 🧠 How It Works

1. The script captures frames at fixed time intervals after pressing `s`.
2. Press `a` to stop capturing. Then the stitching process begins:
   - Detect SIFT keypoints and descriptors.
   - Match features using Brute-Force matcher.
   - Estimate homography via RANSAC.
   - Warp and blend the images together.
3. The result is cropped and saved as `panorama.jpg`.

---

## 🗂 Project Structure

```
.
├── panorama_generator.py     # Main script
├── panorama.jpg              # Output image (after running)
├── README.md
```

---

## 💡 To Do / Ideas

- Add support for image files instead of live camera
- Add ORB / SURF as alternate feature extractors
- Allow manual selection of capture regions
- Real-time preview stitching

---

Made with 🧠 + 📷 using OpenCV.
