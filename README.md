
# Usage of the PolynomialRegression API



```
data = [[0 for x in range(2)] for y in range(4)]
data[0][0] = 1
data[0][1] = 13
data[1][0] = 2
data[1][1] = 26
data[2][0] = 3
data[2][1] = 42
data[3][0] = 4
data[3][1] = 68

independent = []
dependent = []
for (x, y) in data:
    independent.append(x)
    dependent.append(y)
    
regression = PolynomialRegression(2)
coefficient = regression.fit(independent, dependent)
print(coefficient)
#[8.25, 1.849999999999909, 3.25]
    
```
#### PolynomialRegression(n) <--- Here n indicates the degree of the curve being fit for regression.
#### coefficient = regression.fit(independent, dependent) <--- independent, dependent are two lists containing independent and dependent variable from the sample
#### The returned coefficients are listed in increasing order of the degree terms, i.e. (B0, B1, B2, B3, ....)

```
regression = PolynomialRegression(2)
coefficient = regression._fit(data)
print(coefficient)
#[8.25, 1.849999999999909, 3.25]
```
#### PolynomialRegression(n) <--- Here n indicates the degree of the curve being fit for regression.
#### coefficient = regression._fit(data) <--- data is a two dimensional array holding samples of (independent, dependent)
#### The returned coefficients are listed in increasing order of the degree terms, i.e. (B0, B1, B2, B3, ....)
