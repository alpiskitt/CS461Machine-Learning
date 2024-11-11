# CS461Machine Learning Homework 1 README


# Classification on Amazon Reviews

## Overview
This project involves sentiment classification of Amazon reviews using Multinomial and Bernoulli Naive Bayes models. The code includes additive smoothing (Dirichlet prior) options and handles zero-probability cases in log computations. Additionally, total of three models have been used to provide further testing and evaluation of the models. The Project shows the accuracies and options for naive bayes models.

## Models Used
### Multinomial Naive Bayes Model
The Multinomial Naive Bayes model is used for text classification, where the features are the frequencies of words in the text. This model is generaly used for problems where the data represents counts or frequency of occurrences, such as word counts in document classification. In this project, the Multinomial Naive Bayes model helps classify the sentiment of Amazon reviews based on the frequency of specific terms.

### Bernoulli Naive Bayes Model
The Bernoulli Naive Bayes model is another variant that is suited for binary/boolean features. Instead of considering the frequency of words, this model focuses on whether a word is present or absent in a document. In this project, the Bernoulli Naive Bayes model is used to classify Amazon reviews by considering the presence of important terms in the text. This model can be effective when the focus is on the occurrence of specific words rather than their frequency.

Both models are evaluated with different configurations, including additive smoothing (using the Dirichlet prior) and adjustments for handling zero probabilities. These models provide insights into the impact of different feature representations and assumptions on the overall sentiment classification performance.

## Requirements
- Python 3.x
- Required libraries: `matplotlib`, `pandas`, `numpy`, `seaborn`

To install the required libraries, run:
```bash
pip install -r requirements.txt
```

Ensure the data files (`x_train.csv`, `y_train.csv`, `x_test.csv`, `y_test.csv`) are in the same directory as `q2main.py`.

## Default Parameters
- **alpha** (Dirichlet prior α): Set to 1 for additive smoothing; set to 0 otherwise.
- **Small log assumption**: Default value is set to `-np.inf` to replace zero probabilities in the computations.

## Running the Code
To execute the program, run the following terminal command:
```bash
python q2main.py --alpha 1
```
This command runs the sentiment classification using additive smoothing and a small log assumption for zero probabilities. You can adjust the `alpha` value to modify the model's behavior.

## Troubleshooting Tips
- Ensure the data files (`x_train.csv`, `y_train.csv`, `x_test.csv`, `y_test.csv`) are in the same directory as `q2main.py`.
- Check that the required Python version and libraries are installed.

## Outputs
- **Model Accuracy: Displays accuracy scores for different models to three decimal places.
- **Confusion Matrices: Visualizes and prints confusion matrices for model comparisons in the terminal and in plots.
- **output example:

  ```
          Train Percentages  Test Percentages
Positive          36.913043         35.857143
Neutral           33.130435         34.000000
Negative          29.956522         30.142857
Count of 'good' in Positive Class: 207
Count of 'bad' in Positive Class: 12
Log Probability of 'Good' Given Positive Sentiment: -4.29
Log Probability of 'Bad' Given Positive Sentiment: -7.14
Accuracy without small log assumption: 0.301
Accuracy with Dirichlet prior: 0.649
Accuracy with Bernoulli Naive Bayes: 0.641
  ```

## Additional Notes
- The program automatically generates and displays related graphs to visualize results.
- For each example, different combinations of `alpha` can be used to evaluate the models effectively.

