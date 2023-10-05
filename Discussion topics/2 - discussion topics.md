# Discussion topics part 2

## The AWS-lesson

1. Is it a good idea to be using Python and Jupyter notebooks? Are there any alternatives like Julia, R, Java, C#, …? A: Yes, Python and Jupyter notebooks are commonly used on AWS for data analysis and machine learning. While there are alternatives like R and Scala, Python's ecosystem and Jupyter's interactive capabilities make them well-suited for AWS cloud computing.
2. Amazon has some managed services that provide AI-services without the need for any real understanding of the technology involved. Will they preform better than a model that we can make ourselves? What are the [dis]advantages of using them? 
A: Using AI services from Amazon or other providers can be beneficial for ease of use, but whether they perform better than a custom-built model depends on your specific needs: 
Advantages:

Easy to use.
Scalable.
Pre-trained models available.

Disadvantages:

May not fit unique requirements.
Less understanding of underlying technology.

    ![](files/2023-04-11-18-35-30.png)

3. Give an example of supervised and unsupervised learning when using a file with all data about students (grades, but also age, shoe size, family situation, …).
A: Supervised Learning Example: Predicting student grades (A, B, C, etc.) based on features like age, family situation, and shoe size using a labeled dataset where past student grades are known.

Unsupervised Learning Example: Clustering students into groups based on similarities in their age, family situation, and shoe size, without any prior labels or grade information.

Supervised learning uses labeled data to make predictions, while unsupervised learning finds patterns and structures in unlabeled data.
4. We have a file of student grades and how much they studied for a test. We want to predict their test scores. Explain the difference between binary classification, multi-label classification and regression in this context.
A: Binary classification: 0 or 1, failed or passed. Predicts wether a student passed or failed nothing else.
Multi label classification: Would predict multiple categories like "A", "B" ... and "failed" for example.
Regression: this would predict the actual test scores based on number of study hours and is a continuous prediction.
5. Can we use AI to do feature engineering? Is it regularly done this way?
A: In summary, while AI can assist with feature engineering by automating certain aspects of the process, it is still important to combine human expertise with automated techniques to ensure effective feature selection and transformation. The specific approach to feature engineering may vary depending on the problem at hand and the characteristics of the dataset.
6. Explain over- and underfitting in the context of multi-label classification.
A: Overfitting occurs when a model is too complex and fits the training data too closely, resulting in poor generalization to new data. In the context of multi-label classification, overfitting can occur when a model is too complex and tries to fit the training data too closely, resulting in poor performance on new data. Overfitting can be caused by several factors, such as using too many features or having too many parameters in the model.

Underfitting, on the other hand, occurs when a model is too simple and is unable to capture the underlying patterns in the data. In the context of multi-label classification, underfitting can occur when a model is too simple and fails to capture the complex relationships between the input features and output labels. Underfitting can be caused by several factors, such as using too few features or having too few parameters in the model


## The powerpoint and exercises

1. The powerpoint states: "The model should generalize to unseen data if you are using it to predict. If it’s just to explain the data overfitting isn’t a problem." Explain!
A: If it just needs to explain the data but doesn't need to generalize to use it to predict data overfitting is not a concern because it is only a concern with generalizing of data to predict data.
1. To get rid of outliers, we simply look at the values and delete the row with the highest value for every column. Or is there a better way? A: while deleting the row with the highest value for every column may work in some cases, it is not a reliable or recommended method for removing outliers. Instead, it’s better to use statistical methods such as IQR or z-scores to identify and remove outliers from your dataset.
1. Why does the Z-score not matter in a column that is used in one hot encoding? A: Z-scores are not relevant in one-hot encoding because it's used for categorical data, and Z-scores are for continuous numerical data.
1. What is scaling/normalization of data?
A: Scaling/Normalization of data is the process of adjusting the range of values in your dataset to a common scale, typically between 0 and 1, to ensure that all features contribute equally to data analysis or modeling.




