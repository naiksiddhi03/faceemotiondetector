# Face-Emotion-Recognition-Deep-Learning
  
## Problem Statement 

 Digital classrooms are conducted via video telephony software program where it’s not possible for medium scale class (25-50) to see all students and access the mood. Because of this drawback, students are not focusing on content due to a lack of surveillance. While digital platforms have limitations in terms of physical surveillance but it comes with the power of data and machines which can work for you. It provides data in the form of video, audio, and texts which can be analyzed using deep learning algorithms. Deep learning backed system not only solves the surveillance issue, but it also removes the human bias from the system, and all information is no longer in the teacher’s brain rather translated in numbers that can be analyzed and tracked.

We will solve the above-mentioned challenge by applying deep learning algorithms to live video data.The solution to this problem is by recognizing facial emotions.
## Dataset Information

we have defined the image size to 48 so each image will be reduced to a size of 48x48. Each image corresponds to a facial expression in one of seven categories (0=Angry, 1=Disgust, 2=Fear, 3=Happy, 4=Sad, 5=Surprise, 6=Neutral). The dataset contains approximately 36K images.

Dataset link - [www.kaggle.com/jonathanoheix/face-expression-recognition-dataset](https://www.kaggle.com/jonathanoheix/face-expression-recognition-dataset)

## Emotion detection Recognition using deep learning (Streamlit frontend)

In this repository we have created front-end using Streamlit for webapp and used streamlit-webrtc which helped to deal with real-time video streams. Image captured from the webcam is sent to VideoTransformer function to detect the emotion. 

Then this model was deployed on heroku platform with the help of buildpack-apt which is necessary to deploy opencv model on heroku. But heroku platform only allows model size as 500 mb. And tensorflow 2.0 itself takes 420 mb so we replaced it with tensorflow-cpu. All the other packages used and their version can be found in requirements.txt 

## Dependencies

- Python
- Tensorflow
- Keras
- Opencv
- Streamlit
- Streamlit-Webrtc

## Run WebApp Locally
Open Anaconda Prompt &
Go to the project directory
```bash
  cd Face-Emotion-Recognition-Using-Streamlit
```

Install dependencies

```bash
  pip install -r requirement.txt
```

Start local webcam

```bash
  streamlit run app.py
```
