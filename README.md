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

## Usage

```python
def run_experiment_with_these(x, y, z):
    # stuff here
    return [stats]

def measure_performance(stats):
    pass

domains = [
    ['x', -10, 10],  # search for best x in -10 <= x <= 10
    ['y', -10, 10],  # search for best y in -10 <= y <= 10
    ['z', -10, 10],  # search for best z in -10 <= z <= 10
]

kwargs = {
    # Number of iterations to run
    'N': 1000,

    # Definition of parameter search domain
    'domains': domains,

    # Function that will run a test
    'run_test': run_experiment_with_these,

    # Function that will take the return of run_test and determine
    # how well the parameters worked.
    'calc_cost': measure_performance,
}
print GradientDescent.descend(**kwargs)
```

## Requirements

```
pip install -r requirements.txt
```