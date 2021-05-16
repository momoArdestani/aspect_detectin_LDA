# aspect_based sentiment DSS

<br/>
0) Introduction and purpose<br/>
0.1) Setups and input, output format and data frame clarification<br/>
	0.2) Purposes <br/>
<br/>
Part 1) Preprocessing the data and preparing it<br/>
	1.1) cleaning Data<br/>
	1.2) vectorizing <br/>
<br/>
Part 2) Phase One ( Finding Sentiments)  <br/>
	2.1) Unsupervised approach with “textblob” library<br/>
		2.1.1) Estimating Sentiments<br/>
		2.1.2) Extrapolating ratings <br/>
<br/>
<br/>
part 3) Phase Two ( Extracting Topics or Aspects)<br/>
	3.0) Training LDA model <br/>
	3.1) Finding soft/fuzzy clustering of words <br/>
	3.2) Finding words distribution for each Topic<br/>
	3.3) Finding Topics-distribution for each document<br/>
<br/>
part 4) Evaluations and visualizations <br/>
	4.1) visualizing topic-sentiment graph of corpus <br/>
	4.2) Evaluating and visualizing LDA method<br/>
	4.3)  Evaluating and visualizing “textblob” method
<br/>

----------------------

1. (Part 1) Preprocessing the data and preparing it
	1. cleaning data: We go through following steps:
		1.	removing user names
		2.	removing numbers
		3.	removing URLs
		4.	removing punctuations
		5.	removing stopwords
		6.	removing words with length less than 3
		7.	transform to the lower case
		8.	stemming
	2) vectorizing
2. (Phase One) Finding Sentiments (textblob approach)
[pic]
In a nut shell, TextBlob library has unsupervised methods for finding polarity and subjectivity (and etc) of a text. A lot of linguists, namely Tom De Smedt, have come together and have figured out all different aspect of words manually. Based on this great job that has done recently, we are able to estimate polarity (means sentiment score that is between -1 and +1) even better than KNN or Bayes which have expensive calculation. In our case, we have reached 0.799 percent accuracy for estimating polarity (sentiment) of reviews. We will explain this in “Evaluation of TextBlob” part.(More info about textblob for interested reader, perhaps you!, : link1 , link2) <br/>
Estimating Sentiments:<br/>

We help of polarity function we can easily find sentiment score and map it to {Pos , Neg , Neu}.<br/>
Extrapolating ratings: <br/>
For finding ratings we need to extrapolate them with respect to current behavior of users. For this purpose, beside defining a linear map from sentiment score to {1,2,3,4,5}, we define a non-linear function that is trained by ratings distribution of the reviews in data set. <br/>

3. three
4. eval 
