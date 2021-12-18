![header](https://capsule-render.vercel.app/api?type=waving&color=gradient&width=1000&height=200&section=header&text=Machine%20Learning%20Training%20Bot&fontSize=30&fontColor=black)

<!-- header is made with: https://github.com/kyechan99/capsule-render -->

[John Sung](https://linkedin.com/in/john-sung-3675569) [<img src="https://cdn2.auth0.com/docs/media/connections/linkedin.png" alt="LinkedIn -  John Sung" width=15/>](https://linkedin.com/in/john-sung-3675569/)

                                                             
<br>
Columbia FinTech Bootcamp Assignment - Module 14

---

### Table of Contents

* [Overview](#overview)
* [Requirements](#requirements)
* [Data](#data)
* [Evaluation Report](#evaluation-report)
* [License](#license)

---

## Overview


The program was designed to improve the existing algorithmic trading systems and maintain the firm’s competitive advantage in the market. In order to enhance the existing trading signals with machine learning algorithms that can adapt to new data, the following was accomplished...

* Established a Baseline Performance

* Tuned the Baseline Trading Algorithm

* Evaluated a New Machine Learning Classifier

* Created an Evaluation Report

---

## Requirements

This project leverages python 3.7 and scikit-learn.

A [conda](https://docs.conda.io/en/latest/) environment with liabraries listed below and [Jupyter Notebook/Lab](https://jupyter.org/) are required to run the code.

The following library was used:

1. [Scikit Learn](https://scikit-learn.org/stable/index.html) - Scikit Learn or Sklearn is one of the most used Python libraries for Data Science, along with others like Numpy, Pandas, Tensorflow, or Keras.


Install the following librarie(s) in your terminal...

    pip install -U scikit-learn

---

## Data

The data used in this neural network model was from derived from a CSV file called emerging_markets_ohlcv.csv:

---

## Evaluation Report


### Step 1: Tune the training algorithm by adjusting the size of the training dataset. 

To do so, slice your data into different periods. Rerun the notebook with the updated parameters, and record the results in your `README.md` file.

Baseline: 3 month window
![cumulative_return_plot_3_mo](Images/cum_ret_plot_act_strat_ret_3_mo.PNG)
![svm_testing_report](Images/svm_testing_report.PNG)

Increase trading window to 6 months
![cumulative_return_plot_6_mo](Images/cum_ret_plot_act_strat_ret_6_mo.PNG) 
![svm_testing_report_6_mo](Images/svm_testing_report_6_mo.PNG)

Decrease trading window to 45 days
![cumulative_return_plot_45_day](Images/cum_ret_plot_act_strat_ret_45_day.PNG)
![svm_testing_report_45_day](Images/svm_testing_report_45_day.PNG)


Answer the following question: What impact resulted from increasing or decreasing the training window? By increasing or decreasing the training window, the strategy results continued to outperform the actual results in each of the three instances; however, the original 3 months displayed the best overall performance of the three scenarios from a standpoint of the strategy returns outperforming the actual returns throughout the majority of the time evaluated. The 6 month period displayed the best overall return of the strategy returns despite the actual returns outperforming the strategy returns for a significant portion of the time evaluated. When reviewing the testing report, the delta in training window did not show material chainge in accuracy, precision or recall.

### Step 2: Tune the trading algorithm by adjusting the SMA input features. 

Adjust one or both of the windows for the algorithm. Rerun the notebook with the updated parameters, and record the results in your `README.md` file. 

Baseline: Short Window = 4 | Long Window = 100
![cumulative_return_plot_3_mo](Images/cum_ret_plot_act_strat_ret_3_mo.PNG)

Increase SMA long window to 200 days
![sma_change_200](Images/sma_change_200.PNG)

Answer the following question: What impact resulted from increasing or decreasing either or both of the SMA windows? When the long window was increased from 100 and 200 days with the training window remaining contant at three months, the results were extremely volitile. There was constant change of one outperforming the other. You also saw a significant inverse relationahip between actual returns and strategy returns with the strategy returns underforming significantly. 

### Step 3: Choose the set of parameters that best improved the trading algorithm returns. 

Save a PNG image of the cumulative product of the actual returns vs. the strategy returns, and document your conclusion in your `README.md` file. 

Increase trading window to 6 months
![cumulative_return_plot_6_mo](Images/cum_ret_plot_act_strat_ret_6_mo.PNG) 

The best set of parameters was reflected in the 6 month training windows by increasing the training dataset. Keeping the short window at 4 and long window at 100 seemed to imptove the algorithm returns   


### Step 3: Backtest the new model to evaluate its performance. 

Save a PNG image of the cumulative product of the actual returns vs. the strategy returns for this updated trading algorithm, and write your conclusions in your `README.md` file. 

Answer the following questions: 

Did this new model perform better or worse than the provided baseline model?

Baseline Model
![cumulative_return_plot_3_mo](Images/cum_ret_plot_act_strat_ret_3_mo.PNG)
![svm_testing_report](Images/svm_testing_report.PNG)

New Model
![adaboost_classifier](Images/adaboost_classifier.PNG)
![testing_report](Images/testing_report.PNG)

By importing the AdaBoost Classifier, the strategy returns in the new model did outperform the strategy results from the base model. Although there are instances where the actual returns outperformed the strategy results, the final returns were better in the new model. 

Did this new model perform better or worse than your tuned trading algorithm?

Tuned trading algorithm
![sma_change_200](Images/sma_change_200.PNG)

New Model
![adaboost_classifier](Images/adaboost_classifier.PNG)

This new model outperformed the tuned trading algorithm. Remember that step 2, by increasing the long window to 200 days, the model was not stable. The tuning made the model had unattractive returns.
Increase SMA long window to 200 days

---

## License

MIT
