# Midterm Project: Classification Analysis

> Submission: GitHub Repository with Jupyter Notebook and Peer Review

---

## Overview
Organizations frequently need to classify data to support decision-making. 
For example, a healthcare provider may want to predict whether a patient has a specific condition based on lab results,
or a business may classify customer behavior to tailor marketing strategies.
Machine learning classification models help automate these decisions by recognizing patterns in historical data.

This project demonstrates your ability to apply classification modeling techniques to a real-world dataset. You will:
- Load and explore a dataset.
- Analyze feature distributions and consider feature selection.
- Train and evaluate a classification model.
- Compare different classification approaches.
- Document your work in a structured Jupyter Notebook.
- Conduct a peer review of a classmate’s project.

---

## Dataset Options
Select one dataset from the list below. If you get good results, you can try the process on a suitable dataset of your own. 
A suitable dataset for classification includes:
- Categorical or numerical features that help predict the target.
- A **categorical target variable** for classification (binary or multiclass).
- Enough samples per class to effectively train and test a model.

1. **Mushroom Classification Dataset** (Predict whether a mushroom is edible or poisonous based on characteristics)
   - [UCI Mushroom Dataset](https://archive.ics.uci.edu/ml/datasets/mushroom)
2. **Titanic Survival Dataset** (Predict whether a passenger survived the Titanic disaster)
   - [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic/data)
3. **Banknote Authentication Dataset** (Predict whether a banknote is authentic based on wavelet-transformed images)
   - [UCI Banknote Authentication Dataset](https://archive.ics.uci.edu/ml/datasets/banknote+authentication)

---

## Assignment Requirements
Your Jupyter Notebook must follow a structured format with clearly numbered second-level headings and reflection remarks after each section.

Start your notebook professionally with:
- a single top-level title
- your name (or alias)
- the date
- a brief introduction that describes the problem and the dataset.
- Import the external Python libraries used (e.g., pandas, numpy, matplotlib, seaborn, sklearn).

### Section 1. Load and Explore the Data
- 1.1 Load the dataset and display the first 10 rows.
- 1.2 Check for missing values and display summary statistics.

Reflection 1: What do you notice about the dataset? Are there any data issues?

---

### Section 2. Visualize Feature Distributions
- 2.1 Create histograms, boxplots, and count plots for categorical variables.
- 2.2 Identify patterns or anomalies in feature distributions.

Reflection 2: What patterns or anomalies do you see? Do any features stand out?

---

### Section 3. Feature Selection and Justification
- 3.1 Choose two to four features to use as input for classification.
- 3.2 Justify your selection with reasoning.

Reflection 3: Why did you choose these features? How might they impact classification?

---

### Section 4. Train a Classification Model
- 4.1 Define X (features) and y (target).
- 4.2 Train a classification model using Scikit-Learn (e.g., Decision Tree, Random Forest, Logistic Regression).
- 4.3 Report accuracy, precision, recall, and F1-score.
- 4.4 Report Confusion Matrix (as a heatmap) to visualize how well the model distinguishes between classes.

Reflection 4: How well did the model perform? Any surprises in the results?

---

### Section 5. Compare Alternative Models
- 5.1 Train an alternative classifier (e.g., Random Forest if Decision Tree was used initially).
- 5.2 Compare performance metrics between both models.

Reflection 5: Which model performed better? Why might one classifier be more effective in this specific case?


---

### Section 6. Final Thoughts & Insights
- 6.1 Summarize findings.
- 6.2 Discuss challenges faced.
- 6.3 If you had more time, what would you try next?

Reflection 6: What did you learn from this project?

---

## Tasks to Complete the Assignment

1. Create a GitHub repository named ml_classification_yourname.  
1. Upload your dataset to a data/ folder in the repository.  
1. Develop a Jupyter Notebook (classification_yourname.ipynb) structured as outlined above.  
1. Complete and write reflections for each section as you work.
1. Write a README.md summarizing your project, dataset, and findings.  (See below).
1. Review a classmate’s project and provide feedback in peer_review.md. (See below).

---

## README.md (Required)

Include a professional README.md that introduces your project. Include:
- a clickable link to your notebook file.
- a clickable link to your your peer review Markdown file.
- Instructions on how to set up your virtual environment and run your notebook locally. 

## Peer Review (Required)

Review one other GitHub repository and provide feedback on:

1. Clarity & Organization (Is the notebook structured and easy to follow?)
1. Feature Selection & Justification (Do the chosen features make sense?)
1. Model Performance & Comparisons (Is the evaluation well explained?)
1. Reflection Quality (Are insights well thought out?)

Submission: Submit a short peer review document in your own repository titled peer_review.md.  
The peer review must contain a **clickable Markdown link to the notebook (.ipynb) file reviewed** along with your personal, well-organized and presented 4-pont review. 



---

## 4-point Repository Checklist

Verify your repository contains:

[ ] Jupyter Notebook (classification_yourname.ipynb) with numbered sections and reflections.  
[ ] README.md (see above)
[ ] Dataset stored in a data/ folder.  
[ ] Peer Review (peer_review.md).  

---
