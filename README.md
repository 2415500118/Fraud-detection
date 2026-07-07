# Financial Fraud Detection using ANN

An end-to-end machine learning project that detects fraudulent credit card transactions using an Artificial Neural Network (ANN).

## What this project does

- Loads and explores a credit card fraud dataset
- Preprocesses the data for model training
- Handles class imbalance using SMOTE
- Trains an ANN with TensorFlow/Keras
- Evaluates the model using accuracy, loss, confusion matrix, and classification report
- Saves the trained model for later use

## Project Structure

```text
Financial Fraud Detection/
├── Dataset/
│   └── creditcard.csv
├── models/
│   └── fraud_ann.keras
├── notebook/
│   └── fraud_detection.ipynb
├── .venv/
├── .gitignore
├── .gitattributes
├── requirements.txt
└── README.md
```

## Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn
- TensorFlow / Keras
- Jupyter Notebook

## Dataset

The project uses:

- `Dataset/creditcard.csv`

Important note:

- This file is large, so it is tracked with Git LFS in the repository.
- If you clone the repo, make sure Git LFS is installed so the dataset downloads correctly.

## Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/2415500118/Fraud-detection.git
cd Fraud-detection
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

### 3. Activate the virtual environment

**Windows PowerShell**

```powershell
.\.venv\Scripts\Activate.ps1
```

**Command Prompt**

```cmd
.venv\Scripts\activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

If you are using the notebook from VS Code, also make sure the Jupyter extension is installed and select the `.venv` interpreter.

## Run the Notebook

Open:

- `notebook/fraud_detection.ipynb`

Then run the cells in order.

The notebook covers:

1. Library imports
2. Loading the dataset
3. Basic exploration
4. Splitting features and target
5. Scaling data
6. Applying SMOTE
7. Building the ANN
8. Training the model
9. Plotting training and validation curves
10. Evaluating predictions
11. Saving the model

## Model Output

The trained model is saved here:

```text
models/fraud_ann.keras
```

You can reload it later with:

```python
from tensorflow.keras.models import load_model
model = load_model("models/fraud_ann.keras")
```

## Example Usage

```python
import pandas as pd
from tensorflow.keras.models import load_model

model = load_model("models/fraud_ann.keras")
df = pd.read_csv("Dataset/creditcard.csv")
```

## Notes

- The project is configured for the local `.venv` in VS Code.
- TensorFlow on native Windows will run on CPU only unless you use WSL2 or a DirectML setup.
- If you change the dataset path, update the notebook accordingly.

## Future Improvements

- Try different model architectures
- Add hyperparameter tuning
- Compare ANN with XGBoost, Random Forest, and logistic regression
- Build a simple prediction UI

## License

No license has been added yet.
