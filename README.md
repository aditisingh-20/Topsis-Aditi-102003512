# TOPSIS
## Assignment for UCS654
---
Aditi Singh

102003512

3CO20
### What is TOPSIS?

TOPSIS stands for "The Technique for Order of Preference by Similarity to Ideal Solution" is a multi-criteria decision analysis method, which was originally developed by Ching-Lai Hwang and Yoon in 1981 with further developments by Yoon in 1987, and Hwang, Lai and Liu in 1993. TOPSIS chooses the alternative of shortest Euclidean distance from the ideal solution, and farthest distance from the negative-ideal solution. More details at [wikipedia](https://en.wikipedia.org/wiki/TOPSIS). The TOPSIS algorithm is succinctly explained in this [paper comparing TOPSIS and VIKOR methods]https://www.sciencedirect.com/science/article/abs/pii/S0377221703000201)
### How do I use TOPSIS?

First, install the TOPSIS module using pip.
```pip install Topsis-Aditi-102003512```

Then, run the TOPSIS file with the arguements - 
```python Topsis-Aditi-102003512 102003512-data.csv 1,1,1,1,1 +,-,+,-,+ 102003512-result.csv```

Here, the first argument after the python program is your subject dataframe is stored in csv format in data.csv.
The second arguement is the weights you are assigning to each feature of the dataset. The default weights are 1.
The third arguement are the assigned impacts. The default impact is '+'.
The fourth argument is the filename in which the output table is to be stored. If no file name is given then '102003512-data.csv' file is chosen.

Output is the csv file of the model with TOPSIS Score and TOPSIS Rank.


### Example
Running command -

```python Topsis-Aditi-102003512 102003512-data.csv 1,1,1,1,1 +,-,+,-,+ 102003512-result.csv```

Input Dataset - (102003512-data.csv)

|Fund Name|P1|P2|P3|P4|P5|
|--------------|--------------|--------------|--------------|--------------|--------------|
|M1|0.68|0.46|5|38.5|11.16|
|M2|0.78|0.61|5|30.6|9.25|
|M3|0.79|0.62|6.9|34.9|10.8|
|M4|0.82|0.67|6.2|36.1|10.95|
|M5|0.64|0.41|6.7|46.8|13.64|
|M6|0.63|0.4|7|59.5|16.88|
|M7|0.77|0.59|4|45.3|12.67|
|M8|0.79|0.62|3.9|33.6|9.73|

Weights -> 2,2,3,3,4
Impacts -> -,+,-,+,-

Output Dataset - (stored in 102003512-result.csv)

|Fund Name|P1|P2|P3|P4|P5|Topsis Score|Rank|
|--------------|--------------|--------------|--------------|--------------|--------------|--------------|--------------|
|M1|0.68|0.46|5|38.5|11.16|0.545126218|4|
|M2|0.78|0.61|5|30.6|9.25|0.561913424|3|
|M3|0.79|0.62|6.9|34.9|10.8|0.469000051|6|
|M4|0.82|0.67|6.2|36.1|10.95|0.50574866|5|
|M5|0.64|0.41|6.7|46.8|13.64|0.405123307|7|
|M6|0.63|0.4|7|59.5|16.88|0.404922284|8|
|M7|0.77|0.59|4|45.3|12.67|0.60568518|2|
|M8|0.79|0.62|3.9|33.6|9.73|0.607093772|1|