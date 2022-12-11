# Face-Recognition

Problem Statement
We intend to perform face recognition. Face recognition means that for a given image you can tell the subject id. 
Our database of subject is very simple. It has 40 subjects.

1. Download the dataset and understand the format (10 Points)
  a. We will use ORL dataset.
    http://www.cl.cam.ac.uk/research/dtg/attarchive/facedatabase.html
  b. The data is available at the following link.
    http://www.cl.cam.ac.uk/Research/DTG/attarchive/pub/data/att_faces.tar.Z
  c. The dataset has 10 images per 40 subjects. Every image is a grayscale image of size 92x112.

2. Generate the Data Matrix and the Label vector (10 Points)
  a. Convert every image into a vector of 10304 values corresponding to the image size.
  b. Stack the 400 vector into a single Data Matrix D and generate the label vector y.
    The labels are integers from 1:40 corresponding to the subject id.
3. Split the Dataset into Training and Test sets (10 Points)
  a. From the Data Matrix D 400x10304 keep the odd rows for training and the even rows for testing. This will give you 5 instances per person for training and 5 instances per person for testing.
  b. Split the labels vector accordingly.
4. Classification using PCA.(45 points)
  a. Use the pseudo code below for computing the projection matrix U. Define the alpha ={0.8,0.85,0.9,0.95}
  b. Project the training set and test sets separately using same projection matrix.
  c. Use a simple classifier (first Nearest Neighbor to determine the class labels).
  d. Report Accuracy for every value of alpha separately.
  e. Can you find a relation between alpha and the classification accuracy?
  
5. Classifier Tuning (20 points)
  a. Set the number of neighbors in the K-NN classifier to 1,3,5,7.
  b. Tie breaking at your prefered strategy.
  c. Plot (or tabulate) the performance measure (accuracy) against the K value.
    This is to be done for PCA.

6. BONUS (20 Points)
  a. [5 points] Use different Training and Test splits. Change the number of instances per subject to be 7 and keep 3 instances per subject for testing. compare the results you have with the ones you got earlier with 50% split.
  b. [15 points] Download non-face images and make them of same size 92x112. and try to solve the classification problem faces vs. Non-faces.
    i. Show failure and success cases.
    ii. Plot the accuracy vs the number of non-faces images while fixing the number of face images.
    iii. Criticize the accuracy measure for large numbers of non-faces images in the training data.
