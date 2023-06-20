## Credit Card Fraud Detection
Credit card fraud detection is a critical task in maintaining the security and integrity of financial transactions. This repository provides an overview of a comprehensive credit card fraud detection system that incorporates various techniques and models to detect fraudulent activities.


## Data Preprocessing:
Pre-processing is an essential step in credit card fraud detection to gain a better understanding of the data and uncover patterns, anomalies, or trends that may indicate fraudulent activities. Sensitive information like credit card numbers, merchant details, and coordinates are encrypted using encryption techniques to ensure data security and privacy. Two techniques used for encryption are:

FF3: FF3 is a format-preserving encryption scheme that encrypts credit card numbers while preserving their original format and length. It ensures that the encrypted output maintains the same format as the original credit card number, allowing for reversible encryption without compromising data integrity.

GeoHashing: GeoHashing is used to encode and index geographical coordinates, such as latitude and longitude, into a string format. This technique enables efficient indexing and searching of geographical data based on proximity.

RFM: RFM (Recency, Frequency, Monetary) is performed to derive meaningful features from the transaction data. RFM metrics capture the recency of transactions, the frequency of transactions, and the monetary value of transactions, along with the risk and credit score of merchants and categories.We have used this to gain a better understanding of customer behaviour and identify segments with different characteristics. It provides insights into customer value and engagement by analysing three key dimensions: recency, frequency, and monetary value.

## Over Sampling
Credit card fraud detection involves dealing with imbalanced datasets where fraudulent transactions are significantly less common than legitimate transactions. To address this class imbalance issue, the Adaptive Synthetic Sampling (ADASYN) technique is used. ADASYN generates synthetic instances of the minority class (fraudulent transactions) based on their feature distributions. This approach helps in creating a more representative dataset for training the model and improves the performance in detecting credit card fraud instances.

## Feature Selection

Weighted feature selection techniques are implemented to determine the importance or relevance of features in the dataset. Two feature selection techniques used in this system are:

Genetic Algorithm (GA): Genetic algorithms are well-suited for feature selection in credit card fraud detection. They automatically search through a large feature space and identify the most informative subset of features for fraud detection. GA can capture feature interactions, handle multicollinearity, and optimize model hyperparameters.

Particle Swarm Optimization (PSO): PSO is a metaheuristic optimization algorithm that iteratively searches the solution space to find the optimal feature subset. PSO is efficient, parallelizable, and capable of balancing accuracy and complexity in feature selection.

## Train the LSTM model:
1. Set up the LSTM architecture, including the number of layers, hidden units, and activation functions.
2. Prepare the training data by formatting it into appropriate input-output sequences.
3. Initialize the LSTM model with the defined architecture.
4. Train the LSTM model using the training data.
5. Monitor the training process and adjust hyperparameters if needed.
6. Save the trained LSTM model for future use.

## Generate LSTM predictions:
1. Load the saved LSTM model.
2. Prepare the testing data by formatting it into appropriate input sequences.
3. Generate predictions using the trained LSTM model.
4. Evaluate the performance of the LSTM predictions using appropriate metrics.

## Combine LSTM predictions with original features:
1. Retrieve the original features from the testing data.
2. Concatenate the LSTM predictions with the original features.
3. Perform any necessary post-processing on the combined data.

## Train the ARF model:
1. Set up the ARF (AutoRegressive Forest) model architecture.
2. Prepare the training data by formatting it into appropriate input-output sequences.
3. Initialize the ARF model with the defined architecture.
4. Train the ARF model using the training data.
5. Save the trained ARF model for future use.

## Generating LSTM predictions for new Data:
1. Load the saved LSTM model.
2. Prepare the new data by formatting it into appropriate input sequences.
3. Generate predictions for the new data using the trained LSTM model.

## Combine LSTM predictions with original features for new data:
1. Retrieve the original features from the new data.
2. Concatenate the LSTM predictions with the original features for the new data.
3. Perform any necessary post-processing on the combined data.

## Make predictions using ensemble:
1. Combine the LSTM predictions with the original features for both the testing data and the new data.
2. Feed the combined data into the trained ARF model.
3. Generate final predictions using the ensemble of LSTM and ARF models.
4. Evaluate the performance of the ensemble predictions using appropriate metrics.


This README provides an overview of the steps involved in data preprocessing, training LSTM and ARF models, generating predictions, and using ensemble techniques
