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

cars_6_to_10 = cars.iloc [5:10]
cars_6_to_10

cars_6_to_10 = cars_6_to_10.loc [:, ['Model', 'mpg', 'cyl', 'hp', 'gear']]
cars_6_to_10
```

## B. MODEL LOOKUP

The model lookup problem uses boolean indexing to locate specific vehicle models based on their values in the Model column. The complete record of the Toyota Corolla is stored in toyota, while the Pontiac Firebird result contains only the requested columns: Model, mpg, hp, and wt.

The following methods are used: 

• `cars ['Model'] == 'Toyota Corolla'` - Creates a boolean condition that identifies the Toyota Corolla.

• ` cars.loc [cars ['Model'] == 'Pontiac Firebird', ['Model', 'mpg', 'hp', 'wt']]'` - Selects the record that satisfies the boolean condition and specifies the columns to retain for the Pontiac Firebird.

The combination of the different operations gives the final function:

```python
toyota = cars.loc[cars ['Model'] == 'Toyota Corolla']
toyota

Pontiac = cars.loc [cars ['Model'] == 'Pontiac Firebird', ['Model', 'mpg', 'hp', 'wt']]
Pontiac
```

The boolean conditions allow the models to be located using their names rather than hard-coded row numbers, following the requirement in the experiment.

## C. MULTI-MODEL SUBSETTING

The multi-model subsetting problem creates a new DataFrane named selected_Cars contaiining the three requested models: Datsun 710, Lotus Europa, and Ferrari Dino. Boolean conditions are combined using the `| ` operator to select records matching any of the three model names. Only Model, mpg, cyl, hp, and gear are retained.

The following methods are used: 

• `cars.loc[...]` - Selects the requested records and columns.

• `(cars ['Model'] == )]` - Identifies the car models in the record.

• `selected_cars.shape` - Checks the dimensions of the final DataFrame.

The combination of the different operations gives the final function:

```python
selected_cars = cars.loc[
    (cars ['Model'] == 'Datsun 710') |
    (cars ['Model'] == 'Lotus Europa') |
    (cars ['Model'] == 'Ferrari Dino'),
    ['Model', 'mpg', 'cyl', 'hp', 'gear']
]

selected_cars

print (selected_cars.shape)
```
Thank you for reading!

For reference of the main python program for Programming Assignment 3, kindly click the link and download: (https://github.com/sphmrlle/ECE-2112-PA-3)
### README File Version History:

September 9, 2026 - Initial README ouput uploaded and drafted.

September 10, 2026 - Final README updated
