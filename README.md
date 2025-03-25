# 📷 CamSpector

An advanced **CCTV-based Automatic Theft Detector** and **Vehicle Crash Detector** system that leverages real-time video analysis to enhance security and safety. CamSpector provides a user-friendly interface for monitoring, detecting, and alerting suspicious activities and crash events.

---
## 🎥 Demo Video

[Watch the Demo](SAMPLE.mp4)


## 🚀 Features

- 📊 **Automatic Theft Detection**: Identifies suspicious activities using YOLOv5 object detection and CNN binary classification.
- 🚗 **Vehicle Crash Detection**: Detects vehicle collisions and triggers alerts in real-time.
- 📹 **Real-time Monitoring**: Live feed visualization with detection overlays.
- 🔔 **Alert System**: Sends automated emails to police using SMTP upon detection.
- 📸 **Frame Extraction**: Captures and saves CCTV frames for further analysis.
- 📈 **Event Logging**: Records detected events with timestamps for review.
- 🖥️ **User-Friendly UI**: Intuitive graphical interface for police to monitor and manage feeds.

---

## 🛠️ Tech Stack

- **Programming Language**: Python (YOLOv5, OpenCV, Tkinter)
- **Object Detection**: YOLOv5 for real-time detection of theft and crashes
- **CNN Classification**: Binary classification for event verification
- **UI Framework**: Tkinter for building a responsive and simple user interface
- **Email Service**: SMTP protocol for alerting authorities

---

## 📋 Prerequisites

Ensure you have the following installed:

- Python 3.x
- OpenCV (`pip install opencv-python`)
- YOLOv5 dependencies (`pip install torch torchvision matplotlib`)
- Tkinter (Comes pre-installed with Python)

---

## 📦 Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/hanish9193/CamSpector.git
    cd CamSpector
    ```

2. Install required packages:

    ```bash
    pip install -r requirements.txt
    ```

3. Set up YOLOv5:

    ```bash
    git clone https://github.com/ultralytics/yolov5.git
    cd yolov5
    pip install -r requirements.txt
    ```

4. Run the application:

    ```bash
    python main.py
    ```

---

## 📊 How It Works

1. **Theft Detection**:
   - YOLOv5 identifies objects in the CCTV feed.
   - CNN binary classifier verifies potential theft.
   - Alerts are sent via SMTP if theft is detected.

2. **Crash Detection**:
   - Detects sudden changes in vehicle motion patterns.
   - Logs the event and sends an alert to authorities.

3. **Frame Extraction**:
   - Captures frames from the CCTV feed.
   - Saves frames for offline analysis and review.

4. **User Interface**:
   - Provides live monitoring with event overlays.
   - Allows police to manage and track incidents.

---

## 📸 Frame Extraction Code

Here's a snippet to extract and save frames from the CCTV feed:

```python
import cv2

def extract_frames(video_path, output_folder):
    cap = cv2.VideoCapture(video_path)
    frame_count = 0

    while cap.isOpened():
        ret, frame = cap.read()
        if not ret:
            break

        frame_path = f"{output_folder}/frame_{frame_count}.jpg"
        cv2.imwrite(frame_path, frame)
        frame_count += 1

    cap.release()

extract_frames('cctv_feed.mp4', 'output_frames')
```

---

## 📷 UI Preview

![CamSpector UI Screenshot](assets/ui_preview.png)

---

## 🤝 Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m "Added new feature"`).
4. Push to the branch (`git push origin feature-name`).
5. Open a pull request.

---

## 📄 License

This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.

---

## 📞 Contact

For queries or collaboration, feel free to reach out via:

- **GitHub**: [hanish9193](https://github.com/hanish9193)
- **Email**: hanish.kumar9193@gmail.com
---

🔒 **CamSpector – Securing Spaces, Saving Lives.**

