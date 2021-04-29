# Machine Learning with Python.

- ML is a subset of Artificial Intelligence
- It provides intelligence to machines with the ability to automatically learn with experiences without being explicitly programmed.

![What-is-Artificial-Intelligence-The-Layers-Explained.jpg](https://community.hpe.com/t5/image/serverpage/image-id/109882iA1402861948B2498/image-size/large?v=1.0&px=2000)

## Problem it Solves (Basic)

#### Scan a picture and tell whether it is a Dog or a Cat?

- Using traditional programming techniques, logic can be very complex depending upon the kind of picture fed
- ML is the technique to solve these kind of problems
- We build a Model / Engine and give it lots of lots of data, thousands of thousands of pictures of cat and dog
- Our Model will then find and learn patterns in the input data
- Based on that we can feed a new picture of cat or dog and our model will tell us with a certain level of accuracy
- The more data we feed to our Model, the more accurate our model be

## Applications

- Self-driving Cars
- Robotics
- Language Processing
- Vision Processing
- Forecasting Stock Market Trends

## High-Level Steps to follow in a ML Project

1. Import the data
   - We can import our Database in the form of a CSV file that can be conveniently used
2. Clean the data
   - Removing duplicate, redundant, irrelevant data so that our model don't learn bad patterns thereby producing wrong results
3. Split the data into Training / Test Sets
   - If we have thousands of pictures of dog / cat, we can reserve 80% for the training and 20% for the testing
4. Create a Model
   - It is actually selecting an Algo(Decision Trees, Neural Networks etc) to analyze our data
   - Each algo has some pros and cons in terms of Accuracy and Performance
   - So the choice of algo depends upon the kind of problem we want to solve and Input data
   - No need to explicitly program an algo, there are libraries like scikit-learn to provide these algos  
5. Train the Model
   - Feeding data to the Algo
6. Make Predictions
   - Based on the patterns it find in the data, Algo will make predictions
   - We can ask our model - Is it a Cat or a Dog?
7. Evaluate and Improve
   - Evaluate the predictions and measure the accuracy
   - Based on that, select a different Algo or fine-tune the parameters of our model

#### Note 

```
- In ML, understanding the dataset is the most crucial part
- Because we are not required to write a ML algo, it is already written, we just need to fed the data and it will do its work
- It is a 10 min job of feeding it with data and fetching its generated results.
- The accuracy of your model depends upon the choice of your dataset, what data you fed into the algo.
- The key concept is - the more data we give to our ML model and the cleaner it is, we get the better results
```

## Libraries and Tools (Popular)

- NumPy - provides Multidimensional-Arrays, very powerful, very popular
- Pandas 
  - Data Analysis Library, provides a concept called DataFrames
  - DataFrame is a 2-dimensional data structure similar to an excel spreadsheet
  - We have rows and columns, we can select data in a row or a column or a range of rows and columns
- MatPlotLib
  - 2-dimensional plotting library for creating graphs and plots
- Scikit-learn
  - It provides all the common Algorithms like Decision Trees, Neural Networks and so on

#### Note

```
- Exploratory Data Analysis (EDA) is an approach of analyzing data sets to summarize their main characteristics, often using statistical graphics and other data visualization methods.
- All these tools come under EDA
```

## Getting Started

- **Anaconda** is a free, open-source distribution of Python and R programming languages for Data Science and ML related applications.
- It comes with Python, Jupyter Notebook and Data Science libraries like Pandas, NumPy etc.
- So instead of downloading python, install **Anaconda**
- All these features make **Anaconda** one-step solution for creating ML Projects using Python

## Misc.

#### Jupyter Notebook Shortcuts

- There are two modes for a cell : Edit mode(Green) and Command Mode(Blue)
- In Edit mode, we can type in the cell
- In Command mode, we can perform actions related to cells like adding or deleting cells below or above
- Shortcuts (Command Mode)
  - a - insert cell above the current cell
  - b - insert cell below the current cell
  - press d twice - delete the current cell
  - press enter - to enter in edit mode
  - press escape - to enter in command mode
  - ctrl + enter - runs the current cell without adding a cell beneath it

#### References

- kaggle.com for data sets