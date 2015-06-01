---
layout: post
title:  "The case against Java as a first programming language"
date:   2015-05-31 00:00:00
---

**First of all: I am biased. I started learing programming with the really
high high-level programming languages. Ruby, Python, Haskell, well even PHP
and Javascript.**

What you learn in those languages is different. Different from what you would
learn in a programming language like C or Java. You don’t have to care about
pointers, references or object oriented programming in the beginning. These
high-level programming languages let you forget that you actually work with
the dumbest thing in the world: a computer. You can just start by playing
about. The languages are merciful, especially ruby, where it is totally normal
to have more than just one way to solve a problem.

<!--~~Some python folks are now on a rant because there’s only one way to do it right, but guess what there’s always more than one way to solve a problem. Deal with it.~~-->

If you start to learn programming in Java, there is a lot of overhead. Think
about the classical Hello World example.

```java
public class MyFirstProgram {

    public static void main(String [] args) {
         System.out.println("Hello World");
    }

}
```

Personally I would be terrified. People say that Java is an easy language,
while this example shows the complete opposite. Sure, if you are familiar with
object oriented programming you can understand what is going on, but as a
beginner you would be definitely overwhelmed. Compare that to a language like
Ruby

```ruby
puts "Hello World"
```

Look how simple it is. All it takes is a text editor and 1 line of code.
That’s it. Your students have written their first program, and the best part
is you didn’t have to explain what class, static, void and all these dots do.
You can concentrate on the concepts you want to teach and not the language.
When explaining the different data types you can be sure to explain it without
the need of technical details like the internal implementation of a string or
the binary representation of an integer. These are important topics of course,
but at the moment you want to show how to write a simple program, not how a
computer works. Higher level languages abstract these implementation details
away, so that nobody has to care about overflow errors. Programming is a
complex subject, but it is also fun to play around with the language and see
instant results and that’s possible in such an environment. It's not necessary
to use everything a higher level language provides, like the syntactic sugar
of an ".each" loop in ruby, you can still use the universally accepted old-
school imperative way with a for loop to iterate over an array.

But after grasping a first glance at how to write simple programs and what
object oriented programming is about, it is easy to adapt the mind to a
statically typed language like Java. Students are now familiar with the
fundamental concepts of programming and after a while they will figure out
that it is not the best idea to represent the 1000th fibonacci number as an
int variable or how costly a resizable array can be. They will be grateful for
all the heavy lifting the programming language did to keep the quirks of
computers out of sight. In the end everyone had a more pleasant experience,
teachers because they are not compelled to skip questions about the weird
"public static void main" syntax and students because of a smooth start and
instant successes.

I don’t suggest to dumb down the programming part in a computer science
degree, but instead to concentrate on the ideas behind programming, and the
mental models it is build around, not the quirks of overly complex languages.
Java, C#, C++ and C are all very powerful and one should learn how to programm
in them, but please not as the first programming language. We can do better
than that.

Especially in academia I sometimes have the feeling, that there’s a bizarre
love to express easy things in a complex manner. I don’t know who came up with
the idea to let freshman students implement math formulae as computer science
assignments, but it certainly is a more than just foolish thought, to believe
that a challenging subject like programming gets any easier by combining it
with higher mathematics. We should stop that and show programming as the fun
it can be and not the enterprise-grade bullshit we turned it into.
