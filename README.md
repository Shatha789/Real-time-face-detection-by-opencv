# Real-time-face-detection-by-opencv

I using pycharm and python using opencv, firstly I use and save file Haar cascade classifiers feature for detecting face, The files you will find it here : (https://github.com/opencv/opencv/tree/master/data/haarcascades)


# Import And Define The Classifiers : 

    import cv2

    face_cascade = cv2.CascadeClassifier('haarcascade_frontalface_default.xml')

# Call The Classifier Function And Read The Image : 

    img = cv2.imread('img.jpg')

    gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

    faces = face_cascade.detectMultiScale(gray, 1.1, 4)

# Detect The Face : 

    for (x, y, w, h) in faces:

    cv2.rectangle(img, (x, y), (x + w, y + h), (255, 0, 0), 2)

# Desplay The Output :

    cv2.imshow('img', img)

    cv2.waitKey() 


<img width="600" alt="image" src="https://user-images.githubusercontent.com/86571348/125369216-86b30700-e384-11eb-8c3f-8ca5675d74ec.png">


