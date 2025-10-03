Majority voting vs Individual classifiers
- An individual classifier has their own strength and weaknesses.Majority voting  combines the predictions of multiple classifiers and outputs the class that gets the most votes. 
Ensemble often performs better because the errors of different classifiers tend to "cancel out". If a classifier makes a mistake the other ones can correct it. It increases stability and reduces varience.
Ensemble might perform worse if all classifiers are week in the same way. if one model is much stronger it might dilute the performance . the ensembled can be dragged down if there are manny por classifiers. 
Bagging further improves performance by training classifiers on different subsetsof dta, making the ensemble more robust and less prone to over fitting 

AdaBoost Insights
The more estimators the more the ensemble is stable. The performance usually improves at first because averaging over many models smooths out randomness.
Bootstrap sampling means that each base model is trained on a random sample with replacement. This means each model sees a slightly different dataset. Leads to diversity amoung classifiers , which is crucial for ensemble success. 
Bagging reduces overfitting by the decision trees, decision trees are high-varience learners.
Bagging reduces overfitting because it averages out the high variance of single decision trees, producing a more stable and generalizable model.
Learning rate: smaller= slower but better generalization; larger= faster but risk of overfitting.
Error plot: Training error=0, test error may rise again(overfitting)
Decision stumps: ideal weak learners since AdaBoost can boost them into a powerful esemble without overfitting too quickly.

Comparative Performance
On the Iris dataset, Random Forest performed best due to reduced variance and strong handling of feature interaction. random forest extends bagging by adding feature randomness, improving diversity among trees. Bagging is best for reducing variance, boosting is best for reducing bias, and the choice of esemble depends on dtatset size, noise level, and whether you want interpretability or raw predicitive power.


Practical Considerations

Computational trade-offs: Voting is cheapest, bagging/Random Forest are moderate but parallelizable, boosting is slowest due to sequential training. Ensemble size: Larger ensembles reduce variance, but don't reduce bias and eventually give diminishing returns.