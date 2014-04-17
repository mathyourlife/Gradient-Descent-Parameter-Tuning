# Gradient-Descent-Parameter-Tuning

Provide a function to find the best input parameters.  "Best" is quantified through a function provided by the user to quantify the results of the test.

## Example

An experiment creates data based on the underlying equation of
    (x-5)^2 + (y+2)^2 + (z-1)^2

Gradient descent should find the local minimum of (5, -2, 1)

```bash
python gradient_descent.py
```

```
Best performance at
x:
  val: 4.67357  range: -10,10   std: 0.786667
y:
  val: -2.37629 range: -10,10   std: 0.606853
z:
  val: 0.920501 range: -10,10   std: 0.548887
```

## Requirements

```
pip install -r requirements.txt
```