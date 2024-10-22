### **Metric**
The metric used is the **micro-average F1 score**, a performance metric used in multi-class or multi-label classification tasks. It combines precision and recall into a single metric that takes into account the class imbalance. Here's how it works:

- ***Precision***: The ratio of true positive predictions to the total number of positive predictions made (true positives + false positives).
- ***Recall***: The ratio of true positive predictions to the total number of actual positive instances (true positives + false negatives).
- ***F1 Score***: The harmonic mean of precision and recall, which balances these two metrics.

**Micro-Averaging:** <br>
When dealing with multiple classes or labels, micro-averaging calculates the metric by summing up the individual true positives, false positives, and false negatives **across all classes**, and then calculating precision and recall from these aggregated counts.

$$
\text{Precision}_{\text{micro}} = \frac{\sum_{c} \text{TP}_c}{\sum_{c} \left( \text{TP}_c + \text{FP}_c \right)}
$$

$$
\text{Recall}_{\text{micro}} = \frac{\sum_{c} \text{TP}_c}{\sum_{c} \left( \text{TP}_c + \text{FN}_c \right)}
$$

$$
\text{F1}_{\text{micro}} = 2 \times \frac{\text{Precision}_{\text{micro}} \times \text{Recall}_{\text{micro}}}{\text{Precision}_{\text{micro}} + \text{Recall}_{\text{micro}}}
$$

### **Benchmark**
A baseline score was obtained by converting the SMILES to Morgan fingerprints and then training a Decision Tree algorithm with the default parameters from scikit-learn. You can reproduce this score by using the introduction notebook associated with the challenge.

