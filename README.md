# Face-Recognition

We intend to perform face recognition. face recognition means that for a given image you can
tell the subject id. Our database of subjects is very simple. It has 40 subjects. Below we will
show the needed steps to achieve the goal of the assignment.

# 1. Download the dataset and understand the format 

  a. ORL dataset is available at the following link.
  https://www.kaggle.com/kasikrit/att-database-of-faces
  
  b. The dataset has 10 images per 40 subjects. Every image is a grayscale image of
  size 92x112.
  
  
# 2. Generate the Data Matrix and the Label vector 

  a. Convert every image into a vector of 10304 (92x112) values corresponding to the image
  Size.
  
  b. Stack the 400 vectors into a single Data Matrix D and generate the label vector y.
  The labels are integers from 1:40 corresponding to the subject id.
  
  
# 3. Split the Dataset into Training and Test sets 
  (don’t split randomly, as you might end with a whole class/subject in the test set that the model
  never saw in the training set )
  
  a. From the Data Matrix D 400x10304 () keep the odd rows for training and the even rows
  for testing. This will give you 5 instances per person for training and 5 instances
  per person for testing.
  
  b. Split the labels vector accordingly.
  
  
# 4. Classification using PCA.

  a. Use the pseudo-code below for computing the projection matrix U. Define the
  alpha ={0.8,0.85,0.9,0.95}
  
  b. Project the training set and test sets separately using the same projection matrix.
  
  c. Use a simple classifier (first Nearest Neighbor to determine the class labels).
  
  d. Report Accuracy for every value of alpha separately.
  
  
# 5. Classifier Tuning 

  a. Set the number of neighbors in the K-NN classifier to 1,3,5,7.
  
  b. Tie-breaking at your preferred strategy.
  
  c. Plot (or tabulate) the performance measure (accuracy) against the K value.
  This is to be done for PCA and LDA as well.
  
  
# 6. Bonus

  a. Use different Training and Test splits. Change the number of
  instances per subject to be 7 and keep 3 instances per subject for testing.
  compare the results you have with the ones you got earlier with 50% split.
