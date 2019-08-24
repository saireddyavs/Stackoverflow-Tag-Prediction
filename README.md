# Stack-Overflow Tag Prediction

Suggest the tags based on the content that was there in the question posted on Stackoverflow.

for libraries :

`pip install -r /path/to/requirements.txt`


`It is any Multilabel-Classification Problem`

Data set size:6.75GB
Number of Rows:6034195

## Data Field Explaination

Dataset contains 6,034,195 rows. The columns in the table are:

Id - Unique identifier for each question

Title - The question's title

Body - The body of the question

Tags - The tags associated with the question in a space-seperated format (all lowercase, should not contain tabs '\t' or ampersands '&')


### It is a multi-label classification problem
**Multi-label Classification:** Multilabel classification assigns to each sample a set of target labels. This can be thought as predicting properties of a data-point that are not mutually exclusive, such as topics that are relevant for a document. A question on Stackoverflow might be about any of C, Pointers, FileIO and/or memory-management at the same time or none of these.
[more Explaination]( http://scikit-learn.org/stable/modules/multiclass.html)

### Performance metric

**Micro-Averaged F1-Score (Mean F Score) :** The F1 score can be interpreted as a weighted average of the precision and recall, where an F1 score reaches its best value at 1 and worst score at 0. The relative contribution of precision and recall to the F1 score are equal. The formula for the F1 score is:

F1 = 2 * (precision * recall) / (precision + recall)

In the multi-class and multi-label case, this is the weighted average of the F1 score of each class.

**Micro f1 score:**
Calculate metrics globally by counting the total true positives, false negatives and false positives. This is a better metric when we have class imbalance.



**Macro f1 score:**
Calculate metrics for each label, and find their unweighted mean. This does not take label imbalance into account.

[Mean F1-Score](https://www.kaggle.com/wiki/MeanFScore)



**Hamming loss :** The Hamming loss is the fraction of labels that are incorrectly predicted.

[Hamming Loss](https://www.kaggle.com/wiki/HammingLoss)
