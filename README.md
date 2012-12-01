*REDUCT*

Test driven development is an increasingly popular method of developing programs. Developers using this methodology write programs in their language of choice and specify the intended behavior of their programs by writing a series of programmatic tests. These tests are typically structured as a set of inputs and their respective desired outputs.

REDUCT is the apotheosis of the test driven development methodology. It is test driven development reduced to its purest essence, the wine to a testing framework's grape juice.

Furthermore, REDUCT is a simple declarative programming language. In REDUCT you only specify what a program does, not how it does it.

Even an utter novices can write a REDUCT program, sometimes even correctly.

Sounds to good be true? Lets take a look.

**Syntax and Semantics**

Here is an example REDUCT program that may specify the factorial function.

```
[0, 1, 3, 5, 20]
[1, 1, 6, 120, 2432902008176640000]

```

A REDUCT program consists of two lines. Each line is a JSON array containing arbitrary JSON objects. The first line represents sample inputs. The second line represents corresponding outputs. The correct behavior on other inputs is inferred by the evaluator.

Thus the above program specifies a program that returns '1' for the input '0', '1' for the input '1', '3' for the input '6', '120', for the input '5' and '2432902008176640000' for the input '20'.


**Falsifiablity**

Those of you who are still reading might have a question. How on Earth do we know that's a factorial function? It's just some examples!

There are two different directions from which we can approach a proof.

***Argument from observation***

It so happens that the only way to verify the output of a REDUCT interpreter is to declare an additional input/output pair, which by definition the program will evaluate correctly. Thus, for all observable answers, this REDUCT program matches the factorial function. QED

***Argument from definition***
It passes the tests. The rest of the behavior is inferred correctly.


Note that REDUCT provides exactly the same assurances as more traditional and widely used test driven design systems.

**REDUCT in REDUCT**

The following program specifies a REDUCT interpreter written in REDUCT, but only if you want it to.
```
[]
[]
```

Do you want it?

**REDUCT outside REDUCT**

A correct REDUCT interpreter that allows testing of inputs outside the test set is an open research problem. We think this is a fascinating opportunity to join the techniques of machine learning with the principles of programming language theory.

But uhhh, if you don't care about that requirement, you could use a hash table. Cheater.
