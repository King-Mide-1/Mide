## Everything you need to know about Arrays in Python

# This article will teach you how to use arrays more efficiently when writing codes in Python.

Before we begin I would want you to understand that **Arrays** are not predefined in Python, but for us to make use of them we use **Lists** instead. So come with me lets see how we can use **Arrays** in Python from a beginner level example to an advanced level.

## **What is an Array?**
Arrays are used to store multiple items or values in one single variable. *Confused?*😂 well an array is a special variable, that is capable of holding more than one value at a time. You can compare an array to a basket and values to different types of fruits. Enough of the explanations, let's dive into some real world examples of **Arrays**  

## **How to use an Array.**

Let's say we have a list of fruits, storing them in a single variable would look like this:

```
fruit1 = "Strawberry"
fruit2 = "Banana"
fruit3 = "Mango"
``` 
The above example is the correct method of storing values inside a variable, which is totally fine and acceptable by Python. But what if we want to store about 100 fruits? that would definitely take a lot of time. So instead of having long lines of codes in our Python file, we can simply make use of Arrays. Let us see how we can do that.

```
fruits = ["Strawberry", "Banana", "Mango"]
``` 
You see how simple and easy the above example is? That is what an Array is. Also note that it can store as much as possible values. Give it a try.
## How to access the values in arrays.
Now that we have a full idea of what an Array is and what it does. Let's see how we can access each elements inside it.

To do that we need to make use of index(index is another word for number). Please note that index starts from 0 to 1 to 2 and so on and so forth.
The next example will teach us how to access the first value in the array of fruits.
```
fruits = ["Strawberry", "Banana", "Mango"]
print(fruits[0])
``` 
The output of the above lines of code will be **Strawberry**.
Remember we said the index starts from 0, so the first value in fruits will be index 0. To print out "Mango" we will simply replace 0 with 2.
## Length of elements in an Array
When we have a lot of values in our array, we might lose count and become worried. The next example shows how we can know the numbers of values in our array no matter how many it is.

``` 
fruits = ["Strawberry", "Banana", "Mango"]
print(len(fruits))
``` 
The output of the above lines of code will be **3**. We are able to know the numbers of values in our array using the "**len**" function.
## Loops in Array
For us to loop through each items or access each items in our array we must use the "**for**" "**in**" function. Lets see how we can implement this.

```
fruits = ["Strawberry", "Banana", "Mango"]
for x in fruits:
    print(x)
``` 
This program will print out all the values in fruits vertically **["Strawberry", "Banana", "Mango"]**
## Add and remove values in an Array
To add or remove a value from our array we do not have to type or delete a value every single time in our code. We can seamlessly do that anywhere in our program by simply calling the existing array and modifying it with some functions. First let's see how we can add a value to our existing array

```
fruits = ["Strawberry", "Banana", "Mango"]
fruits.append("Grape")
print(fruits)
``` 
The above lines of code will simply print out **["Strawberry", "Banana", "Mango", "Grape"]**. This is made possible because we used the ".append()" function.

To remove an element from our array, we need to make use of the **".pop()"** or **".remove()"** function. The difference between these two functions is that **".pop()"** deletes the value using an integer but *".remove()"* deletes a using a string. Let's try them out.

```
fruits = ["Strawberry", "Banana", "Mango"]
fruits.remove("Banana")
print(fruits)
``` 
```
fruits = ["Strawberry", "Banana", "Mango"]
fruits.pop(1)
print(fruits)
``` 
The output of these two examples will be ["Strawberry", "Mango"]

Below are other functions or methods you can use to make an array fully functional without too much lines of code.


- **index()	Returns the index of the first element with the specified value**
- **clear()	Removes all the elements from the list**
- **copy()	Returns a copy of the list**
- **count()	Returns the number of elements with the specified value**
- **extend()	Add the elements of a list (or any iterable), to the end of the current list**
- **insert()	Adds an element at the specified position**
- **reverse()	Reverses the order of the list**
- **sort()	Sorts the list**

I hope you find this piece of information educating. If you do, please do me a favor by hitting the like button and also do well to share with friends who are also learning.