All of the algorithms are performed using the software Weka.

Datasets/result files are located at this link:

https://github.com/MLord8/ML/assignment1

Given a .arff file (e.g., spambase.arff), we need to split it into testing and training data, and then we need to split the training data into 10, 20, 30, ... , 90 percent files for analysis of the algorithms compared to the training set size. 

To randomize the data, select Filter > Unsupervised > instance > randomize.

To split the data into our testing and training sets, select
Filter > Unsupervised > Remove Percentage > 30%
This removes 30% of the data. Save this as spambase-train.arff (or whatever your data is)

To get the rest of the data as our test set, do Undo, then Invert.
Save this as spambase-test.arff (or whatever your dataset is)

Load up the spambase-train.arff. Using similar steps as just described, split the training set into 10%, 20%, ... , 90% files using the Filter > Unsupervised > Remove Percentage > x%.

Now we have all of our necessary files to begin running the algorithms.

A) Decision tree
- For decision trees, go to Classify > Choose > Weka > Classifiers > Tress > J48.
- Ensure the minimum instances per leaf is 2.
- Select "Use training set", then Start. Different data about the algorithm run will be displayed once the model is created.
- Set the supplied test set as spambase-test.arff (or your data, yadayada)
- Right click that run in the result list and select "Re-evaluate model on current test set." This gives the result of the test dataset on that model.
- Choose cross-validation with Folds = 10, and Start. Different data about the algorithm run will be displayed once the model is created.

- Do this for varying values of confidence factor.
- Once the optimum value of the hyperparameter is found, load each of the 10%, 20%, ... , 90% training files and run the algorithm.

The rest of the algorithms follow generally the same steps as this, so I will instead outline which hyperparameters to alter

B) Neural Network
	- multilayer perceptron function
	- vary training time (# epochs)
	- vary nodes per hidden layer
	- accuracy vs training set size for testing/training sets 

C) AdaBoost
	- AdaBoostM1 w J48 implementation
	- vary cf and # iterations
	- accuracy vs training set size
	- 

D) SVM
	- SMO w Poly kernel
	- Exponent 1, 2, 3
	- accuracy vs training set size
	- SMO w RBF kernel
	- Gamma of 0.01, .1, 1
	- accuracy vs training set size

E) kNN
	- IBK algo
	- unweighted on different values of k
	- weighted 1/distance on different values of k
	- accuracy vs training set size