# HandwrittenEquationSolver

A handwritten equation solver using Convolutional Neural Networks. 

It works on images having handwritten digits from 0 to 9 and the symbols '+', 'x' and '-' in black colour and white background. 
 
1. The training dataset can be downloaded from the [Handwritten math symbols dataset](https://www.kaggle.com/xainano/handwrittenmathsymbols) on Kaggle. Unfortunately, this dataset has greater than 80% repeated examples
2. `unique.py` removes repeated images from the dataset and `extracted_images.zip` contains the cleaned dataset
3. `Data_extraction.ipynb` extracts the data from the dataset, applies image processing techniques like Contour Detection and Bounding Rectangle using OpenCV, and creates `train_final.csv`
4. `train.ipynb` trains the CNN model with TensorFlow using the data in `train_final.csv` and saves the model in `model_final.h5` and `model_final.json`
5. `CNN_test.ipynb` processes the handwritten equation in `test1.png`, uses `model_final.h5` and `model_final.json` to recognize the equation, and uses the 'eval' function to solve the equation

Achieved a test accuracy of 97.12% in recognizing handwritten digits & mathematical symbols. 