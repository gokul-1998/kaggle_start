- https://www.w3schools.com/python/pandas/exercise.asp?filename=exercise_series3
    - these will be exercises for you to do on your own from w3schools

- How to read csv from pandas
```
import pandas as pd
df=pd.read_csv("data.csv")
df.to_string()
```

- Dictonary to pandas
```
import pandas

mydataset = {
  'cars': ["BMW", "Volvo", "Ford"],
  'passings': [3, 7, 2]
}

myvar = pandas.DataFrame(mydataset)

print(myvar)
```

# What is a Series?
- A Pandas Series is like a column in a table.

- It is a one-dimensional array holding data of any type.

```
import pandas as pd

a = [1, 7, 2]

myvar = pd.Series(a)

print(myvar)
```

- to create label

```
import pandas as pd

a = [1, 7, 2]

myvar = pd.Series(a, index = ["x", "y", "z"])

print(myvar)
```
- Key value objects as series
```
import pandas as pd

calories = {"day1": 420, "day2": 380, "day3": 390}

myvar = pd.Series(calories)

print(myvar)
```

- Create a Series using only data from "day1" and "day2":
```
import pandas as pd

calories = {"day1": 420, "day2": 380, "day3": 390}

myvar = pd.Series(calories, index = ["day1", "day2"])

print(myvar)
```

- Dataframe
- Data sets in Pandas are usually multi-dimensional tables, called DataFrames.

- Series is like a column, a DataFrame is the whole table.
```
import pandas as pd

data = {
  "calories": [420, 380, 390],
  "duration": [50, 40, 45]
}

myvar = pd.DataFrame(data)

print(myvar)
```

- locate row
```
#refer to the row index:
print(df.loc[0])
```
- Return row 0 and 1:
```
#use a list of indexes:
print(df.loc[[0, 1]])
```

- Add a list of names to give each row a name:
```
import pandas as pd

data = {
  "calories": [420, 380, 390],
  "duration": [50, 40, 45]
}

df = pd.DataFrame(data, index = ["day1", "day2", "day3"])

print(df) 
```

- Use the named index in the loc attribute to return the specified row(s).

Example

Return "day2":

#refer to the named index:
print(df.loc["day2"])

- `df.to_string()` 
- to print the dataframe
    - this will print the entire dataframe

- Increase the maximum number of rows to display the entire DataFrame:
```
import pandas as pd

pd.options.display.max_rows = 9999

df = pd.read_csv('data.csv')

print(df) 
```