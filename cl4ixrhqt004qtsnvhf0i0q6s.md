---
title: "Everything you need to know about Arrays in Python"
seoTitle: "Arrays in Python."
seoDescription: "This article will teach you how to use arrays more efficiently when writing codes in Python."
datePublished: Fri Jun 17 2022 21:01:16 GMT+0000 (Coordinated Universal Time)
cuid: cl4ixrhqt004qtsnvhf0i0q6s
slug: everything-you-need-to-know-about-arrays-in-python
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1655498730198/rAWigJInv.jpg
tags: python, array

---

# This article will teach you how to use arrays more efficiently when writing codes in Python.

Before we embark on this journey, let's clear up a little confusion: while arrays are not predefined in Python, we have an excellent substitute called Lists. So, don't worry, we have all the tools we need to explore the fascinating world of arrays in Python. Together, we'll start with simple beginner-level examples and gradually level up to more advanced concepts. So, buckle up and let's dive into the exciting realm of Python Lists, where arrays come to life!

## **What is an Array?**

Arrays serve as efficient containers to store multiple items or values within a single variable. If the concept seems puzzling, think of an array as a unique variable that can hold not just one but multiple values simultaneously. An analogy can be drawn by considering an array as a basket and its values as diverse types of fruits it can contain. Now that we've covered the basics, let's shift gears and delve into real-world examples of how arrays work their magic in practical scenarios. Brace yourself for a captivating journey into the realm of arrays!

## **How to use an Array.**

Let's say we have a list of fruits, storing them in a single variable would look like this:

```plaintext
fruit1 = "Strawberry"
fruit2 = "Banana"
fruit3 = "Mango"
```

The above example is the correct method of storing values inside a variable, which is totally fine and acceptable by Python. But what if we want to store about 100 fruits? that would definitely take a lot of time. So instead of having long lines of code in our Python file, we can simply make use of Arrays. Let us see how we can do that.

```plaintext
fruits = ["Strawberry", "Banana", "Mango"]
```

Do you see how simple and easy the above example is? That is what an Array is. Also note that it can store as much as possible values. Give it a try.

## How to access the values in arrays.

Now that we have a full idea of what an Array is and what it does. Let's see how we can access each element inside it.

To do that we need to make use of index(index is another word for number). Please note that index starts from 0 to 1 to 2 and so on and so forth. The next example will teach us how to access the first value in the array of fruits.

```plaintext
fruits = ["Strawberry", "Banana", "Mango"]
print(fruits[0])
```

The output of the above lines of code will be **Strawberry**. Remember we said the index starts from 0, so the first value in fruits will be index 0. To print out "Mango" we will simply replace 0 with 2.

## Length of Elements in an Array

When we have a lot of values in our array, we might lose count and become worried. The next example shows how we can know the number of values in our array no matter how many it is.

```plaintext
fruits = ["Strawberry", "Banana", "Mango"]
print(len(fruits))
```

The output of the above lines of code will be **3**. We are able to know the numbers of values in our array using the "**len**" function.

## Loops in Array

For us to loop through each item or access each item in our array we must use the "**for**" and "**in**" function. Lets see how we can implement this.

```plaintext
fruits = ["Strawberry", "Banana", "Mango"]
for x in fruits:
    print(x)
```

This program will print out all the values in fruits vertically **\["Strawberry", "Banana", "Mango"\]**

## Add and remove values in an Array

To add or remove a value from our array we do not have to type or delete a value every single time in our code. We can seamlessly do that anywhere in our program by simply calling the existing array and modifying it with some functions. First, let's see how we can add a value to our existing array

```plaintext
fruits = ["Strawberry", "Banana", "Mango"]
fruits.append("Grape")
print(fruits)
```

The above lines of code will simply print out **\["Strawberry", "Banana", "Mango", "Grape"\]**. This is made possible because we used the ".append()" function.

To remove an element from our array, we need to make use of the **".pop()"** or **".remove()"** function. The difference between these two functions is that **".pop()"** deletes the value using an integer but *".remove()"* deletes a using a string. Let's try them out.

```plaintext
fruits = ["Strawberry", "Banana", "Mango"]
fruits.remove("Banana")
print(fruits)
```

```plaintext
fruits = ["Strawberry", "Banana", "Mango"]
fruits.pop(1)
print(fruits)
```

The output of these two examples will be \["Strawberry", "Mango"\]

Below are other functions or methods you can use to make an array fully functional without too much lines of code.

* **index() Returns the index of the first element with the specified value**
    
* **clear() Removes all the elements from the list**
    
* **copy() Returns a copy of the list**
    
* **count() Returns the number of elements with the specified value**
    
* **extend() Add the elements of a list (or any iterable), to the end of the current list**
    
* **insert() Adds an element at the specified position**
    
* **reverse() Reverses the order of the list**
    
* **sort() Sorts the list**
    

I hope you find this piece of information educating. If you do, please do me a favor by hitting the like button and also do well to share with friends who are also learning.