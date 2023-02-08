# Facial Expression Recognition with Keras

### This project was developed by building and training a convolutional neural network (CNN) in Keras to recognize facial expressions of seven categories (0=Angry, 1=Disgust, 2=Fear, 3=Happy, 4=Sad, 5=Surprise, 6=Neutral).

<br>

### The final result is a flask application that allows serve the trained model predictions and perform real-time facial expression recognition on video and image data, using OpenCV to automatically detect faces in images and draw bounding boxes around them. 

<br>

##### *This project is based on a Snehan Kekre course.*

<br>
<br>

## Run locally

1. Install:
```
    Flask==2.2.2
    opencv-python==4.7.0.68
    tensorflow==2.11.0
    numpy==1.24.1
```
2. Dowload the
[model_weights.h5](https://drive.google.com/file/d/12rpqlFi58FJMxs8swqiAELrzL6Rr_aoz/view?usp=sharing "download here")
file and add to the root directory of the project.

3. Add the path of your video in the `__init__` method of the class `VideoCamera` in the file camera.py

```python
    class VideoCamera(object):
        def __init__(self):
            self.video = cv2.VideoCapture("<add_your_video_here>")
``` 

4. Run Flask
```
    flask --app main run
```
- also with:
```
    python main.py
```