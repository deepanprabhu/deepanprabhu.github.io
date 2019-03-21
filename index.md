# How to craft programming Functions

All programming languages allow you to create functions. When i first saw people writing functions and reusing them, i felt they are very powerful and I should also *create* one. And when i wrote my first function, i felt so powerful !!

In this article, I am sharing some experience, mental model and examples on how to compose a function. 

## Crafting Functions

Functions in programming are indeed functions from mathematics.

For example, in mathematics, we describe a function that doubles a value as,
f(x) = x*2;

1. f(x) is the name of the function.
2. x is an input, or in programming terms called a **parameter**.

The same function written in javascript is,

```javascript
function doubleX(x) {
  return 2 * x;
}
```
So the above function has the name, **doubleX**, it takes one parameter, **x** and it gives back f(x).
So f(x) = x\*2 in *mathematics* is doubleX(x) in javascript !!

Lets write a second function,

``` javascript
function doubleXAndAddY(x,y){
  int intermediate = 2 * x;
  int finalval = intermediate + y;
  return finalval;
}
```
The above function has 2 parameters (inputs), and gives back the output of the function.
So f(x) = 2\*x + y in *mathematics* is doubleXAndAddY(x,y) in javascript !!

Now I am writing a third function, but now with three parameters,

```javascript
function doubleXAndAddYAndAppendZ(x,y,z){
  int first = 2 * x;
  int second = first + y;
  // the above are numbers, but the final operation of appending is on strings.
  var third = second.toString() + String(z);
  return third;
}
```
The third function has 3 parameters, and does something more complex than the above 2 functions !

We have seen three functions as examples, now to the **mental model** I am trying to convey here :P.

Functions in programming have a name, bunch of parameters and a return value ( of a particular type like may be an integer, or string.. )

1. Name - Choose a function name, that conveys the functionality. Example, **areaOfSquare**
2. Parameter names - Choose parameter names, that convey the value they hold. Example, function areaOfSquare(length, breadth) {}
3. **Parameter Order** - If a function has 4 parameters, you can order them in 24 ways :). So what is the best way to order them when specifying a function ?
   1. Order the parameters in the order in which they are to be utilized/used to arrive at the final result.
   2. In the doubleXAndAddYAndAppendZ, we are having the order of parameters as x, y and followed by z. We could have had y,x,z    too.
   3. But We double *x* first, use that value to add *y* and then append *z* to it. Hence from the functionality and how it is derived at, we arrive at the parameter order, as x,y, followed by z.
