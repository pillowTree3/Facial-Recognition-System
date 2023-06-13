# Facial-Recognition-System-Using-Siamese-Neural-Network



The project can be sub-classified into 2 sub-problems:
1) Face Detection
2) Face Recognition

The face detection problem is resolved using the Haar Features which all together is based on regions with dark and light pixels in face.
This is implemented using the opencv library.
The sample detected faces can be seen sample_faces/detected_faces which is when ran over the images in sample_faces.

### One Shot Learning ###
The project is based on one-shot learning which is because we need a facial recognition system which is fast, scalable and has high accuracy with small data.
- We use *convulational layers* to extract indentifying features from faces. The convolutional layers should map faces from the same subject close to one another in this lower-dimension feature space and vice versa, faces from different subjects should be as far away as possible in this lower-dimension feature space.
- Using the *Euclidean Distance* which is  the difference of the two lower-dimension vectors output from the convolutional layers which are indeed the basis of our Siamese Network

#### DataSet ####
The dataset that is chosen is the Database of Faces, created by AT&T Laboratories, Cambridge. The database contains photos of 40 subjects, with 10 photos of each subject. The photos of each subject were taken under different lighting and angles, and they have different facial expressions. For certain subjects, multiple photos were taken of people with and without glasses.

### Siamese Neural Network ###
Siamese Neural Network is a special type of neural network architecture that is designed to compare and measure the similarity between pairs of inputs. The network consists of two identical subnetworks that share the same weights and architecture. Each subnetwork takes in one input from a pair and transforms it into a lower-dimensional feature representation. The outputs from both subnetworks are then compared using a similarity metric such as Euclidean distance or cosine similarity.
The shared convulational neural network of the siamese net is made with the help of keras library in python, where each of the identical layers have a series of *Conv2D, MaxPooling2D, Flatten and Dense* layers with *contrastive loss* as the loss function.
After the training and the onboarding process in this process, a dissimalirity score(distance output by the model...the greater the distance, the greater the dissimilarity between the two faces) using which we can analyze the result.











