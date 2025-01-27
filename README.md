

## SUBMITTED FOR DALI 2025

### Preparing the Dataset
- Images of barnacles and their corresponding masks were used.
- Masks provided labels for each pixel: `1` for barnacle, `0` for non-barnacle.
- RGB values of pixels were used as features.
- To make training efficient, the dataset was downsampled by randomly selecting a subset of pixels.

### Model
- Logistic Regression was used for its simplicity and effectiveness in binary classification tasks.

### Training the Model
- The dataset was split into training and test sets.
- The logistic regression model was trained on sampled pixel data.
- Model performance was evaluated on unseen images to check how well it generalized.

### Challenges
- Processing high-resolution images caused memory errors.
- Initial results with RGB values alone were limited, leading to iterative improvements.
- Implemented batch predictions to handle large images efficiently.

## Repository Structure

- `barnacles.ipynb`: Jupyter Notebook with code for training and testing the model.
- `img1.png`, `img2.png`: Example training images.
- `mask1.png`, `mask2.png`: Masks corresponding to the training images.
- `unseen_img1.png`, `unseen_img2.png`: Test images used for evaluating model performance.
- `masked_img1.png`, `masked_img2.png`: Example visualizations of annotated barnacle regions.
- `README.md`: This file.

## How to Run

### Prerequisites
Install the required dependencies:

numpy 
opencv-python 
opencv-python-headless 
scikit-learn
matplotlib

### Steps
1. Place the training and test images in the same directory as the notebook.
2. Open and run `barnacles.ipynb` to:
   - Train the logistic regression model on the provided dataset.
   - Evaluate the model on test images.

### Outputs
- Binary masks showing predicted barnacle regions.
- Model accuracy

## Conclusions
- **Strengths**: Logistic regression provides a simple and interpretable baseline for pixel classification.
- **Challenges**: Memory limitations required optimizations like batch-based processing. Makes things much more inefficient and inaccurate. Also generally could use more training data for the sake of accuracy.
- **Future Suggestions**:
  - Add more features (like spatial location or texture).
  - Experiment with advanced models like Random Forests or CNNs for better accuracy.