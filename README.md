#### M.TECH IN COMPUTER SCIENCE AND ENGINEERING (SCS) 
#### SEMESTER – II 
#### Course Code 20SCSL26 
#### DATA SCIENCE LABORATORY 

The purpose of this laboratory is to get you acquainted with Python/R and use them in implementing Data Science and Algorithms. 

Data Sets 

Iris

Iris is a particularly famous toy dataset (i.e. a dataset with a small number of rows and columns, mostly used for initial small-scale tests and proofs of concept). This specific dataset contains information about the Iris, a genus that includes 260-300 species of plants. The Iris dataset contains measurements for 150 Iris flowers, each belonging to one of three species: Virginica, Versicolor and Setose. (50 flowers for each of the three species). Each of the 150 flowers contained in the Iris dataset is represented by 5 values: 
• Sepal length, in cm 
• Sepal width, in cm 
• petal length, in cm 
• petal width, in cm 

Iris species, one of: iris-setose, iris-versicolor, iris-virginica. Each row of the dataset represents a distinct flower (as such, the dataset will have 150 rows). Each row then contains 5 values (4 measurements and a species label). The dataset is described in more detail on the UCI Machine Learning Repository website. The dataset can either be downloaded directly from there (iris.data file), or from a terminal, using the wget tool. The following command downloads the dataset from the original URL and stores it in a file named iris.csv. $ wget "https://archive.ics.uci.edu/ml/machine-learning-databases/iris/iris.data" -O iris.csv 

Citybik.es

Citybik.es is a website that offers an Application Programming Interface (or API, for short) for the usage of bike-sharing services throughout the world. Among the others, data for one of Turin’s bike sharing system is available. The information available is at a “station” granularity. This means that all the data available regards the bike stations: some of the useful information available is the station name, its position (in terms of latitude and longitude), the number of available bikes and the number of free docks. The data is offered in near real-time (i.e. it is updated every 15-30 minutes). The API endpoint to request the data about for the Bike service is the following: http://api.citybik.es/v2/networks/to-bike. This dataset is in the JSON (JavaScript Object Notation) format.

MNIST

 The MNIST dataset is another particularly famous dataset as CSV file. It contains several thousands of hand-written digits (0 to 9). Each hand-written digit is contained in a 28 × 28 8-bit grayscale image. This means that each digit has 784 (282 ) pixels, and each pixel has a value that ranges from 0 (black) to 255 (white). The dataset can be downloaded from the following URL: https://raw.githubusercontent.com/dbdmg/data-science-lab/master/datasets/mnist_test.csv. Each row of the MNIST datasets represents a digit. For the sake of simplicity, this dataset contains only a small fraction (10,000 digits out of 70,000) of the real MNIST dataset, which is known as the MNIST test set. For each digit, 785 values are available.

Exercises 

1. Iris dataset Load the Iris dataset as a list of lists (each of the 150 lists should have 5 elements). Compute and print the mean and the standard deviation for each of the 4 measurement columns (i.e. sepal length and width, petal length and width). Compute and print the mean and the standard deviation for each of the 4 measurement columns, separately for each of the three Iris species (Versicolor, Virginica and Setose). Which measurement would you consider “best”, if you were to guess the Iris species based only on those four values? 

2. Load the Citybik.es dataset as a Python dictionary. Use of the json module. Count and print the number of active stations (a station is active if its extra.status field is "online"). Count and print the total number of bikes available (field free_bikes) and the number of free docks (field empty_slots) throughout all stations. Given the coordinates (latitude, longitude) of a point (e.g. 45.074512, 7.694419), identify the closest bike station to it that has available bikes. For computing the distance among two points (given their coordinates), you can use the function distance_coords() defined in the code snippet below (which is an implementation of the great-circle distance): from math import cos, acos, sin defdistance_coords(lat1, lng1, lat2, lng2): """Compute the distance among two points.""" deg2rad = lambda x: x * 3.141592 / 180 lat1, lng1, lat2, lng2 = map(deg2rad,[ lat1, lng1, lat2, lng2 ]) R = 6378100 # Radius of the Earth, in meters return R * acos(sin(lat1) * sin(lat2) + cos(lat1) * cos(lat2) * cos(lng1 - lng2)) 

3. Load the MNIST dataset. Create a function that, given a position 1 ≤ k ≤ 10, 000, prints the kthdigit of the dataset (i.e. thekthrow of the csv file) as a grid of 28 × 28 characters. More specifically, you should map each range of pixel values to the following character [0, 64) → " " [64, 128) → "."  [128, 192) → "*" [192, 256) → "#" Compute the Euclidean distance between each pair of the 784-dimensional vectors of the digits at the following positions: 26th, 30th, 32nd, 35th. Based on the distances computed in the previous step and knowing that the digits listed are 7, 0, 1, 1, can you assign the correct label to each of the digits ? 

4. Tips dataset Read the dataset. “Tips.csv” as a dataframe “Data”. Extract the columns in the following sequence - Time, TotalBill, Tips. Plot a histogram for the variable ‘TotalBill’ to check which range has the highest frequency. Draw a bar chart for the variable “Day”. Identify the category with the maximum count. Demonstrate the data distributions using box, scatter plot, histogram, and bar chart on iris dataset. Demonstrate the correlation plot on iris dataset and perform exploratory visualization giving an overview of relationships among data with covariance analysis. 

5. Split the Iris dataset into two the datasets - IrisTest_TrainData.csv, IrisTest_TestData.csv. Read them as two separate data frames named Train_Data and Test_Data respectively. Answer the following questions:
   1. How many missing values are there in Train_Data?
   2. What is the proportion of Setosa types in the Test_Data?
   3. What is the accuracy score of the K-Nearest Neighbor model (model_1) with 2/3 neighbors using Train_Data and Test_Data?
   4. Identify the list of indices of misclassified samples from the ‘model_1’.
   5. Build a logistic regression model (model_2) keeping the modelling steps constant. Find the accuracy of the model_2


1. program 1: <a href="https://github.com/DhanyaJayanA/Basic-Programming/blob/main/DS_LAB_Program1.ipynb">Code</a>
2. program 2: <a href="https://github.com/DhanyaJayanA/Basic-Programming/blob/main/DS_Lab_Program_2.ipynb">Code</a>
3. program 3: <a href="https://github.com/DhanyaJayanA/Basic-Programming/blob/main/DS_Lab_program3.ipynb">Code</a>
4. program 4: <a href="https://github.com/DhanyaJayanA/Basic-Programming/blob/main/DS_Lab_Program_4%20(1).ipynb">Code</a>
5. program 5: <a href="https://github.com/DhanyaJayanA/Basic-Programming/blob/main/DS_Lab_Program5%20(1).ipynb">Code</a>
6. image read, display write <a href="https://github.com/DhanyaJayanA/Basic-Programming/blob/main/Read%2C_Display_and_Write_images.ipynb">Code</a>
