# Deepan Prabhu's Website


# How to craft programming Functions

I have been programming for more than 15 years, and i have written lots of code.
When you spend so much time on something, getting expertise is inbuilt :).

But currently programming has become a means of making money and I have moved away from the art.

I chose my passion ( computer science ) as my career so that I could cherish it every moment, but when working for someone as an engineer , its more of a business rather than an art.

Lately, i spent some time to think about what **functions** are and how to write them ? What is an appropriate mental model that is easy and apt for people to understand ?

## Crafting Functions

Functions in programming are indeed functions from mathematics.

For example, in mathematics, we describe a function that doubles a value as below,
f(x) = x*2;

1. f(x) is the name of the function.
2. x is an input, or in programming terms called a parameter.

The same function written in javascript is,

```javascript
function doubleX(x) {
  return x*2;
}
```
So a function has the name, **doubleX**, it takes one parameter, **x** and it gives back f(x).
So f(x) = x*2 in *mathematics* is doubleX(x) in javascript !!

Lets write a second function,

``` javascript
function doubleXAndAddY(x,y){
  int intermediate = 2 * x;
  int finalval = intermediate + y;
  return finalval;
}
```
The above function has 2 parameters, and gives back a value.

Now I am writing a third function with three parameters,

```javascript
function doubleXAndAddYAndAppendZ(x,y,z){
  int first = 2*x;
  int second = first + y;
  var third = second.toString() + String(z);
  return third;
}
```
The third function has 3 parameters, and does something more complex than the above functions !

We have seen three functions as examples, now to the **mental model** I am trying to convey here :P.

Functions in programming ( javascript here ) have a name, parameters and a return value ( of a particular type like may be an integer, or string.. )

1. Name - Choose a function name, that conveys the functionality.
2. Parameter names - Choose names, that convey the value they hold.
3. **Parameter Order** - If a function has 4 parameters, you can order them in 24 ways :). So how can we order them ?
   1. Order the parameters in the order in which they are to be utilized to arrive at the final result.
   2. In the doubleXAndAddYAndAppendZ, we are having the order of parameters as x, y and followed by z. We could have had y,x,z    too.
   3. But We double *x* first, use that value to add *y* and then append *z* to it. Hence from the functionality and how it is derived at, we arrive at the parameter order, as x,y, followed by z.
