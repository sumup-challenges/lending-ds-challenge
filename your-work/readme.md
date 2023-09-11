# Overview of Model Development Journey

Our journey towards credit default prediction was meticulously planned and executed, commencing with a rigorous data cleaning process. Subsequently, we applied binary encoding through pd.dummies to ensure our data was represented as one-hot encoding.

We delved into the descriptive statistics of our dataset, conducting an extensive exploration of its features. This encompassed evaluating class distributions within features and features concerning our target variable to comprehend their behavior. During this exploration, we identified a column with potential adverse impact on model performance, irrespective of its nature.

Recognizing the imbalance in class distribution, with 0-GOOD being the majority class, it became evident that this imbalance needed addressing. To tackle this issue, we implemented resampling within the training set, ensuring the proper separation of training and test sets—a pivotal aspect for model integrity.

Our model evaluation encompassed an analysis of four classification algorithms, with cross-validation performed on both the original and resampled balanced datasets. The Random Forest model, trained on the balanced data, emerged as the victor, grounded in critical metrics such as precision, recall, and area under the ROC curve.

However, a deeper investigation uncovered the presence of overfitting within the training data, hampering the model's generalization capability on the test set, especially concerning the identification of bad credit (1 BAD). To mitigate overfitting, we executed hyperparameter optimization using K-fold cross-validation and random search CV.

This optimization yielded a more precise and balanced model, proficient in effectively classifying the bad credit class. This outcome successfully met our objectives, enabling more accurate identification of risky credits, thereby safeguarding the financial institution and its Basel Index.

Lastly, we showcased the significance of each feature through corresponding plots, culminating in a comprehensive summary of our model development process.
