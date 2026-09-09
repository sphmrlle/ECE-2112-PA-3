# ECE-2112-PA-3

**Made by: Sophia Marielle R. Quizon | 2ECE-B**

The content of this repository contains the Programming Assignment for the course Advanced Computer Programming and Algorithms for the S.Y. 2026-2027.

## A. POSITIONAL AND LABEL-BASED SLICING

The positional and label-based slicing problem loads the `cars.csv` dataset into a Pandas named `cars`. The shape and column are first displayed. The shape and column names are first displayed then uses positional slicing with `iloc` to have rows 6 through 10. From these rows, only the columns Model, mpg, cyl, hp, and gear are selected using column labels.

The following methods are used: 

• `pd.read_csv()` - Loads the dataset into a Pandas DataFrame.

• `cars.shape` - Displays the number of rows and columns in the DataFrame.

• `cars` - Displays the complete DataFrame and its records.

• `cars.iloc [5:10]` - Uses positional indexing to select rows  6 through 10.

• `.loc [:, ['Model', 'mpg', 'cyl', 'hp', 'gear']]` - Selects the required columns using their labels and keeps them in the requested order.


The combination of the different operations gives the final function:

```python
import pandas as pd

cars = pd.read_csv ('/cars.csv')
cars

cars.shape
