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
    - learning_rate = 5e-3
4. Loss:  0.48977 
    - Performance was better than when I trained with batch-size greater than 10. However, it seems the batch is still too small. The loss decreases at a very small rate and gets stuck around 40% at the 30th epoch.
    - batch-size = 5
    - epochs = 50
    - learning_rate = 5e-3
5. Loss:  1.80411
    - Realized I forgot to reset the learning rate to 1e-3 after the 2nd trial. Will redo all previous trials with learning_rate set to 1e-3. The loss dropped to .48 at it's lowest around the 13th epoch, and shot back up after the 14th epoch.
    - batch-size = 8
    - epochs = 50
    - learning_rate = 5e-3
6. Loss:  0.0794493
    - This is the lowest loss value so far. The model started to get stuck around 10% around the 40th epoch. So it seems I am on the right track with learning_rate and batch size for now.
    - batch-size = 8
    - epochs = 50
    - learning_rate = 1e-3
7. Loss:  0.135729
    - It seems 8 was a better choice for batch size. Will try 9 and 11 just to be sure.
    - batch-size = 7
    - epochs = 50
    - learning_rate = 1e-3
8. Loss:  0.138438
    - Loss shot up a little bit. Seems I need to experiment with batch-size a little more, but 8 seems ideal so far.
    - batch-size = 9
    - epochs = 50
    - learning_rate = 1e-3
9. Loss:  0.0853587
    - It seems 8 was the best so far. Although, 11 came really close. May be useful too keep playing with batch sizes.
    - batch-size = 11
    - epochs = 50
    - learning_rate = 1e-3
10. Loss:  0.0982808
    - Not the ideal situation. looking for a way to further reduce error.
    - batch-size = 8
    - epochs = 50
    - learning_rate = 5e-4
11. Loss:  0.146899
    - The loss just oscillated around 15% 
    - batch-size = 11
    - epochs = terminated at 35
    - learning_rate = 5e-4
12. 
    - 
    - batch-size = 8
    - epochs = 50
    - learning_rate = 8e-4