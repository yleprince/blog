---
title: "Scala `case classes` explained"
date: 2023-01-10T017:00:47Z
summary: "Description of case classes in scala"
author: chat-gpt
showToc: true
TocOpen: true
TocSide: 'left'
---

Scala is a powerful programming language that is well-suited for building large, complex software systems.
One of the features of Scala that makes it particularly well-suited for this task is its support for case classes.
In this article, we'll take a closer look at case classes and how they can be used to write clean, maintainable code.

At a high level, a `case class` is a special kind of class that is designed to be used in the context of pattern matching.
A `case class` is defined using the `case` keyword, which automatically generates several useful things for you:
- A primary constructor, which defines the fields of the `case class`
`equals` and `hashCode` methods that are based on value, not reference identity
- A `toString` method that provides a useful string representation of the `case class` instance
copy method
- An `apply` method, which allows you to create an instance of the `case class` without using the `new` keyword.
- An `unapply` method, which allows the `case class` to be used in pattern matching.

Here's an example of a `case class` definition:

```scala
case class Point(x: Int, y: Int)
```

With this definition, you can create instances of the `case class` like this:

```scala
val p1 = Point(1, 2)
val p2 = Point(3, 4)
```

You can also access the fields of a `case class` instance using the dot notation:

```scala
val x = p1.x
val y = p1.y
```

One of the most powerful features of case classes is that they can be used in pattern matching.
Here's an example of how you might use a `case class` in a pattern match:

```scala
val point = Point(1, 2)
point match {
  case Point(x, y) => println(s"x = $x, y = $y")
  case _ => println("Not a Point")
}
```

The above pattern match will output "x = 1, y = 2", because the point variable matches the pattern Point(x, y).

Another feature of `case class` is `copy` method which is used to create a new instance of `case class` with some modifications to the original instance.

```scala
val p2 = p1.copy(x = 3)
```

p2 will be a new instance of Point class with value x = 3 and y = 2

In summary, case classes are an incredibly powerful feature of Scala that makes it easy to write code that is both clean and maintainable.
With case classes, you can define simple classes that have a useful `toString` representation,
and you can use them in pattern matching to write expressive, powerful code.

As you continue to work with Scala, case classes will become an essential tool in your toolbox, so it is a good idea to get familiar with them early on.

----

### Comparison `case class` vs `case object`

The main differences between `case class` and `case object` are:
- 1. `case class` has constructor parameters and `case object` doesn't have.
- 2. `case class` creates instances while `case object` creates singleton instances
- 3. `case class` instances are compared by value while `case objects` are compared by reference.

Both are used in pattern matching but `case class` instances are used more frequently in pattern matching.

👉 You should use `case class` if you want to define a class with data, and you should use `case object` if you want to define a singleton object with no data.
