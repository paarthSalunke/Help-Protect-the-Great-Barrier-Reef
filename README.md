# Help-Protect-the-Great-Barrier-Reef
Detect crown-of-thorns starfish in underwater image data
---

Help Protect the Great Barrier Reef
Detect crown-of-thorns starfish in underwater image data
https://www.kaggle.com/soumya9977/learning-to-sea-underwater-img-enhancement-edaProblem Statement - Help Protect the Great Barrier Reef 
Australia's stunningly beautiful Great Barrier Reef is the world's largest coral reef and home to 1,500 species of fish, 400 species of corals, 130 species of sharks, rays, and a massive variety of other sea life. Unfortunately, the reef is under threat, in part because of the overpopulation of one particular starfish - the coral-eating crown-of-thorns starfish (or COTS for short).The outbreak of the COTS is one of the greatest threats to the great barrier reef , together We need to take action because if you don't…. then the great barrier reef won't be so great!
FACTOS 7 !⚽⭐🌊
With the help of scientist tourism operators and Queensland University of technology is developing a robot that can identify and inject COTS autonomously. We need to develop object detection model which can identify COTS in live video footage so the robot can identify COTS inject white vinegar inside COTS
Up to 2021 great barrier reef foundation manually counts COTS within range in GBFR to analyze outbreak of COTS which is not accurate , with help of object detection model and Underwater video footage , thousands of reef images and the AI technology could drastically improved efficiency and scale at which the reef manages detect and control COTS outbreaks.
Our work will help researchers identify species that are threatening Australia's Great Barrier Reef and take well-informed action to protect the reef for future generations.

---

Table of content
Business Problem
Business Constraint
Performance Metrics
Data Analysis
EDA
Feature Engineering
Modelling / Approaches Tried
Model Comparison
model Pipeline & Deployment
Future Extension
Reference

Business Problem
In this competition, we  will predict the presence and position of crown-of-thorns starfish in sequences of underwater images taken at various times and locations around the Great Barrier Reef. Predictions take the form of a bounding box together with a confidence score for each identified starfish. An image may contain zero or more starfish.

---

2.Business Constraint
We are solving 2 business problems here.
1. We need to identify COTS in real time video footage.
2. With the help of underwater video footage the great barrier reef foundation will analyze COTS breakout within a time period.
For task 1 we need low latency and for task 2 we don't have any barrier to detect within any constraints.

---

3.Performance Metrics
This competition is evaluated on the F2 Score at different intersection over union (IoU) thresholds. The F2 metric weights recall more heavily than precision, as in this case it makes sense to tolerate some false positives in order to ensure very few starfish are missed.

---

4.Data Analysis
video_id - ID number of the video the image was part of. The video ids are not meaningfully ordered.
video_frame - The frame number of the image within the video. Expect to see occasional gaps in the frame number from when the diver surfaced.
sequence - ID of a gap-free subset of a given video. The sequence ids are not meaningfully ordered.
sequence_frame - The frame number within a given sequence.
image_id - ID code for the image, in the format '{video_id}-{video_frame}'
annotations - The bounding boxes of any starfish detections in a string format that can be evaluated directly with Python. Does not use the same format as the predictions you will submit. Not available in test.csv. A bounding box is described by the pixel coordinate (x_min, y_min) of its upper left corner within the image together with its width and height in pixels.

We have a total 23501 number of images in the data frame.
Data frame contains three different video images. Those video images can be separated by variable video ID.
Video 0 contain 6708 number of images 
video 1 contain 8232 number of images 
video 2 contain 8561 number of images.

---

5.Exploratory Data Analysis (EDA)
