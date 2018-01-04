# Semantic Segmentation
### Introduction
In this project, you'll label the pixels of a road in images using a Fully Convolutional Network (FCN).

### Setup
##### Frameworks and Packages
Make sure you have the following is installed:
 - [Python 3](https://www.python.org/)
 - [TensorFlow](https://www.tensorflow.org/)
 - [NumPy](http://www.numpy.org/)
 - [SciPy](https://www.scipy.org/)
##### Dataset
Download the [Kitti Road dataset](http://www.cvlibs.net/datasets/kitti/eval_road.php) from [here](http://www.cvlibs.net/download.php?file=data_road.zip).  Extract the dataset in the `data` folder.  This will create the folder `data_road` with all the training a test images.

### Start
##### Implement
Implement the code in the `main.py` module indicated by the "TODO" comments.
The comments indicated with "OPTIONAL" tag are not required to complete.
##### Run
Run the following command to run the project:
```
python main.py
```
**Note** If running this in Jupyter Notebook system messages, such as those regarding test status, may appear in the terminal rather than the notebook.

### Submission
1. Ensure you've passed all the unit tests.
2. Ensure you pass all points on [the rubric](https://review.udacity.com/#!/rubrics/989/view).
3. Submit the following in a zip file.
 - `helper.py`
 - `main.py`
 - `project_tests.py`
 - Newest inference images from `runs` folder  (**all images from the most recent run**)
 
 ## How to write a README
A well written README file can enhance your project and portfolio.  Develop your abilities to create professional README files by completing [this free course](https://www.udacity.com/course/writing-readmes--ud777).

# Results
1. Loss:  0.0936639
- Added regularization loss to Cross-Enthropy Loss for overall loss calculation. 
- batch-size = 10
- epochs = 50
- learning_rate = 1e-3
2. Loss:  1.45224
- Loss dropper from 73k to .82 in the 22nd epoch. However, it shot back up from there until I terminated training at 25 epochs. Will experiment with batch size first before messing with learning rate.
- batch-size = 20
- epochs = terminated at 25
- learning_rate = 5e-3
3. Loss:  0.815233 
- Loss began to oscillate around 80% starting from epoch 22. No further progress seems possible.
- batch-size = 15
- epochs = terminated at epoch 39
- learning_rate = 1e-3
4. 
- 
- batch-size = 5
- epochs = 50
- learning_rate = 1e-3