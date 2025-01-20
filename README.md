# submitted for 2025 dali application

my process: 

- preparing the dataset:
    * start with barnacle image and a mask
    * treat this as a data set with labels, as the  mask tells you where the barnacles are
    * this prototype will have the RGB values of the picture as features
    * full data set is pixel by its RGB value
    * label is 0 or 1 depending on if pixel marked as barnacle
    * these images are high resolution and have a lot of pixels, so we need a way to generalize the data a bit more, so we downsample the image (lowering pixel) and we train on random pixels to be efficient

- model:
    * using logistic regressions as it's a simple model that works decently well for binary classification

- training model:
    * features & mask values are split into training and test datasets
    * test data will evaluate performance
    * make sure to value barnacle pixels more than non-barnacle pixels by adjusting class weights

- evaluating model performance:
    * besides the test set, we are also provided more images that can serve as better data

