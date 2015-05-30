# The Case against Java as your first programming language

First of all: I am biased. I started learning programming with the really high high-level programming languages. Ruby, Python, Haskell, well even PHP and Javascript. 

What you learn in those languages is different. Different from what you would learn in a programming language like C or Java. You don’t have to care about Pointers, References or Object Oriented Programming in the first place. These high-level programming languages let you forget that you actually work with the dumbest thing in the world: a computer. You can just start by fiddling around. These languages are merciful, especially ruby, where it is totally normal to have more than just one way to do things.

If you start to learn programming in Java, there is a lot of overhead. Think about it, you never seen a computer program before and now somebody wants you to write this.

```java
public class MyFirstProgramm {

    public static void main(String [] args) {
         System.out.println("Hello World");
    } 

}
```

Personally I would be terrified. What really bothers me are the things that you don’t need. You just wanted to print out the String `Hello World` to the console and now you are confronted with questions like „What the heck is a class“, „What is `static`“ and „What is it about those dots?“. You have to write all this stuff just to do such a simple task, compare that to a language like ruby or python where you can write:

```ruby
print "Hello World"
```

It can be so easy. You don’t have to explain what a class is, or a function you can just start smoothly. Later on after understanding how to write simple programs you can learn what object oriented programming is, or how data structures work. Once you understood those things, it’s easy to teach people more low-level languages like Java. One of the big advantages of ruby or python is the ability to see your progress from a very early stage on. Consider how easy it is to draw a rectangle on a canvas in python and what you have to know. While in Java you are confronted with the horrible JavaFx Api. 