# Predicting-customer-emotion
# Goal of the project
- Find the best model for sentiment analysis of customer reviews on Shopee, then apply that model to classify reviews related to product quality (in-domain) or reviews about other aspects (out-domain)
- Propose rating scores for customer reviews, thereby looking more objectively at product quality.
This classification helps improve the accuracy of assessments. Businesses will be able to more clearly identify which elements need to be improved in their sales and service processes, thereby providing timely corrective measures.
# Methodology
![image](https://github.com/ThuyBumr/Predicting-customer-emotion/assets/104961603/e428a75b-4a0a-459c-9d2a-910d93abdfe9)
# 1. Data crawling
- I used Shopee's API to collect data from Shopee with total of 18,392 customer reviews. Each row in the dataset represents a customer review and includes comment ID, product ID, product name, review text, and rating. 
# 2. Data Pre-processing
- Remove empty duplicate comments.
- Create a slang and symbols dictionary
- Normalize and clean text data
- Word segmentation
# 3. Implement and result model
- On each dataset, we trained five models: Naive Bayes, Logistic Regression, Support Vector Machine (SVM), Convolutional Neural Network (CNN), and PhoBERT; then evaluated the models based on the indicators: Accuracy, F1 Score, and Recall. We also used the K-fold technique to increase model accuracy and minimize bias in evaluating model performance due to the effects of random data splitting.
- Experiment results for classifying the review (No word segmentation 
  ![image](https://github.com/ThuyBumr/Predicting-customer-emotion/assets/104961603/c83feaf0-0834-4eea-9b2a-ae4f2a90f2c3)
- Experiment results for classifying the review (Word segmentation)
  ![image](https://github.com/ThuyBumr/Predicting-customer-emotion/assets/104961603/544713b2-fd2a-4b4e-8788-30ce1d675fb7)
- Experiment results for predicting rating scores (No word segmentation)
  ![image](https://github.com/ThuyBumr/Predicting-customer-emotion/assets/104961603/c0621d5b-a25c-44eb-8be6-ca5823d0ef57)
- Experiment results for predicting rating scores (Word segmentation)
- ![image](https://github.com/ThuyBumr/Predicting-customer-emotion/assets/104961603/ed1c1d76-5c9f-4149-bbe4-ce70dd0623ce)

# 4. Conclusion
- The pre-trained PhoBERT model which was fine-tuned by the word segmentation dataset, got the best result with the highest accuracy of 96.29% for the review classification and 75.62% for the rating score prediction.
