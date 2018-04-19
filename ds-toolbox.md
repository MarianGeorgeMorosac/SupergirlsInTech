# [Jupyter Notebook](http://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/what_is_jupyter.html)
> the shell of IPython Notebook (local web server that
runs a python session; can add markdown and code visualisation)
> appeared as a response to the need of the Data Scientists
> to frequently experiment and share their progress
```bash
jupyter notebook --port=8889 --ip=127.0.0.1 --notebook_dir=notebook_path
```

# [pandas](https://pandas.pydata.org/)
> pandas is an open source library providing high-performance,
> easy-to-use data structures and data analysis tools
> for the Python programming language
```python
import pandas as pd
```

# [pandas.DataFrame](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.html)
> Two-dimensional size-mutable, potentially heterogeneous
> tabular data structure with labeled axes (rows and columns).
> Arithmetic operations align on both row and column labels.
> Can be thought of as a dict-like container for Series objects.
> The primary pandas data structure

```python
    # ex. of DataFrame sources
    pd.DataFrame(object)
    pd.read_csv('file_source', sep=, names=, header=, index_col=, parse_date=)
```


# [pandas.DataFrame.head()](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.head.html)
> first entries of a DataFrame; default = 5
```python
df.head(n=3)
```

# [pandas.DataFrame.tail](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.tail.html)
> last entries of a DataFrame; default = 5
```python
df.tail(n=4)
```

# [pandas.DataFrame.info()](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.info.html)
> Concise summary of a DataFrame.
> Specified each data type and the non-null count
```python
df.info()
```

# [pandas.DataFrame.fillna()](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.fillna.html)
> Fill NA/NaN values using the specified method
```python
df['column'].fillna('value') # or
df.fillna(method)
```

# [pandas.Series](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.Series.html)
> One-dimensional ndarray with axis labels (including time series).
```python
    # ex. of obtaining an instance:
    df['column_name']
```

# [matplotlib.pyplot](https://matplotlib.org/api/pyplot_api.html)
> Provides a MATLAB-like plotting framework.
```python
import matplotlib.pyplot as plt
plt.plot() # create plot
plt.show() # display plot
plt.clf() # clear display
```

# [pandas.DataFrame.plot](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.plot.html#pandas-dataframe-plot)
> Make plots of DataFrame using matplotlib / pylab.
```python
df.plot()
```

# [pandas.Series.value_counts](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.Series.value_counts.html)
> Returns object containing counts of unique values.
```python
df['column'].value_counts()
```

# [pandas.Series.iteritems](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.Series.iteritems.html)
> lazy iterate with index, value tuples
```python
for key, value in df['column'].iteritems():
    print(key, value)
```

# [pandas.DataFrame.from_dict](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.from_dict.html)
> Construct DataFrame from dict of array-like or dicts
```python
DataFrame.from_dict(data, orient='columns', dtype=None)
```

# [pandas.DataFrame.sort_values](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.sort_values.html)
> Sort by the values along either axis
```python
df.sort_values(['column'], axis=0, ascending=True)
```

# [pandas.DataFrame.corr](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.corr.html)
> Compute pairwise correlation of columns, excluding NA/null values
```python
DataFrame.corr(method='pearson', min_periods=1)
```

# [numpy and ndarray](https://docs.scipy.org/doc/numpy-1.13.0/user/whatisnumpy.html)
> NumPy is the fundamental package for scientific computing in Python.
> It is a Python library that provides a multidimensional array object,
> various derived objects (such as masked arrays and matrices), and an
> assortment of routines for fast operations on arrays,
> including mathematical, logical, shape manipulation, sorting, selecting,
> I/O, discrete Fourier transforms, basic linear algebra, basic statistical
> operations, random simulation and much more.
> At the core of the NumPy package, is the ndarray object.
> - have a fixed size at creation
> - have a fixed size at creation
> - facilitate advanced mathematical and other types of
>    operations on large numbers of data
```python
import numpy as np
x = [1, 2, 3]
np_x = np.array(x)
```