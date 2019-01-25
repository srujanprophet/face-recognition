# face-recognition
Face recognition using opencv.

### The following steps take place while recognising a face :
1. Face Detection: Look at the picture and find a face in it.
2. Data Gathering: Extract unique characteristics of Kirti’s face that it can use to differentiate him from another person, like eyes, mouth, nose, etc.
3. Data Comparison: Despite variations in light or expression, it will compare those unique features to all the features of all the people you know.
4. Face Recognition: It will determine “Hey, that’s Kirti!”

## The process is divide into 3 steps :
1. Prepare Training Data: Read training images for each person/subject along with their labels, detect faces from each image and assign each detected face an integer label of the person it belongs.
2. Train Face Recognizer: Train OpenCV's LBPH recognizer by feeding it the data we prepared in step 1.
3. Prediction: Introduce some test images to face recognizer and see if it predicts them correctly.
### CODE DEPENDENCIES : 
- OpenCV 3.2.0
- Python v3.5
- NumPy

### REQUIRED MODULES :
Following modules were used :
cv2: This is the OpenCV module for Python used for face detection and face recognition.
os: We will use this Python module to read our training directories and file names.
numpy: This module converts Python lists to numpy arrays as OpenCV face recognizer needs them for the face recognition process.
1. PREPARE TRAINING DATA :
The premise here is simple:
The more images used in training, the better.
Being thorough with this principle is important because it is the only way for training a face recognizer so it can learn the different ‘faces’ of the same person; for example: with glasses, without glasses, laughing, sad, happy, crying, with a beard, without a beard, etc.
So, our training data consists of total two people with 100 images of each one. All training data is inside the folder:training-data.
2. DATA PREPARATION FOR FACE RECOGNITION :
Well, to know which face belongs to which person, OpenCV face recognizer accepts information in a particular format. In fact, it receives two vectors:
One is the faces of all the people.
The second is the integer labels for each face.
For example, if we had two individuals and two images for each one. Then, the data preparation step will produce face and label vectors.
3. PREDICTION :
This is where we get to see if our algorithm is recognizing our individual faces or not.We’re going to take one test image of each person, use face detection and then pass those faces to our trained face recognizer. Then we find out if our face recognition is successful.
