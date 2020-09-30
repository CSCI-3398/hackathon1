# Hackathon 1: Northeastern vs. Western Accents

## Overview of the task
For this first hackathon, your team will develop a model for distinguishing the speech of people who grew up in the **Northeastern US** (specifically, New England and New York City) from the speech of people who grew up in the **Western US** (the states on the US west coast and in the southwest). 

### Data
The `wav` and `TextGrid` files can be found in the correspondingly named directories (`Northeast` and `West`). This data is a subset of the TIMIT database, which you can learn more about [here](https://github.com/philipperemy/timit). 

### Code
In the `starter_code.ipynb` file, I have given you code that extracts some basic speech features and classifies with cross validation. 

### Baselines
I've provided two baselines: the majority class baseline, and a baseline using the sorts of features we've  extracted before (mean pitch, mean intensity, duration, and mean F1 in vowel segments). I've used parselmouth here, but you are free to use Praat directly and then save out the features to files that you then read in with Python to do classification.

---

## Schedule of activities

### Step 1: Thursday 10/1 through Tuesday 10/6
Between now and Tuesday, you should work with your team to improve over these baselines. How will you improve over the baselines? There are two things you should do:

* Experiment with different classifiers and model parameters, with scikit and other relevant libraries. 
* Extract more features from the `wav` and `TextGrid` files, and do some feature selection.


### Step 2: Tuesday, October 6
On Tuesday, October 6, I will post a small unseen test set. You will then test your best model on that test set. You are free to continue developing your models using that new test data throughout the day on Tuesday. Then by 11:59pm Boston time on Tuesday, you will turn in a python program or a Jupyter notebook that will read in *any* test data, apply your model to that new test data, and produce **a file with this EXACT format**:

```
wavfilename,class
```

where `wavfilename` is the name of the test `wav` file and class is either `1` (West) or `0` (Northeast). 

Remember: In the version of the code you provide to me, you will **not** do cross validation. You will train on *all* of the training data I am giving you now, and then you will apply that model to the unseen new test data I provide. You learned how to do this in ps4.

**It is crucial that I be able to grab your code (and any other necessary data, such as files containing feature values in case you extract features outside your modeling code) from your GitHub repo, and trivially run your code on unseen data. Describe how to run the program in a *README* file or similar. If I can't do this easily, your submission will be ineligible.**

### Step 3: Thursday, October 8
By 2:45pm on Thursday, October 8, you will submit to Canvas **one or more slides** (either a PDF or a link to a Google Slides document) describing exactly what features and classifiers you explored. You should talk about the challenges you faced (including logistical challenges), pitfalls you encountered, and why you decided to proceed in the directions that you did. You should provide **tables and/or graphs and charts** showing the evaluation metrics for various models you created as you worked toward your final model.

During class on Thursday 10/8, you will present your slides to the class. You are expected to speak for around 5 minutes, so make sure you have enough material to talk about. If you like, you can designate a few people to speak and a few people to prepare the slides. Make a note at the end of your presentation of who took responsibility for which activity.

---

## Prizes and grading

### Grading
You will be graded on your presentation and on how much work you did, and *not* on your final accuracy or F1 measure. I expect to see a lot of code and enough material to take up the full 5 minutes for your presentation.

### Prizes
Members of the team with the highest accuracy and the team with the highest F1 measure will have their *two* lowest quiz grades dropped when I calculate their final grades.

---

## Getting started

Clone this repo, and then open `starter_code.ipynb` with Jupyter notebook to view and run the code that will give you the baselines. **READ THE COMMENTS IN THE CODE!** Also, remember that you can't proceed to the next code block until the asterisk to the left of the current code block has turned into a number. 

```
[ ] = code has not been executed
[*] = code is currently executing
[2] = code has been executed

```

Post your questions on the [Slack channel for Hackathon 1](https://csci3398.slack.com/archives/C019MUSM0BY).
