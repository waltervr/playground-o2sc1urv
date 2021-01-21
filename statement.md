# Create a Car class

Create a Car class with two instance attributes:

- Color, which stores the name of the car’s color as a string.
- Mileage, which stores the number of miles on the car as an integer.
- Then instantiate two Car objects, a blue car with 20,000 miles and a red car with 30,000 miles. Finally, print out their colors and mileage. 

**Your output should look like this:**
``` 
The blue car has 20,000 miles.
The red car has 30,000 miles.
```

```python runnable
class Car:
    def __init__(self, color, mileage):
        self.color = color
        self.mileage = mileage
    def __str__(self):
        return "The {} car has {} miles.".format(self.color, self.mileage)
    def print_car(self):
        return "The {} car has {} miles.".format(self.color, self.mileage)

blue = Car("blue", "20,000")
red = Car("red", "30,000")
print(blue)
print(red)
blue.print_car()
red.print_car()
```

# Counting parameters

Define a function `param_count` that takes a variable number of parameters. The function should return the number of arguments it was called with.

For example, `param_count()` should return `0`, while `param_count(2, 3, 4)` should return `3`.

```python runnable
def param_count(*param):
    return(len(param))
    
result = param_count(2,3)
print(result)
```
