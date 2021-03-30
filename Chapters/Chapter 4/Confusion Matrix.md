# Confusion Matrix

## Terms
- TP
- FP
- TN
- FN

## Formulae
- Accuracy = (TP + TN) / (TP + TN + FP + FN)
- FP rate = FP / (FP + TN)
- FN rate = FN / (FN + TP)
- TP rate = 1 - FN rate
- Recall = TP / (TP+FN) (also called TPR)
- Precision = TP / (TP+FP)

## ROC Curve

- Plot TPR and FPR values by varying the thresholds.
- The 45 degree line is random classification (think of a coin flip classification)

![[Pasted image 20210323185850.png]]

The AUC or area under curve captures extent of ROC curve. Higher AUC, better model.
