# ❗

> Already it stopped to think about how the logical NOT operator (!) works at the computational level?

## The idea

Given the pressupost of that the computer understands 0 and 1 and arithmetical cáculos, I and my friend <a href="https://github.com/GabrielBibiano" target="_blank">Gabriel Bibiano</a> create this repository only with the intention of a joke: try to explain how does logical not operator work at the mathematical level in a function.

## The Logical Not Operator (!)

As it is no longer surprising, ! is a logical operator that represents the negation (inverse) of the current variable. If it is true, it becomes false, and vice versa.

``` js
  !true         // false
  !false        // true
  !1            // false
  !0            // true
  !19           // false
  !undefined    // true
  !!true        // true
  !function(){} // false
  !NaN          // true
  .
  .
  .
```

## It's just an if

That was the initial inquiry I proposed, but my friend claimed that computing does not understand conditional structure at low level, but only binaries and arithmetic calculations. So we had to explain at the mathematical level.

## 0 and 1

The computer understands only 0 (false) and 1 (true). So the formula for this is:
> 1-n

Note that if we want to deny the 0:

|            | Operation | Result |
|:----------:|:---------:|:------:|
|   Logical  |   !false  |  true  |
| Arithmetic |    1-0    |    1   |

And if we want to deny the 1:

|            | Operation | Result |
|:----------:|:---------:|:------:|
|   Logical  |   !true   |  false |
| Arithmetic |    1-1    |    0   |

## The Function

``` js
  const not = n => Boolean(1-(Number(Boolean(n))));
```

## The behavior is similar to the ❗

``` js
  not(true)         // false
  not(false)        // true
  not(1)            // false
  not(0)            // true
  not(19)           // false
  not(undefined)    // true
  not(not(true))    // true
  not(function(){}) // false
  not(NaN)          // true
  .
  .
  .
```

## Note

We are not computer experts, but we always want to understand the basis of everything. These inquiries exposed in this README are just our considerations on how the logic behind the logical not operator. If something is wrong, correct us.