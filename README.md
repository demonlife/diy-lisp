## DIY Lisp 

> batteries included, some assembly required

In this tutorial/workshop we'll be implementing our own little language, more or less from scratch. 

By the end of the tutorial you will be the proud author of a programming language, and will hopefully better understand how programming languages work  on a fundamental level.

### What we will be making

We will make a relatively simple, but neat language. We aim for the following features:

- A handful of datatypes (integers, booleans and symbols)
- Variables
- First order functions with lexical scoping
- That nice homemade quality feeling

We will *not* have:

- A proper type system
- Error handling
- Good performance
- And much, much more

The language should be able to interpret the following code by the time we are done:

```lisp
;; Some example lisp code. By the end of the tutorial, our Lisp will be
;; able to run this.

;; To run the code:
;;
;;    ./diy example.diy
;;

(define fact 
    ;; Factorial function
    (lambda (n) 
        (if (<= n 1) 
            1 ; Factorial of 0 is 1, and we deny 
              ; the existence of negative numbers
            (* n (fact (- n 1))))))

;; When parsing the file, the last statement is returned
(fact 5)
```

The syntax is that of the languages in the Lisp family. If you find the example unfamiliar, you might want to have a look at [a more detailed description of the language](parts/language.md).

### Prerequisites

Before we get started, make sure you have installed [Python](http://www.python.org/) and [Pip](https://pypi.python.org/pypi/pip). 

Then install `nose`, the Python test framework we'll be using.

```bash
pip install nose
```

*Optional: If your are familiar with [virtualenv](http://www.virtualenv.org/en/latest/) you might want to do this in a separate pyenv.*


### Get started!

The workshop is split up into seven parts. Each consist of an introduction, and a bunch of unit tests which it is your task to make run. When all the tests run, you'll have implemented that part of the language.

Have fun!

- [Part 1: parsing](parts/1.md)
- [Part 2: evaluating simple expressions](parts/2.md)
- [Part 3: evaluating complex expressions](parts/3.md)
- [Part 4: working with variables](parts/4.md)
- [Part 5: functions](parts/5.md)
- [Part 6: working with lists](parts/6.md)
- [Part 7: using your language](parts/7.md)
