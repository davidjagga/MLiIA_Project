***This code will perform with far less complications on a Jupyter Lab PyTorch server on Rivanna***


# Formatting the Dataset
This section explains how to prepare the dataset for training and testing (using `makeDataset.ipynb` file).

***Before using this code, be sure to move the Regression Dataset provided into the working directory or properly specify location***
## Steps:
1. **Install Dependencies**  
   The `makeDataset` script uses several dependencies. Ensure all required libraries are installed before proceeding. You can install necessary ones as follows:
   ```bash
    !pip install -r requirements.txt
   ```
   If other dependicies are needed install them as well.
2. **Update Code Paths**  
   In the `makeDataset` file, update the following lines to point to the correct data directories:
   ```python
    mnist_path = "/path/to/mnist"
    quick_draw_path = "/path/to/google_quickdraw"
    data_path = "/path/to/dataset"
   ```
   Ensure these paths match the location of your MNIST and Quick Draw datasets.

3. **Run the Code**  
   Execute all code blocks in the `makeDataset` jupyter notebook

---

# Training
This section guides you through training the Transmorph model (using `trainTransmorph.ipynb` file).


***Pre-trained models are typically stored under the `experiments` folder. However, because of model size only one was included. 
If needed you can move model file into this folder and test this model with***

## Steps:
1. **Update Data Path**  
   Update the data path in the `trainTransmorph` file to match the path specified in the `makeDataset` file.
   ```python
    data_path = "/path/to/dataset"
   ```
2. **Configure Model Parameters**  
   Adjust the following parameters in the script as needed (Epochs, Learning rate, etc.).

3. **Run the Code**  
   Execute all code blocks in the `trainTransmorph` file

4. **Training Logs**  
   After training, the logs will be saved in the `logs` folder for reference.

---

# Testing 
This section explains how to test the trained model (using `inferTransmorph.ipynb` file).

## Steps:
1. **Update Data Path**  
   Update the data path in the `inferTransmorph` file to match the path specified in the `makeDataset` file.
   ```python
    data_path = "/path/to/dataset"
   ```
2. **Run the Code**  
   Execute all code blocks in the `infer_Transmorph` file:
   ```bash
   python infer_Transmorph.py
   ```


