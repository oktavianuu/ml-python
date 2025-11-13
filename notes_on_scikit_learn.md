#### How to use scikit-learn library?
In order to use scikit learn library, we need to convert pandas dataframe to numpy array. because scikit learn was originally designed around NumPy, not Pandas DataFrame its core algorithm are implemented on top of NumPy and SciPy, which are optimized for numerical computation on dense arrays.

So internally, scikit-learn expects data in a numerical matrix form — something like this:
```python
X = np.array([[1.2, 3.4],
              [5.6, 7,8],
              [9.0, 1.2]])
```
