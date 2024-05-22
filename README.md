# Intelligent Categorization and Tagging System for Craigslist Computer Listings

## Project Overview

Craigslist, a major platform for classified advertisements, has encountered challenges in accurately categorizing computer and computer parts listings, leading to inefficiencies and a suboptimal user experience. This project aims to address these issues by developing an advanced categorization and tagging system utilizing natural language processing (NLP) and image recognition algorithms to enhance the accuracy and relevance of listings.

## Project Background

Craigslist, a pioneer in online classified advertisements, operates in over 700 cities across 70 countries. The platform's democratized approach allows anyone to post ads, leading to a diverse and vibrant marketplace. However, the computer and computer parts section suffers from misclassification issues, impacting user search efficiency and overall experience.

## Objectives

The primary objective of this project is to develop an intelligent categorization and tagging system that:
- Enhances the accuracy of computer and computer parts listings.
- Improves user experience by providing relevant search results.
- Reduces operational costs by minimizing manual oversight.
- Opens new avenues for monetization through targeted advertising and premium features.

## Data Collection and Preparation

### Data Sources
- **Amazon Dataset**: Used for training and validation, comprising titles, descriptions, and images of computer-related products.
- **Craigslist Data**: Collected from the Chicago area, used for out-of-sample validation to test the model's performance on real Craigslist listings.

### Data Preprocessing
#### Text Data
1. **Cleaning**: Removal of non-alphanumeric characters, punctuation, symbols, and emojis.
2. **Tokenization**: Breaking down text into individual words or terms.
3. **Stopwords Removal**: Eliminating common words with negligible analytical weight.
4. **Stemming**: Truncating words to their root forms.
5. **Lemmatization**: Reducing words to their dictionary form for better semantic representation.
6. **TF-IDF Vectorization**: Transforming text into numerical format to evaluate word importance.

#### Image Data
1. **Reshaping**: Standardizing image size to 64x64 pixels.
2. **Normalization**: Scaling pixel values to a range of 0 to 1.
3. **Color Space Conversion**: Ensuring all images are in RGB color space.

## Methodology

### Text Classification
- **Models Tested**: Random Forest, Logistic Regression, Multinomial Naive Bayes, Support Vector Machine (SVM), Long Short-Term Memory (LSTM) networks.
- **Best Model**: Random Forest with 100 estimators, achieving 81.01% holdout accuracy and 89% test accuracy.

### Image Classification
- **Models Tested**: Random Forest, XGBoost, Convolutional Neural Networks (CNN) using VGG16 architecture.
- **Best Model**: Random Forest with mean CV score of 0.84 and F1 score of 0.831.

## Model Training and Evaluation

- **Holdout Validation**: Using Craigslist data to rigorously test models on unseen data.
- **Merged Classification System**: Combining text and image classification results, with higher probability class assigned as the final class.
- **Performance Metrics**: Accuracy, Precision, Recall, F1 Score.

## Results

- **Final Classification Accuracy**: Misclassification rate reduced to 19.7% on Craigslist test data.
- **Significant Improvement**: Enhanced user experience by ensuring relevant search results, reducing inefficiencies, and potential for new monetization strategies.

## Conclusion

This project successfully developed an intelligent categorization and tagging system for Craigslist's computer listings, leveraging advanced NLP and image recognition techniques. The system significantly improves the accuracy of listings, user experience, and operational efficiency, positioning Craigslist for future growth and competitiveness in the online classifieds market.

## Future Work

- **Enhancing Model Robustness**: Incorporate additional datasets and refine algorithms for better performance.
- **Expanding to Other Categories**: Apply the system to other high-traffic categories on Craigslist.
- **User Feedback Integration**: Continuously improve the system based on user interactions and feedback.
