# Natural Language Processing for review prediction
##Training SVM using 1,000 restaurant reviews to predict your review is 'Positive' or 'Negative'
### 1.Introduction
In this project, I trained a linear Support Vector Machine(SVM) to realize reviews prediction, all the reviews ahas been labelled as "Positive" and "Negetive".
### 2. Approach
There are several steps for input sentence preprocessing, first is get rid of every symbol('.','!',etc),and only English Alphabet can stay. Second is lower case every letter and split the every term into seperated string. Final step is filter all stop words. stop words I use is from library of Natural Language Toolkit(NLKT), stop words will download automatically when this script runinning.

And then I will creat my the Bags of Words model, I resized my model into 1500 features, algebraic operations can be speed up by clearing zero values in the matrix.

### 3.Training model
Training model I use is linear SVM which imported from SciKit Learn(sklearn) Library. My configuration is 20% for testing use and 80% for training use.

### 4. Result
In all these 200 test cases, SVM output 74 correct negetive reviews and 70 positive reviews, 23 wrong negetive reviews and 33 wrong negetive reviews. Overall, the total accuracy is 72%

I also build in the function which can make user input there own words. Here are some examples:
```
python natural_language_processing.py 'Good food and quick service, never disappoints'
Positive
```
```
python natural_language_processing.py 'THIS PLACE IS A MUST AVOID! They charge insane prices for food made with no love'
Negetive
```
Enjoy trying your own words!
