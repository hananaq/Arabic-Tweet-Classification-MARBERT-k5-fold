# Arabic-Tweet-Classification-MARBERT
This repository contains a Jupyter Notebook designed for Arabic text classification using the MARBERT model, k-fold cross-validation was used to ensure robust performance evaluation.
MARBERT is a state-of-the-art transformer-based model fine-tuned for tasks involving Arabic natural language processing (NLP).

<h3>Dataset <h3>
the dataset used to train the model can be obtained from the following link https://www.sciencedirect.com/science/article/pii/S2352340923009472#bib0001.
it's collected from Twitter and has two classes Spam and Ham.<br>
I have also added the dataset to this project for ease of use. <br>

<h3>Prerequisites</h3> 
Ensure you have the following dependencies installed before running the notebook:

Python 3.7+ <br>
Jupyter Notebook <br>
Hugging Face Transformers <br>
PyTorch <Br>
scikit-learn <br>
pandas <br>
numpy <br>
matplotlib

<h3>Notes for excution</h3> 
During the execution of this project, the dataset is accessed from Google Drive, and the trained model is saved back to Google Drive. To ensure the project runs correctly, update the path parameter to match your own Google Drive directory.
<br><br>
For example: path = '/content/drive/MyDrive/Colab/AR/'
<br><br>
Replace '/content/drive/MyDrive/Colab/AR/' with the path where your dataset and model will be stored in your Google Drive.
<br>
<br>

<h3>Model Evaluation</h3>
The performance of the trained MARBERT model was evaluated using 5-fold cross-validation to ensure robust and unbiased results. During cross-validation:
<ul>
<li>The dataset was split into 5 folds, with each fold used once as a validation set while the remaining folds were used for training.</li>
<li>Precision, recall, and F1-score were calculated for each fold.</li>
<li>At the end of the evaluation, the average results for both class 0 (Ham) and class 1 (Spam) were obtained.</li>
  </ul>
  
<h4>Final 5-Fold Cross-Validation Results</h4>
<strong>Class 0 (Ham):</strong>
<ul>
<li>Precision: 0.9943</li>
<li>Recall: 0.9950</li>
<li>F1-score: 0.9947</li>
</ul>
<strong>Class 1 (Spam):</strong>
<ul>
<li>Precision: 0.9963</li>
<li>Recall: 0.9957</li>
<li>F1-score: 0.9960</li>
</ul>

<strong>Overall Metrics</strong>
<br>
Confusion Matrix:<br>
[[11189    56]<br>
 [   64 14851]]<br>
<strong>Overall Accuracy:</strong> 0.9954
<br>
These results demonstrate the model's excellent performance in accurately classifying both Ham and Spam tweets, with a near-perfect accuracy and strong F1-scores for both classes.



