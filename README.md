# American-Express---Default-Prediction
American Express is a globally integrated payments company. The largest payment card issuer in the world, they provide customers with access to products, insights, and experiences that enrich lives and build business success.


# Evaluation
The evaluation metric, M
, for this competition is the mean of two measures of rank ordering: Normalized Gini Coefficient, G
, and default rate captured at 4%, D.

M=0.5⋅(G+D)

The default rate captured at 4% is the percentage of the positive labels (defaults) captured within the highest-ranked 4% of the predictions, and represents a Sensitivity/Recall statistic.

For both of the sub-metrics G and D, the negative labels are given a weight of 20 to adjust for downsampling.

This metric has a maximum value of 1.0.

Python code for calculating this metric can be found in this Notebook.
