# XAI_Techniques
Explainable AI Techniques for Interpreting Machine Learning Models - This project aims to demonstrate the application of various Explainable AI (XAI) techniques to interpret the predictions of a RandomForestClassifier trained on the Iris dataset. The techniques used include LIME, Anchors, SHAP, and ICE Plots.

1. LIME 🍋 (Local Interpretable Model-Agnostic Explanations):
Generates explanations for individual predictions by perturbing input data and observing the model's behavior.
Produces a human-interpretable local model approximation.
2. Anchors ⚓️:
Creates if-then rules (anchors) to explain individual predictions.
Ensures high precision and clarity in explanations for tabular data.
3. SHAP 🎲 (SHapley Additive exPlanations):
Distributes the output among features based on their contribution.
Offers visualization tools for interpreting predictions both locally and globally.
4. ICE Plots 🧊 (Individual Conditional Expectation):
Shows the effect of a feature on the predicted outcome for each instance.
Complements global model understanding by visualizing individual feature effects.

Dataset:
The Iris dataset, which contains measurements of iris flowers (sepal length, sepal width, petal length, petal width), is used for this project. The dataset is split into training and testing sets to train the model and evaluate the XAI techniques.

Model:
A RandomForestClassifier is trained on the training data to predict the species of iris flowers based on the measurements.

XAI Techniques:

    LIME: Explains the prediction of an instance by approximating the model locally with an interpretable model.
    Anchors: Provides rule-based explanations for individual predictions.
    SHAP: Explains the output of the model by assigning each feature an importance value for a particular prediction.
    ICE Plots: Show the dependence of the prediction on a feature for each instance.

Code Explanation

This code demonstrates the use of various Explainable AI (XAI) techniques to interpret the predictions of a RandomForestClassifier trained on the Iris dataset. Here's a brief overview of each section:

    Loading and Splitting the Dataset:
        The Iris dataset is loaded and split into training and testing sets.

    Training the Model:
        A RandomForestClassifier is trained on the training data.

    Defining the Prediction Function:
        A prediction function is defined to be used by the explainers.

    LIME (Local Interpretable Model-agnostic Explanations):
        LIME explains the prediction of an instance by approximating the model locally with an interpretable model.
        The explanation is visualized in a notebook.

    Anchors:
        Anchors provide rule-based explanations for individual predictions.
        The AnchorTabular explainer is initialized, fitted on the training data, and used to explain a test instance.

    SHAP (SHapley Additive exPlanations):
        SHAP values explain the output of the model by assigning each feature an importance value for a particular prediction.
        A summary plot of SHAP values is generated to visualize the feature importances.

    ICE (Individual Conditional Expectation) Plots:
        ICE plots show the dependence of the prediction on a feature for each instance.
        Partial Dependence Plots (PDPs) are generated for the first two features (sepal length and sepal width) to visualize their effect on the target prediction.
        
Explanation of the Outputs and Code
Outputs

    Partial Dependence Plots (PDPs):
        These plots show the relationship between the target function and a set of features of interest, marginalizing over the values of all other features.
        The left plot shows the partial dependence of the target on sepal length (cm). It indicates how the predicted probability changes as sepal length varies.
        The right plot shows the partial dependence of the target on sepal width (cm). It indicates how the predicted probability changes as sepal width varies.

    SHAP Interaction Values:
        SHAP (SHapley Additive exPlanations) values explain the output of the machine learning model.
        The plot shows the interaction values between different features. Each dot represents an instance, and the color represents the value of the feature on the y-axis.
        The x-axis shows the SHAP interaction value, indicating how much the interaction between the features contributes to the prediction.

    Prediction Probabilities:
        The model predicts the probabilities for each class (setosa, versicolor, virginica).
        For the given instance, the probabilities are 0.00 for setosa, 0.98 for versicolor, and 0.02 for virginica.
        The model predicts the class versicolor with high confidence.

    Anchor Explanation:
        Anchors provide rule-based explanations for individual predictions.
        The anchor explanation for the given instance is:
            1.50 < petal length (cm) <= 5.10
            sepal width (cm) <= 2.80
            0.30 < petal width (cm) <= 1.30
            sepal length (cm) <= 6.40
        These rules describe the conditions under which the prediction is likely to be versicolor.



Results:

    LIME: Visualizes the local explanation of a test instance.
    Anchors: Provides a rule-based explanation for a test instance.
    SHAP: Generates a summary plot of feature importances.
    ICE Plots: Visualizes the partial dependence of the target on the first two features.

Conclusion:
The XAI techniques provide valuable insights into the predictions of the RandomForestClassifier, enhancing the interpretability and trustworthiness of the model.


