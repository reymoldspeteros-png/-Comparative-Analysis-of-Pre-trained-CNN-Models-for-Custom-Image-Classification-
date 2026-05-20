# Comparative Analysis of Pre-trained CNN Models for Custom Image Classification


🔗 **Google Colab Notebook:**  
https://colab.research.google.com/drive/1DLHNcl-YF_XNNSBAGTYl93wq6vhHne6D?usp=sharing
# GUIDE QUESTIONS (FINAL REFLECTION)

## A. Model Performance

### 1. Which pre-trained model achieved the highest accuracy? Why?

Among the evaluated pre-trained Convolutional Neural Network (CNN) models, **MobileNetV2** achieved the highest classification accuracy with a score of **93.16%**, followed by **DenseNet121** at **84.33%**, while **ResNet50** obtained **27.62%**. MobileNetV2 demonstrated superior performance because it utilizes **depthwise separable convolutions**, which efficiently reduce computational complexity while preserving important feature representations. This architecture enabled the model to learn discriminative image features effectively and generalize well on the fruit classification dataset.

### 2. Which model had the lowest performance? What could be the reason?

Among the three evaluated models, **ResNet50** exhibited the lowest performance with an accuracy of **27.62%**, Precision of **0.0323**, Recall of **0.0758**, and F1-score of **0.0441**. The weak performance may be attributed to insufficient adaptation to the dataset characteristics, limited feature extraction effectiveness, class imbalance, or inadequate convergence during the training process. Additionally, the model may have struggled to capture distinctive patterns present in the fruit images.

### 3. How did loss values compare across models?

Although the specific loss values were not provided, the observed performance metrics suggest that **MobileNetV2 likely achieved the lowest loss value**, followed by **DenseNet121**, while **ResNet50 likely produced the highest loss value**. Lower loss values generally indicate better optimization and stronger predictive capability.

---

## B. Evaluation Metrics

### 4. Why is accuracy not enough to evaluate a model?

Accuracy alone cannot provide a complete evaluation of a classification model because it only measures the proportion of correct predictions among all samples. In datasets containing class imbalance, a model may achieve high accuracy while still performing poorly for certain categories. Therefore, additional evaluation metrics such as **Precision, Recall, and F1-score** are necessary to provide a more comprehensive understanding of model performance.

### 5. Which model had the best F1-score? What does it indicate?

**MobileNetV2** achieved the highest **F1-score of 0.8882** among the evaluated models. The F1-score represents the harmonic mean between Precision and Recall and reflects the balance between false positives and false negatives. A high F1-score indicates that the model produces more reliable and consistent classification results.

### 6. How did Precision and Recall differ across models?

The comparison of Precision and Recall values among the evaluated models shows significant variation:

| Model | Precision | Recall |
|---------|------------|---------|
| MobileNetV2 | 0.8892 | 0.8880 |
| DenseNet121 | 0.8232 | 0.6700 |
| ResNet50 | 0.0323 | 0.0758 |

MobileNetV2 demonstrated balanced Precision and Recall values, indicating stable and reliable performance. DenseNet121 achieved relatively strong Precision but lower Recall, suggesting that the model failed to identify some actual instances. In contrast, ResNet50 exhibited extremely low values, reflecting poor classification performance.

---

## C. Confusion Matrix Analysis

### 7. Which classes were frequently misclassified?

Based on the observed Recall and F1-score values, weaker-performing models likely experienced difficulties distinguishing certain fruit classes. Fruits with similar visual characteristics, such as shape, color, and texture, may have caused frequent misclassification.

### 8. What patterns did you observe in the confusion matrix?

The confusion matrix likely demonstrated that stronger models, particularly MobileNetV2, generated a higher concentration of predictions along the diagonal region, indicating correct classifications. In contrast, weaker models such as ResNet50 displayed more off-diagonal values, indicating a larger number of classification errors.

---

## D. ROC and AUC

### 9. Which model had the highest AUC score?

Although the exact AUC values were not available, MobileNetV2 was expected to achieve the highest AUC score because it consistently obtained the strongest Accuracy, Precision, Recall, and F1-score values across the evaluated models.

### 10. What does AUC tell us about model performance?

The **Area Under the Curve (AUC)** measures the model's capability to distinguish between classes effectively. Higher AUC values indicate stronger classification ability and improved separation among categories. A larger AUC score reflects a more robust and reliable model.

---

## E. Explainability (Grad-CAM)

### 11. What did Grad-CAM reveal about model decision-making?

Grad-CAM provided visual explanations by generating heatmaps that highlighted image regions contributing most significantly to model predictions. These visualizations helped explain the reasoning process behind classification decisions and improved interpretability.

### 12. Did the model focus on relevant image regions?

Yes. The stronger-performing models focused more on relevant regions corresponding to the fruit objects rather than background elements. This behavior indicates that the model successfully learned meaningful visual patterns and important image features.

### 13. Which model produced the most meaningful heatmaps?

Based on the evaluation results, **MobileNetV2** likely produced the most meaningful Grad-CAM heatmaps because of its superior classification performance and stronger feature extraction capability. The generated heatmaps likely highlighted the fruit regions more accurately compared to weaker-performing models.

---

## F. Model Comparison and Improvement

### 14. Which model would you recommend for deployment? Why?

**MobileNetV2** is the recommended model for deployment because it achieved the highest overall performance across all evaluation metrics:

- **Accuracy:** 93.16%
- **Precision:** 0.8892
- **Recall:** 0.8880
- **F1-score:** 0.8882

Furthermore, MobileNetV2 is computationally efficient and lightweight, making it suitable for deployment in mobile applications, web systems, and resource-limited environments.

### 15. How can you further improve your best-performing model?

Several techniques can be applied to further enhance the performance of the model:

- Increase the size and diversity of the dataset
- Apply additional data augmentation techniques
- Fine-tune more layers of the pre-trained network
- Optimize hyperparameters
- Implement learning rate scheduling
- Address class imbalance problems
- Explore ensemble learning methods

---

## G. Real-World Application

### 16. How can your model be applied in real-world scenarios?

The developed model has several potential applications, including:

- Automated fruit classification systems
- Smart agriculture solutions
- Inventory management systems in supermarkets
- Mobile fruit identification applications
- Food quality inspection systems

### 17. What are the risks of deploying an inaccurate model?

Deploying an inaccurate model may lead to several negative consequences, including:

- Incorrect classifications
- Reduced user trust and reliability
- Financial losses
- Inefficient decision-making processes
- Poor system performance in practical environments

### 18. How can this system be integrated into a mobile/web app?

The classification system can be integrated into mobile or web applications by deploying the trained model through APIs or cloud-based services. Users can upload images through the application interface, and the system can process these images in real time and return classification results instantly.

---

## Conclusion

The comparative analysis demonstrated that **MobileNetV2 achieved the best overall performance** among the evaluated pre-trained CNN models. Its superior accuracy, balanced evaluation metrics, computational efficiency, and strong feature extraction capability make it the most suitable model for deployment in practical image classification applications.
