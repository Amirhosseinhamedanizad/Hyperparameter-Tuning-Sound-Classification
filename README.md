# Hyperparameter-Tuning-Sound-Classification

librosa/Sound Classification using Mel-frequency cepstral coefficients (MFCCs) and Support Vector Machine (SVM) with Hyperparameter Tuning.



1. Load the dataset: The code loads the dataset from 'Baph_mfccs_data.csv', which contains the Mel-frequency cepstral coefficients (MFCCs) as features and class labels.

2. Data Preprocessing:
   - Rows with all zeros in the MFCC features are dropped to remove any empty or uninformative data points.
   - The features (MFCCs) are extracted, and the class labels are separated.

3. Handling Class Imbalance:
   - The class distribution is checked, and Random Over-Sampling (ROS) is applied to balance the class distribution. ROS creates synthetic samples for the minority class to match the majority class samples.

4. SVM Classifier with Hyperparameter Tuning:
   - A Support Vector Machine (SVM) classifier is used with hyperparameter tuning.
   - Grid search with Leave-One-Out cross-validation is applied to find the best hyperparameters (C and kernel) for the SVM classifier.

5. Visualizing t-SNE Scatter Plot:
   - t-SNE (t-distributed Stochastic Neighbor Embedding) is used to reduce the dimensionality of the MFCC features to 2D for visualization purposes.
   - The t-SNE scatter plot is created to visualize the distribution of dolphin and non-dolphin samples in the reduced 2D space.

6. Printing Results:
   - The best hyperparameters and the accuracy of the best model on the training set are printed.

Note: The accuracy and performance of the model depend on the size and quality of the dataset and the audio features used for classification. In this code, with only one instance per class, the accuracy may not be meaningful, and the model may not generalize well to new, unseen data. To build a more robust model, you need a larger and more balanced dataset with sufficient instances for each class. Additionally, feature engineering and tuning of the classifier's hyperparameters can further improve the model's performance.



The code performs the following main tasks:
1. Preprocessing the dataset containing MFCC features and class labels.
2. Handling class imbalance by applying Random Over-Sampling (ROS).
3. Training an SVM classifier with hyperparameter tuning using Grid Search and Leave-One-Out cross-validation.
4. Visualizing the MFCC features in a reduced 2D space using t-distributed Stochastic Neighbor Embedding (t-SNE).
5. Printing the best hyperparameters and accuracy of the SVM model on the training set.

