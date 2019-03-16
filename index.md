# Deepan Prabhu's Website


# How to craft programming Functions

I have been programming for more than 15 years, and i have written lots of code.
When you spend so much time on something, getting expertise is inbuilt :).

But currently programming has become a means of making money and I have moved away from the art.

I chose my passion ( computer science ) as my career so that I could cherish it every moment, but when working for someone as an engineer , its more of a buisness rather than an art.

Lately, i spent some time to think about what **functions** are and how to write them ? What is an appropriate mental model that is easy and apt for people to understand ?

Functions in programming are functions from mathematics.

For example, in mathematics, we describe a function that doubles a value as below,
f(x) = x*2;

The same function written in javascript is,

```javascript
function doubleX(x) {
  return x*2;
}
```
So a function has a name, **doubleX**, it takes one parameter, **x** and it gives back f(x).

Lets write a second function,

``` javascript
function doubleXAndAddY(x,y){
  int intermediate = 2 * x;
  int finalval = intermediate + y;
  return finalval;
}
```

Now I am writing a third function with three parameters,

```javascript
function doubleXAndAddYAndAppendZ(x,y,z){
  int first = 2*x;
  int second = first + y;
  var third = second.toString() + String(z);
  return third;
}
```
