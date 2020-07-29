# supervised_machine_learning_credit_risk

The challenge's objective is to determine which model, if any, best predicts the status of a loan (high risk, low risk).

## Naive Random Sampling (NRS)

The balanced accuracy score for the NRS model is about 0.50580. About half the time, the model can accurately predict loan status. The model's precision for both high and low-risk loans is perfect, i.e., 1.00. However, while the sensitivity is ideal for low_risk loans, the model has almost no chance at identifying a high-risk loan if the loan was indeed high risk; the sensitivity for high-risk loans was 0.01.

## Synthetic Minority Oversampling Technique (SMOTE) Oversampling

The balanced accuracy score for the SMOTE model is about 0.62620, a small improvement over the NRS model. The precision for low-risk loans is perfect, while high-risk loans had a precision of 0.01. Sensitivity was 0.64 and 0.61 for high and low-risk loans, respectively. While the model is better at flagging all the high-risk loans, if given a loan flagged as high risk, it is likely not to be high risk.

## Undersampling

The undersampling model had an accuracy of about 0.51582. Precision was perfect for low-risk loans, but only 0.01 for high-risk ones. The sensitivity for high-risk loans was 0.63 and 0.40 for low-risk loans. This model was mediocre at flagging all the high-risk loans, but any given loan labeled high risk had a low chance of being high risk.

## Over and Under Sampling

This last model had perfect precision for low-risk loans, but only a precision of 0.01 for high-risk loans. The sensitivity for high-risk loans was 0.72 and for low-risk loans, 0.57. The model was somewhat good at flagging all high-risk loans, but one could not be confident about any one loan flagged as high risk. This model, being more aggressive, missed half of the total of low-risk loans, but for any given low-risk loan, one could be confident it was low risk.

## Recommendation

The over and under sampling model is the best in this exercise because the lender should want to avoid almost all false negatives. The model is aggressive enough at flagging high-risk loans out of all the high-risk loans in the sample. While not as good as the other models at identifying low-risk loans, the lender might have high-interest rates for those who are indeed at low risk of defaulting. High interest rates and hedging can mitigate any deficiencies in flagging high-risk loans.
