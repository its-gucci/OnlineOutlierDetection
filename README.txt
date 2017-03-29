------------------------
Online outlier detection
------------------------

Sample code that trains a model over time. We do this
by initially using OneClassSVM to train the data and 
then use this to train a linear classifier that has been
transformed. We then use sklearn's partial_fit method
to train it online on subsequent datasets, with the rule
that if it's mostly outliers we throw it away and otherwise
we update the model.