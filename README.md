# ACS WIL Data Analysis Project - Group 3

## Telecommunication Customer Churn Project Deliverables

**1: Data Preparation Deliverables:**

- A preprocessed dataset addressing missing data points and encoding categorical variables.
- The dataset is split into distinct training and testing sets to facilitate model validation.
- Appropriate scaling techniques are applied to normalize the data, enhancing model performance.
  

**2: Clustering Analysis Deliverables:**

- The optimal number of clusters is identified using the elbow method.
- A K-Means clustering model is trained on the dataset.
- Resulting clusters are visualized and labeled for interpretation and actionable insights.

**3: Predictive Modeling Deliverables:**

- Defined ANN Architecture: The input layer specifies the input shape; hidden layers with 64, 32, and 16 units use ReLU activation, and the output layer applies a sigmoid activation for binary classification.
- Training Process: Dataset preprocessing includes encoding and scaling; the model is trained with 50 epochs, batch size of 32, and the Adam optimizer for improved convergence.
- Prediction and Performance Evaluation: The model predicts customer churn on test data and evaluates accuracy, precision, recall, and F1-score using a classification report.


By completing these deliverables, the project team ensures the data is appropriately prepared and analyzed, setting the stage for effective modeling and predicting customer churn.



## Data Preparation and Normalisation

**1. Initial Data Overview:**
 - Displays the structure and summary statistics of the dataset.
 - Helps in understanding the type and spread of data.

**2. Handling Missing Values:**
 - Missing values are handled using forward fill (df.fillna(method='ffill', inplace=True)), ensuring no gaps in data.

**3. Encoding Categorical Variables:**
 - Label encoding converts categorical variables into a numerical format suitable for machine learning models.
 - Sample display of the dataset post encoding shows the successful conversion.

**4. Splitting Data:**
 - The dataset is split into training (80%) and testing (20%) sets using train_test_split.
 - Ensures that the model can be validated on unseen data.

**5. Scaling Data:**
 - StandardScaler normalizes the feature set, standardizing it to have a mean of 0 and a variance of 1.
 - Ensures that features contribute equally to the model performance.
 - The scaled features are displayed to verify normalization.
 - Visual comparison of feature distribution before and after scaling ensures its effectiveness.



## Clustering Analysis

**1. Optimal Number of Clusters:**
 - Elbow Method: The elbow plot indicates the optimal number of clusters (k). We plot SSE (Sum of Squared Errors) for a range of k values. The 'elbow' point, where the SSE begins to level off, suggests the optimal k. Here, k=4 appears to be optimal based on the plot.
 - Visualization: The elbow plot visually demonstrates how the SSE decreases with increasing k, guiding the choice of the optimal number of clusters.

**2. Trained K-Means Model:**
 - Training the Model: The K-Means model is trained using the optimal number of clusters (k=4). The code includes steps for training the model on the scaled data.
 -Saving the Model: The trained model is saved as a file (kmeans_model.pkl) for later use or deployment.

**3. Visualization and Labeling of Clusters:**
 - Adding Cluster Labels: Each data point is assigned a cluster label based on the trained model, and these labels are added to the dataset.
 - Cluster Visualization: The clusters are visualized using a scatter plot of 'tenure' vs. 'MonthlyCharges', colored by cluster labels. This visual representation helps interpret the clustering results, providing insights into the distribution and characteristics of different clusters.

**3.1. Explanation of Visualizations**
 - Elbow Plot: Helps determine the optimal number of clusters by showing where the rate of decrease in SSE slows significantly.
 - Cluster Visualization: Displays how data points are grouped into clusters, aiding in the identification of patterns and insights related to customer churn.



## Predictive Modelling

**1. Defined Architecture of ANN Model:**
- Input Layer: The model is defined with an Input layer that specifies the input shape.
- Hidden Layers: The model includes multiple hidden layers with 64, 32, and 16 units, respectively, using the ReLU activation function.
- Output Layer: The model ends with an output layer using a sigmoid activation function for binary classification (churn prediction).

**2. Trained ANN Model on Provided Dataset:**
- Preprocessing: The dataset is preprocessed by encoding categorical variables and scaling the features.
- Training: The model is trained using the provided dataset with 50 epochs and a batch size of 32. The adam optimizer is used to enhance model convergence and generalization.

**3. Predicted Customer Churn and Evaluated Model Performance:**
- Prediction: The model is used to predict customer churn on the test data.
- Evaluation: The model's performance is evaluated by calculating the accuracy and generating a classification report that includes precision, recall, and F1-score.

*The code achieves the following:*
- Architecture Definition: Specifies the input, hidden, and output layers.
- Model Training: Trains the ANN using robust optimization algorithms.
- Prediction and Evaluation: Predicts customer churn and evaluates the model's performance against the ground truth.
