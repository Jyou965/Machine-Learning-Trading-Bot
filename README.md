# Machine-Learning-Trading-Bot

This application uses machine learning algorithms to generate predictive trading signals.  By using this application, investment firms can have sustained advantages in their abilities to adapt to the fast changing market environment real time.  

---

## Libraries and Dependancies

This application leverages python 3.7 with the following packages:

* [pandas](https://pandas.pydata.org/docs/) - an open source, BSD-licensed library providing high-performance, easy-to-use data structures and data analysis tools for the Python programming language.

* [numpy](https://numpy.org/doc/stable/) - the fundamental package for scientific computing in Python. It is a Python library that provides a multidimensional array object, various derived objects (such as masked arrays and matrices), and an assortment of routines for fast operations on arrays, including mathematical, logical, shape manipulation, sorting, selecting, I/O, discrete Fourier transforms, basic linear algebra, basic statistical operations, random simulation and much more.

* [pathlib](https://docs.python.org/3/library/pathlib.html) - a Python module which provides an object API for working with files and directories. The pathlib is a standard module. Path is the core object to work with files.

* [hvplot](https://hvplot.holoviz.org/user_guide/Introduction.html) - provides a high-level plotting API built on HoloViews and Bokeh that provides a general and consistent API for plotting data in all the abovementioned formats.

* [matplotlib](https://https://matplotlib.org/) - a comprehensive library for creating static, animated, and interactive visualizations in Python.

* [scikit-learn](https://scikit-learn.org/stable/) - tools for predictive data analysis.

* [sklearn.preprocessing](https://scikit-learn.org/stable/modules/preprocessing.html) - provides several common utility functions and transformer classes to change raw feature vectors into a representation that is more suitable for the downstream estimators.

* [pandas.tseries.offsets](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.tseries.offsets.DateOffset.html) - Standard kind of date increment used for a date range.

* [sklearn.metrics](https://scikit-learn.org/stable/modules/classes.html#module-sklearn.metrics) - includes score functions, performance metrics and pairwise metrics and distance computations.

*[sklearn.tree](https://scikit-learn.org/stable/modules/tree.html) - Decision Trees (DTs) are a non-parametric supervised learning method used for classification and regression. The goal is to create a model that predicts the value of a target variable by learning simple decision rules inferred from the data features. A tree can be seen as a piecewise constant approximation.

---

## Usage

This application works in four steps:

1. Establish a Baseline Performance

2. Tune the Baseline Trading Algorithm

3. Evaluate a New Machine Learning Classifier

4. Create an Evaluation Report

By using this application, an investment professional can find the best-fitting machine learning model for trading purposes.

---

## Evaluation Report

The chart below shows that the baseline strategy (model 1) return outperforms actual returns by evaluating cummulative returns over the six years.  The cummulative strategy return outperformed cummulative actual return by 13.06%.

![Plot](https://github.com/Jyou965/Machine-Learning-Trading-Bot/blob/main/svm.png)
![Plot]()

This strategy is generated with the following parameters:
- the SVC classifier model from SKLearn's support vector machine (SVM) learning method;
- using three months of data as training data and the remaining 69 months' data;
- with SMA_Fast indicator being the simple moving average of 4 data points and SMA_Slow indicator being the simple moving average of 100 data points.

By changing the training data scope from three months to 24 months while keeping all else equal (model 2), the predictive results improved to the following:
![Plot]()
The outperformance of the cummulative strategy over cummulative actual return widened to 17.86%.
![Plot]()

Such improvement in model 2 performance was due to increasing the training data range from 3 months to 24 months.

Based on model 2, by increasing the SMA_Fast window to 200 datapoints (approx. 50 days) and increasing the SMA_Slow window to 800 datapoints (approx. 200 days), we generated model 3, with the following results:
![Plot]()
The outperformance of the cummulative strategy over cummulative actual return widened to 17.86%.
![Plot]()

Surprisingly, model 3 underperformed cummulative actual return by 102.27% due to increasing the windows of SMA indicators!  

Finally, we establish model 4 by using the Decision Tree model, keeping the windows of SMA_Fast and SMA_Slow at 4 and 100 respectively, using 24 months as training period.  The model performance is demonstrated in the following charts.  
![Plot]()

Model 4 under-performed cummulative actual return by 70%!
![Plot]()

The conclusion is that 
1. Decision Tree model is ill-suited for linear data as stock returns.  SVM model is a better fit.
2. Longer training period of 24 months benefited the model performance.
3. Windows for SMA indicators are best kept relatively short.

---

## Contributors

Jackie You with the support of FinTech Boot Camp Staff

---

## License

Berkeley
