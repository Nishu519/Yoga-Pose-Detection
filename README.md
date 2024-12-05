# Yoga Pose Detection and Correction with AI

## Project Overview  
This project is an AI-powered system that provides **real-time feedback** for yoga poses using a webcam. It leverages **MediaPipe** for efficient pose estimation and gives feedback on joint alignment, helping users correct their posture dynamically and accurately.

## Features  
- **Real-Time Pose Detection**: Uses a webcam to analyze body movements.  
- **Dynamic Feedback**: Provides personalized feedback based on joint angles and predefined thresholds.  
- **Lightweight & Efficient**: MediaPipe ensures fast and accurate detection on most devices.  
- **Configurable**: Easily modify poses and their ideal angles for custom feedback.

## Technologies Used  
- **MediaPipe**: For pose estimation and landmark detection.  
- **OpenCV**: For video capture and display.  
- **NumPy**: For calculating angles between joints.

## Architectural diagram
![Unable to load image](Architectural%20diagram.png)

## Installation Instructions  

1. **Clone the Repository**:  
   ```bash
   git clone <repository-url>
   cd YogaPoseCorrector

2. **Install Dependencies**  
Make sure you have Python 3 installed, then run:  

```bash
pip install -r requirements.txt
```

3. **Run the Program**  

```bash
python mainFile.py
```


## **How to Use**  
1. Connect a webcam to your system.  
2. Run the program using the command mentioned above.  
3. Perform yoga poses in front of the camera.  
4. The system will analyze your pose in real-time and display corrective feedback on the screen.



## **Configuration**  
You can modify the `feedback_config` dictionary in `mainFile.py` to adjust:  
- **Joint names**  
- **Target angles for correction**  
- **Tolerance levels for feedback**  

## Example Configuration:  
```python
feedback_config = {
    'Left Elbow': ([mp_pose.PoseLandmark.LEFT_SHOULDER.value,
                    mp_pose.PoseLandmark.LEFT_ELBOW.value,
                    mp_pose.PoseLandmark.LEFT_WRIST.value], 
                   160, 10)  # Target angle: 160 degrees, Tolerance: ±10 degrees
}
```



## **Future Improvements**  
- Adding more yoga poses with detailed feedback.  
- Implementing voice feedback for hands-free interaction.  
- Integrating a graphical user interface (GUI) for enhanced user experience.  



## **Contributing**  
Contributions are welcome! Feel free to open issues or submit pull requests for new features, bug fixes, or improvements.  




