---
layout: post
title:  Fluent Interfaces in Ruby
date:   2015-07-13 00:00:00
tags: [fluent, interfaces, ruby, martin, fowler, java, expressive]
---
Fluent Interfaces became a standard in many programming languages. They make it
easy to build DSLs that read like normal sentences. Take a look at this code example

```ruby
User.where(:username => 'Steven').all
```

Even if you never wrote a single line of code you can grasp what is going on.
Someone wants to get all the users where the username is "Steve". That seems
legit. In the Ruby world we are spoiled by all the syntactic sugar the
language provides. Blocks, procs, optional parantheses. It's easy to write
expressive code in such a beautiful language. In Java people have to fight the
language to write beautiful code. All the getters, all the setters. The
conventions make it hard to write meaningful code. But somehow a little rose
blossomed in this wasteland. Fluent Interfaces. Instead of writing

```java
Point p = new Point();
p.setX(1);
p.setY(2);
```

You can now write code that reads more like a specification.

```java
Point p = new Point().x(1).y(2);
```

It is easy to write that in a language like Java. Different method signatures
can have different return values. So it's easy to write something like this:

```java
public Point x(int xValue) {
  // code
} 
public int x() {
  // code
}
```

The compiler can figure out which method to call and which return value to
expect. Back to Ruby: You can't do that. Ruby doesn't really know the
concept of overloading. But who needs overloading if you can have default
arguments.

```ruby
def x(x_value = nil)
  if x_value.nil?
    @x_value
  else
    @x_value = x_value
    self
  end
end
```

That is truely ugly. Default arguments, If statements and if you want to write
more than one of those methods it gets tedious to copy and paste the same code
over and over again. Essentially you are doing the work of the java compiler.
Checking if an argument is given and then doing the right thing. We are in
Ruby, we should'nt have to write so much boilerplate code. And we don't have to.

We can write a module that does all the work for us.

```ruby
module FluentInterface
  def fluent_accessor(name)
    define_method(name.to_sym) do |v=nil|
      if(v.nil?)
        self.instance_variable_get("@#{name}")
      else
        self.instance_variable_set("@#{name}", v)
        self
      end
    end
  end
end
```

So essentially what we are doing is this. If someone calls the `fluent_accessor`
method we define a new method on the fly that does exactly the same as the
code above. But that's pretty unflexible. Sometimes the method name doesn't
match the instance variable name. So we should also be capable of injecting
the instance variable name

```ruby
# To keep it short I use the abbreviation va
# instead of variable
module FluentInterface
  def fluent_accessor(name, va_name = nil)
    define_method(name.to_sym) do |v=nil|
      va = va_name.nil? ? name : va_name
      if(v.nil?)
        self.instance_variable_get("@#{va}")
      else
        self.instance_variable_set("@#{va}", v)
        self
      end
    end
  end
end
```

Now we can write fluent interfaces without the need to copy and paste all
the code over and over again

```ruby
class Line
  extend FluentInterface

  fluent_accessor :from, :start_point
  fluent_accessor :to, :end_point
end

l = Line.new.from([0, 0]).to([1, 1])

l.from # => [0, 0]
l.to   # => [1, 1]
```

So you see, fluent interfaces which are a natural fit for statically
typed languages also enrich the world of dynamically typed
languages like Ruby with their expressive syntax.