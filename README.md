# Emotions_Dataset_with_NLP
Kaggle Dataset from: https://www.kaggle.com/praveengovi/emotions-dataset-for-nlp

## Aim
The aim of this project is to determine the emotion that is associated with a given body of text. The emotions are the following:

* anger
* fear
* joy
* love
* sadness
* surprise

## Analysis Plan

The plan of the analysis was to examine the accuracy results using the following vectorizers and to determine which produces the best accuracy:

* CountVectorizer: [Emotions Prediction - CountVect.ipynb](Emotions%20Prediction%20-%20CountVect.ipynb)
* Term Frequency (TF) vectorizer (```TfidfVectorizer(use_idf=False)```): [Emotions Prediction - Tf.ipynb](Emotions%20Prediction%20-%20Tf.ipynb)
* TfidfVectorizer: [Emotions Prediction - Tfidf.ipynb]("Emotions%20Prediction%20-%20Tfidf.ipynb")

## Results

| Vectorizer | Test Prediction Accuracy |
|------------|--------------------------|
| CountVectorizer | 0.9654 |
| TF Vectorizer | 0.962 |
| TFIDF Vectorizer | 0.9256 |

## Conclusion

The prediction accuracy, using all vectorizers, was impressive. It appears, however, that using the Inverse Document Frequency (idf) results in a slightly worse prediction accuracy. This reduced performance might be attributable to the fact that stop words and punctuation were removed before vectorization. 

## Further Research

The analysis using the TfidfVectorizer bears repeating, only without the text cleaning and lemmatization to determine whether its performance would be better without the preprocessing of text.