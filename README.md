# Ensemble Learning on MNIST Dataset (database of handwritten digits)

This project demonstrates the application of ensemble learning techniques on the MNIST dataset. The goal is to classify handwritten digits by training several models and combining their predictions.

## Overview

The project involves the following steps:

1. **Data Preparation**: The MNIST dataset is loaded and split into a training set, a validation set, and a test set.

2. **Training Individual Classifiers**: Four different classifiers (Random Forest, Extra Trees, SVM, and MLP) are trained on the training set.

3. **Creating a Voting Classifier**: The individual classifiers are combined into a voting classifier, which makes its final prediction based on the majority vote of the individual classifiers.

4. **Evaluating the Models**: The performance of the individual classifiers and the voting classifier is evaluated on the validation set and the test set.

5. **Improving the Voting Classifier**: The SVM classifier is removed from the voting classifier to improve its performance.

6. **Creating a Blender**: A blender is trained to make a final prediction based on the predictions of the individual classifiers.

7. **Creating a Stacking Classifier**: A stacking classifier is created using the `sklearn` library, which automatically trains the base classifiers and the blender.

8. **Comparing the Models**: The performance of the blender, the stacking classifier, and the voting classifier is compared.

## Key Findings

- The stacking classifier achieved the highest accuracy on the test set, indicating that it was able to combine the base classifiers' predictions more effectively than the voting classifier or the blender.

- The performance of the voting classifier improved when the SVM classifier was removed from the ensemble. This suggests that the quality and diversity of the individual classifiers are important factors in the performance of an ensemble method.

- The blender performed worse than the voting classifier, possibly due to the quality of the individual predictions, the complexity of the blender, or the diversity of the errors made by the individual classifiers.

## Conclusion

This project demonstrates the power of ensemble methods in machine learning. By combining several models, we can often achieve higher accuracy and better generalization than any individual model. However, the best method to use in practice depends on the specific dataset and models used. It's always a good idea to try different methods and choose the one that performs best on the validation set.
