# Instrument Classification

This project is a deep learning-based image classifier for musical instruments. It uses TensorFlow and Keras to train a convolutional neural network (CNN) on a dataset of instrument images.

## Project Structure

```
Instrument_Classifier.ipynb
instruments.csv
dataset/
    train/
        <instrument folders>/
            <images>.jpg
    test/
        <instrument folders>/
            <images>.jpg
    test_sample/
        1.jpg
        2.jpg
        ...
        stuff.jpg
        test.png
```

- **Instrument_Classifier.ipynb**: Main Jupyter notebook for training, evaluating, and predicting instrument classes.
- **instruments.csv**: CSV file mapping image paths to instrument labels and dataset splits.
- **dataset/**: Contains training, test, and sample images organized by instrument.

## How to Use

1. **Install dependencies**  
   Make sure you have Python 3 and the following packages:
   - tensorflow
   - numpy
   - matplotlib

   You can install them with:
   ```sh
   pip install tensorflow numpy matplotlib
   ```

2. **Prepare the dataset**  
   Place your images in the `dataset/train` and `dataset/test` folders, organized by instrument name.

3. **Run the notebook**  
   Open `Instrument_Classifier.ipynb` in Jupyter or VS Code and run all cells to:
   - Load and preprocess data
   - Build and train the CNN model
   - Predict instrument classes for sample images

## Model

The model is a simple CNN with three convolutional layers, followed by dense layers and dropout for regularization. It is designed for 30 instrument classes.

## Prediction

To predict the instrument in a sample image, use:
```python
predict_instrument('dataset/test_sample/1.jpg', model, class_labels)
```
The result is displayed as an image with the predicted class and printed in the terminal.

## License

This project is for educational
