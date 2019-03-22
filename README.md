# About this project

# logbook 

Making progress on doing classification of the abstracs using Spacy and SciScpay

Now might look at bjuilding a classification model, looking at
https://www.kaggle.com/nujcharee/classification-with-spacy

Also have a look at these videos

https://www.youtube.com/watch?v=COuebh25Fb8  
https://www.youtube.com/watch?v=5di0KlKl0fE
https://www.youtube.com/watch?v=cgwDB1THUBY&list=PLJ39kWiJXSiz1LK8d_fyxb7FTn4mBYOsD
https://www.youtube.com/watch?v=4l_At3oalzk
https://www.youtube.com/watch?v=nxhCyeRR75Q

Should use https://spacy.io/api/textcategorizer 

see also https://github.com/explosion/spaCy/blob/361554f629a6938176cfddbcce368e5d94064ab5/examples/training/train_textcat.py#L58-L74 

probably the best option is to try to use prodigy to create an inital training set:
https://medium.com/@david.campion/text-classification-be-lazy-use-prodigy-b0f9d00e9495

Could try to
- do an initial prodigy run using the raw abstract data, and then try putting in some test abstracts to get scores
- create a model using "cleaned" data, pass the test abstracts in after cleaning them

This looks useful for a discusison on using prodigy:
https://support.prodi.gy/t/prodigy-to-spacy-guide/857/2

I am not 100% sure that what I am doing here is correct, see https://prodi.gy/docs/workflow-first-steps for more discusison on prodigy

# background info

This is for trying to extract abstrats and train a model based on the abstracts.

We have a couple of options to explore:

- scikit-learn   
- spacy  
- prodigy  
- AWS SAGE maker 

Things that we couold look at delivering on:

- how can we create a bi-modal calssifier based on the abstracts, do we need to do feature cleaning of the abstract text to start with?  
- can we create a training job in SAGE Maker to make it easy to classify inbound abstracts  
- could we create a workflow where the inbound abstracts are weighted by our initial model and we present only the edge cases to the SRM team? 
- once we have a model created how might we create an API endpoint that could be integrated into a document processing workflow 

The key blocker is understanding how to create an inital model based on the training data that we have. 
An easy thing to possibly make progress on is creating a training job in SAGE maker and a training job in prodigy 

Some blogs that look useful for this:

Comprehensive overview of text classificaiotn with sklearn 
https://www.analyticsvidhya.com/blog/2018/04/a-comprehensive-guide-to-understand-and-implement-text-classification-in-python/  

experiment with named entity recognition with spacy
https://www.kaggle.com/thebrownviking20/topic-modelling-with-spacy-and-scikit-learn  
https://www.kaggle.com/nirant/hitchhiker-s-guide-to-nlp-in-spacy


Other resources

Multi-Class Text Classification with Scikit-Learn - good overview 
https://towardsdatascience.com/multi-class-text-classification-with-scikit-learn-12f1e60e0a9f  
https://towardsdatascience.com/machine-learning-for-text-classification-using-spacy-in-python-b276b4051a49 
https://github.com/susanli2016/Machine-Learning-with-Python/blob/master/machine%20learning%20spaCy.ipynb


really good intro to SAGE Maker 
https://www.bmc.com/blogs/amazon-sagemaker/

Text classifier with SpacY
https://spacy.io/usage/training

Binary classification model with Amazon Machine Learning and redshift 
https://aws.amazon.com/blogs/big-data/building-a-binary-classification-model-with-amazon-machine-learning-and-amazon-redshift/  


AWS Sage Maker examples 
https://github.com/awslabs/amazon-sagemaker-examples  

Another nice general Spacy tutorial
https://nlpforhackers.io/complete-guide-to-spacy/  

