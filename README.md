# Challenge_14
## Project Overview
notebook that clusters cryptocurrencies by their performance in different time periods.
---

## Technologies

The application is in python and is uing the following libraries:



* [pandas](https://pandas-profiling.github.io/pandas-profiling/docs/master/index.html) - For data analysis.

* [hvplot.pandas](https://github.com/holoviz/hvplot) - For advanced graphs.

* [Path](https://github.com/jaraco/path) - For relative and absolute path to the file.

* [scikit-learn](https://github.com/scikit-learn/scikit-learn)- Has many features. Used for Kmeans, PCA adn StandardScaler for this assignment. 


# Imports


The operating system used in creating the application is Windows 10 64 bit. The application that used to code in notebook is Jupyter and then tested in Gitbash and Terminal. 

I created a engine for the application

The output file was read by:

```python
ohlcv_df = pd.read_csv(
    Path("emerging_markets_ohlcv.csv"), 
    index_col='date', 
    infer_datetime_format=True, 
    parse_dates=True
)
```
---

## Installation Guide

1. Open Gitbach or terminal and go ito the folder where you want to place the files.
2. Click on the blue "code" button which will allow you to clone.![<Code button in Github>]()
3. Then click on SSH or HTTPS as a clone method depending on if you have the SSH key setup. You will copy the link. You will then type "git clone" in Gitback or Terminal. Then paste the ssh or https information and press enter.
4. Next type "git pull" command in Temrinal or GitBash to pull the repository from the remote Github repository to a local directory on your computer.
5. You have access to the application. Also there will be all the python files that the application is depended on,  plus the excel file. 

---

## Usage

Below is a list of steps/analysis seen in the notebook:
    1.Establish a Baseline Performance
        1. Import the OHLCV dataset into a Pandas DataFrame.
        2. Generate trading signals using short- and long-window SMA values.
        3.Split the data into training and testing datasets.
        4.Use the SVC classifier model from SKLearn's support vector machine (SVM) learning method to fit the training data and make predictions based on the testing data. Review the predictions.
        5. Review the classification report associated with the SVC model predictions.
        6.Create a predictions DataFrame that contains columns for Predicted values, Actual Returns, and Strategy Returns.
        7. Create a cumulative return plot that shows the actual returns vs. the strategy returns. Save a PNG image of this plot. This will serve as a baseline against which to compare the effects of tuning the trading algorithm.
        8. Write your conclusions about the performance of the baseline trading algorithm in the README.md file that’s associated with your GitHub repository. Support your findings by using the PNG image that you saved in the previous step.
    2.Tune the Baseline Trading Algorithm
        1. Tune the training algorithm by adjusting the size of the training dataset. To do so, slice your data into different periods. Rerun the notebook with the updated parameters, and record the results in your README.md file. Answer the following question: What impact resulted from increasing or decreasing the training window?
        Answer--If I change it from 1 hour to 6 hours, the graph is either zoomed in or out more to show more focused information.
        2. Tune the trading algorithm by adjusting the SMA input features. Adjust one or both of the windows for the algorithm. Rerun the notebook with the updated parameters, and record the results in your README.md file. Answer the following question: What impact resulted from increasing or decreasing either or both of the SMA windows?
        Answer--If I adjust the SMA window size from 4 to 40 and 100 to 1000, the plot shows with just strategy or actual data.
        3. Choose the set of parameters that best improved the trading algorithm returns. Save a PNG image of the cumulative product of the actual returns vs. the strategy returns, and document your conclusion in your README.md file.
    3.Evaluate a New Machine Learning Classifier
        1. Import a new classifier, such as AdaBoost, DecisionTreeClassifier, or LogisticRegression. (For the full list of classifiers, refer to the Supervised learning page (Links to an external site.) in the scikit-learn documentation.)
        2. Using the original training data as the baseline model, fit another model with the new classifier.
        3. Backtest the new model to evaluate its performance. Save a PNG image of the cumulative product of the actual returns vs. the strategy returns for this updated trading algorithm, and write your conclusions in your README.md file. Answer the following questions: Did this new model perform better or worse than the provided baseline model?-- Answer better.
        Did this new model perform better or worse than your tuned trading algorithm?--Answer worse
    4.Create an Evaluation Report
    

---

## Contributors

This application was provided by the instrutor of Columbia University and addtional code was added by Khatija Azeem to complete the project.

---

## License

For this application, I used Github to uplaod the file into a repository. Since this is a public file, there will be no restriction on usage of this code. 
