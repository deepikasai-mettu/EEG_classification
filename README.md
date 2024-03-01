## EEG_classification

This repository aims to develop a robust classification model to analyze EEG data and effectively categorize it into distinct classes. The primary focus of this classification endeavor is the diagnosis of epilepsy

### Project Summary:

Throughout this project, including data preprocessing, feature extraction, data splitting, model selection, training and evaluation. Here's an overview of the tasks undertaken

#### Data Acquisition and Inspection:

CHB-MIT EEG Database: This dataset encompasses EEG recordings obtained from individuals diagnosed with epilepsy. It offers a diverse range of seizure types and includes non-seizure data for a comprehensive analysis. Data for patients 1 and 5 is used.


#### Feature Extraction:
The feature extraction process is a crucial step in preparing EEG data for classification. The goal is to transform raw EEG signals into a set of relevant features that capture essential characteristics for the subsequent classification task

1. Read Raw EEG Data: Utilize the `mne` library to read the raw EEG data from the specified EDF file.
2. Filter EEG Data: Apply band-pass filtering to focus on relevant frequency components (1 - 50 Hz).
3. Windowed Feature Extraction: Divide the EEG data into overlapping windows of a specified length (3 seconds). Extract primary and secondary features for each window.
4. Feature Storage: Store the extracted features along with timestamps in a structured format.
5. Output: Return a numpy array containing the timestamp, primary features, and secondary features for each windowed segment.

#### Data Splitting:

The data splitting phase involves dividing the dataset into training and test sets, addressing class imbalance through up sampling using Synthetic Minority Over-sampling Technique (SMOTE).

#### Model Selection, Training, and Evaluation:

Used Random Forest Classification, Decision Tree and CNN for modelling, training and evaluation.

The Random Forest model achieved the highest accuracy among the evaluated models, with an accuracy of 97.71%. However, the F1 score is relatively low at 10.38%, suggesting that the model might be struggling with false positives and false negatives.
The Decision Tree model shows a good balance between accuracy (87.52%) and F1 score (87.75%). It's essential to consider both metrics, and the Decision Tree model seems to perform well overall.
The Convolutional Neural Network (CNN) achieved a high accuracy of 97.57%, but the F1 score is lower at 9.21%. This indicates a potential imbalance between precision and recall, which might be addressed through further optimization

#### Visualizations:

Used Matplotlib and Seaborn to visualize accuracy and F1 score of Random Forest, Decision Tree and CNN.
