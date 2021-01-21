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
        print ("The {} car has {} miles.".format(self.color, self.mileage))

blue = Car("blue", "20,000")
red = Car("red", "30,000")
print(blue)
print(red)
blue.print_car()
red.print_car()
```

# Create an Animal class

Create an Animal class with one instance attribute and one method:

- The instance attribute will be the *name*, which stores the name of the animal as a string.
- The method should return the sound of the animal, which returns the following string: "{variable_sound}, I'm {animal_name}! {variable_sound}"
- Then create two subclasses that inherits from the Animal class, and assign a sound to the instance attribute.
- Finally, create an instance of each of the subclasses and print the sound of each of them.

**Your output should look like below, considering you have a cow with sound Moooo and name Milky White:**
``` 
Moooo I'm Milky White! Moooo
```


```python runnable
class Animal:
    sound = ""
    def __init__(self, name):
        self.name = name
    def speak(self):
        print("{sound} I'm {name}! {sound}".format(name=self.name, sound=self.sound))

class Piglet(Animal):
    sound = "Oink!"

class Cow(Animal):
    sound = "Moooo"

milky = Cow("Milky White")
milky.speak()

```

# Capital indexes
Write a function named `capital_indexes`. The function takes a single parameter, which is a string. Your function should return a list of all the indexes in the string that have capital letters.

For example, calling `capital_indexes("HeLlO")` should return the list `[0, 2, 4]`.

```python runnable
def capital_indexes(word):
    result = []
    ind = 0
    for letter in word:
        if(letter.isupper()):
            result.append(ind)
        ind+=1
            
    return result

result = capital_indexes("HeLlO")
print(result)
```

# Counting syllables
Define a function named count that takes a single parameter. The parameter is a string. The string will contain a single word divided into syllables by hyphens, such as these:
```
"ho-tel"
"cat"
"met-a-phor"
"ter-min-a-tor"
```
Your function should count the number of syllables and return it.

For example, the call `count("ho-tel")` should return 2.

```python runnable
def count(param):
    x = param.split("-")
    return len(x)
    
result = count("ho-tel")
print(result)
```

# Up and down
Define a function named `up_down` that takes a single number as its parameter. Your function return a tuple containing two numbers; the first should be one lower than the parameter, and the second should be one higher.

For example, `calling up_down(5)` should return `(4, 6)`.

```python runnable
def up_down(param):
    down = param - 1
    up = param + 1
    return down, up

result = up_down(5)
print(result)
```

# Counting parameters

Define a function `param_count` that takes a variable number of parameters. The function should return the number of arguments it was called with.

For example, `param_count()` should return `0`, while `param_count(2, 3, 4)` should return `3`.

```python runnable
def param_count(*param):
    return(len(param))
    
result = param_count(2, 3, 4)
print(result)
```

# Thousands separator
Write a function named `format_number` that takes a non-negative number as its only parameter.

Your function should convert the number to a string and add commas as a thousands separator.

For example, calling `format_number(1000000)` should return `"1,000,000"`.

```python runnable
def format_number(param):
    ft = "{:,}"
    return ft.format(param)
    
result = format_number(1000000)
print(result)
```