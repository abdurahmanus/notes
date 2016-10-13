# Table of Contents

- [Floating point numbers](#floating-point-numbers)
    - [Types of Number](#types-of-number)
    - [Decimal representation](#decimal-representation)
    - [Binary representation](#binary-representation)
    - [Decimals are innacurate](#decimals-are-innacurate)

# Floating point numbers

## Types of Number

- **real numbers**

All numbers on the number line. [(wiki)](https://en.wikipedia.org/wiki/Real_number)

- **integers** 

Integer - is a number that can be written without a fractional component. The set of integers consists of zero (0), the natural numbers (1, 2, 3, …), also called whole numbers or counting numbers, and their additive inverses (the negative integers, i.e. −1, −2, −3, …). [(wiki)](https://en.wikipedia.org/wiki/Integer)

- **fractions**

Fraction - not an integer. A fraction (from Latin fractus, "broken") represents a part of a whole or, more generally, any number of equal parts. [(wiki)](https://en.wikipedia.org/wiki/Fraction_(mathematics))

- **rational numbers**

A rational number is any number that can be expressed as the quotient or fraction p/q of two integers, a numerator p and a non-zero denominator q. Since q may be equal to 1, every integer is a rational number. The set of all rational numbers, often referred to as "the rationals", is usually denoted by a boldface **Q**; it was thus denoted in 1895 by Giuseppe Peano after quoziente, Italian for "quotient". [(wiki)](https://en.wikipedia.org/wiki/Rational_number)

- **irrational numbers** 

An irrational number is a real number that cannot be expressed as a ratio of integers, i.e. as a fraction. Therefore, irrational numbers, when written as decimal numbers, do not terminate, nor do they repeat. For example, the number π starts with 3.14159265358979, but no finite number of digits can represent it exactly and it does not end in a segment that repeats itself infinitely often. The same can be said for any irrational number. [(wiki)](https://en.wikipedia.org/wiki/Irrational_number)

<img src="/images/math_for_programmers/numbers.png">

## Decimal representation

|100's|10's|1's|.|1/10th's|1/100th's|
|---|---|---|---|---|---|
| | |1|.|5| |

= 1 * 1 + 5 * 1/10 = 1 1/2

Move one column to the right => divide value by 10

## Binary representation

|4's|2's|1's|.|1/2th's|1/4ths's|
|---|---|---|---|---|---|
| | |0|.|1|1|

= 1 * 1/2 + 1 * 1/4 = 3/2

Move one column to the right => divide value by 2

## Hexadecimal representation

|16's|1's|.|1/16th's|1/32th's|
|---|---|---|---|---|
| |0|.|8| |

= 8 * 1/16 = 1/2

Binary <-> Hexadecimal

<img src="/images/math_for_programmers/fractions_in_hexadecimal.png">

## Decimals are innacurate

Most numbers can't be exactly represented

<img src="/images/math_for_programmers/infinite_numbers.png">

If there are an infinite number of numbers between any two points, then to represent all of them exactly you would need an infinite number of bits. On a 64-bit machine, you have just 64 bits. So, we can represent only a finite number of numbers. **Almost every number on the number line can't be represented exactly on a computer that has only a finite number of bits**

<img src="/images/math_for_programmers/innacurate_storing.png">

Even relatively simple numbers can't be stored exactly. 1/3 = 0.333333333333...

### The rule in decimal

- **1/n can be represented exactly if the only prime factors of n are 2 and 5** (Because 10 = 2 * 5)
- **can represent exactly**
    - 1/20 = 0.05 (because 20 = 2 * 2 * 5)
    - 1/50 = 0.02 (because 50 = 2 * 5 * 5)
- **can't represent exactly**
    - 1/6 = 0.166666... (because 6 can't be factored using 2's and 5's)
- **if you can represent 1/n exactly then you can represent 2/n, 3/n etc. exactly**
    - 2/20, 3/20, 4/20 etc. can be exactly represented

### Fractions in binary

- **even fewer fractions can be represented**
    - the only fractions that can be are fractions of the form something/2^n (1/2, 1/4, 1/8, 1/16, 3/8, 3/4 ...)
- **exact in decimal, not in binary**
    - 1/5 = 0.2 = *b*0.001100110011... = *0x*3333333333...
- **can't represent exactly in binary or hex**
    - 0.7
    - 0.3
    - 0.9
    - etc.
- **irrationals can never be represented exactly in any base!**

### Conclusion

- **you can store exactly:**
    - integers
    - a very small proportion of rational numbers
    - nothing else


