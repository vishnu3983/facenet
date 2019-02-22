# facenet

sudo pip3 install -r requirements.txt



DOWNLOAD AND EXTRACT THE PRE-TRAINED MODEL FOLDER: 
https://drive.google.com/file/d/1EXPBSXwTaqrSC0OhUdXNmKSh9qJUQ55-/view

COMPARE TWO IMAGES:
python3 compare.py 20180402-114759/ test-images/v1.jpg test-images/v2.jpg --image_size 160 --margin 32 --gpu_memory_fraction 0

PREPROCESSING:
sudo python3 align_dataset_mtcnn.py raw/ aligned/ --image_size 160 --margin 32



TRAINING THE CLASSIFIER:
sudo python3 classifier.py TRAIN aligned 20180402-114759/ 20180402-114759/my_classifier.pkl --batch_size 64 --min_nrof_images_per_class 5 --nrof_train_images_per_class 5 --use_split_dataset




FACE RECOGNITION ON IMAGE:
sudo python3 face_recognition_image.py test-images/v1.jpg




FACE RECOGNITION ON VIDEO:
sudo python3 face_recognition_video.py test-images/video.3gp 






REFERENCES:

https://github.com/abhijeet3922/Face_ID

https://github.com/davidsandberg/facenet

https://appliedmachinelearning.blog/2018/10/30/yet-another-face-recognition-demonstration-on-images-videos-using-python-and-tensorflow/
