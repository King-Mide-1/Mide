## *Args and **Kwargs in Python

# What is Args and Kwargs?

Before we get into detail about what they mean, it's important to note that those names are simply conventions, and they can alternatively be written as `*Hi` and `**Hello`

In Python, `*args` specifies the number of non-keyworded arguments that can be passed to a function. `**Kwargs` on the other side is used to represent any number of arguments supplied to a function.


# Why use Args and Kwargs?

Primarily, when writing a functions in Python, you must clearly state the arguments that the function will or must accept.

Under some certain scenarios, it is impossible to declare all the arguments that you wish to pass to a function precisely, considering that you might want to accept more arguments in the future. So what do we do in such situations? we use `*args` and `**kwargs`! They allow you to call a function with an unspecified amount of parameters. Let's get started with some use cases.

# The *Args keyword

To know how it works, let us develop a simple program that combines the values of two arguments together.

```
def add_numbers(first_argument, second_argument):
        return first_argument + second_argument

print('Total: ', add_numbers(5, 10))
``` 
**Output**

```
Total: 15
``` 
Now that we've seen what `*args` can accomplish, let's dig a little further by creating a program that combines three arguments.
```
def add_numbers(first_argument, second_argument, third_argument):
        return first_argument + second_argument + third_argument

print('Total: ', add_numbers(5, 10, 15))
``` 
**Output**
```
Total: 30
``` 
It worked exactly as intended because we defined the amount of arguments to be passed to the function. What if we attempt to pass more arguments than anticipated? The compiler throws an error because that is not what we programmed it to do.

# The **Kwargs keyword

Unlike `*args`, we can do more with `**kwargs` because it allows us to pass any number of keyword argument. Suppose we want to develop a program that displays information about a car in a rental company, all we need to do is pass the information about the car to a function, which will in turn print out the data to the console in a dictionary format.

```
def car_x(**kwargs):
     print(kwargs)

car_x(brand='Mercedes Benz',model='AMG A 35',colour='Black',price=50,000)
``` 
**output**

```
{'brand':'Mercedes Benz','model':'AMG A 35','colour':'Black','price':50,000}
``` 
The above function describes how powerful the `**kwargs` keyword is. We can continue giving the car_x more description and it will print them out in the console without errors.

# Can i use the keywords together?

Is it possible to use the two keywords together? yes it is! but we have to follow a particular procedure when declaring a function that uses the two keywords. see example below

```
def two_keywords(*args, **kwargs):
```

# Conclusion

You can give a Python function a variable number of arguments by using the `*args` and `**kwargs` keywords. When using them together, `*args` should come before `**kwargs` and do not forget that the words “args” and “kwargs” are only a convention, you can use any name of your choice and it will work fine.