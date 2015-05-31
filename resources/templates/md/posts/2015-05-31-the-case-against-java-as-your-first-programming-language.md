{:title "A Post"
 :layout :post
 :tags  ["not fetch"]}
# The Case against Java as your first programming language

First of all: I am biased. I started learning programming with the really high high-level programming languages. Ruby, Python, Haskell, well even PHP and Javascript. 

What you learn in those languages is different. Different from what you would learn in a programming language like C or Java. You don’t have to care about Pointers, References or Object Oriented Programming in the first place. These high-level programming languages let you forget that you actually work with the dumbest thing in the world: a computer. You can just start by fiddling around. The languages are merciful, especially ruby, where it is totally normal to have more than just one way to solve a problem.

~~Some python folks are now on a rant because there’s only one way to do it right, but guess what there’s always more than one way to solve a problem. Deal with it.~~

If you start to learn programming in Java, there is a lot of overhead. Think about it, you never seen a computer program before and now somebody wants you to write this.

```java
public class MyFirstProgramm {

    public static void main(String [] args) {
         System.out.println("Hello World");
    } 

}
```

Personally I would be terrified. People say that Java is an easy language, while this example shows the complete opposite. Sure, if you are familiar with object oriented programming you can understand what is going on, but as a beginner you would be definitely overwhelmed. Compare that to a language like Ruby

```ruby
puts "Hello World"
```

Look how simple it is. All it takes is a text editor and 1 line of code. That’s it. Your students have written their first program, and the best part is you didn’t have to explain what class, static, void and all these dots do. You can concentrate on the concepts you want to teach and not the language. When explaining the different data types you can be sure to explain it without the need of technical details like the internal implementation of a string or the binary representation of an integer. These are important topics of course, but at the moment you want to show how to write a simple program, not how a computer works. Higher level languages abstract these implementation details away, so that nobody has to care about overflow errors in such a language. Programming is a complex subject, but it is also fun to fiddle around and see instant results and that’s possible in those languages. 

After grasping a first glance at how to write simple programs and how basic OOP works, it is easy to adapt your mind to a statically typed language like Java. You are now familiar with object orientation, types, classes, and after a while you will figure out that it is not the best idea to represent the 1000th fibonacci number in an int variable. But you started smoothly and had instant successes with your first programming language, and that kept you from thinking that programming is the most complex thing in the world. 

I don’t suggest to dumb down the programming part in a computer science degree, but instead to concentrate on the ideas behind programming, and the mental models it is build around, not overly complex languages. Programming Languages like Java, C#, C++ and C have their right to exist and should be taught, but please not as the first programming language. We can do better than that.   

Especially in academia I sometimes have the feeling, that there’s a bizarre love to express easy things in a complex manner. I don’t know who came up with the idea to let freshman implement math formula as computer science assignments, but it certainly is a more than just foolish thought, to believe that a challenging subject like programming gets any easier by combining it with higher mathematics. We should stop that and show programming as the fun it can be and not the enterprise-grade bullshit you made it.
