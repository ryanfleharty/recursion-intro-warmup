[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly)

# Introduction to Recursion

A first look at recursion

#### Learning Objectives

- Use recursion to loop over an array
- Be able to use either parameters or a parent scope to hold on to data

#### Prerequisites

- Basic javascript

---

## Getting Started

1. Clone this repository

1. A recursive function is simply a function that keeps calling itself until the desired output has been reached. The necessary components of recursion are:
    - A break case. This is usually an if check that determines whether the desired end state has been reached, and if so, returns the answer.
    - Advancing the solution towards the break case. Much like a while loop, we must be sure that a recursive function will advance towards the break case, otherwise it may recurse forever.
    - Recurse. If the end state has not been reached, the recursive function will be called inside of itself.

1. Here is an example of recursively counting to 100:
    <code> const rCount = (num = 0) => {
        if(num === 101){
            return num;
        } else {
            console.log(num);
            num++;
            return rCount(num)
        }
    }
    </code>

1. As you can see, the recursive function is continuously given the parameter num in order to keep track of how far along the function has gotten. An alternative way of keeping track of our number is to wrap the recursive function inside of a non-recursive function's scope.
    <code> const count = () => {
        let num = 0;
        const rCount = () => {
            if(num == 101){
                return num;
            } else {
                console.log(num);
                num++;
                return rCount();
            }
        }
        return rCount();
    }
    <code>

## Deliverables

Using these two patterns, write a recursive function that will find the maximum value in a given array of numbers.

You can warm up by writing a simpler function that just console.logs each element in a given array.

## Bonus algorithms

Some classic recursion examples include calculating the Xth number in the Fibonacci sequence, calculating the factorial of a number, and using binary search to scan a sorted array for a specific value. 

*Copyright 2018, General Assembly Space. Licensed under [CC-BY-NC-SA, 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)*