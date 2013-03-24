---
layout: post
title: Polymorphism of java
category: java
tags: java
---
{% include JB/setup %}

The java polymorphism is actually a upcasting. Look like this:

```java
Animal aml = new Dog();
```
The Dog class must be inherited from the Animal class, and they are all having a same method. For example: the eat() method.  

When the aml object use the eat() method, the eat method of Dog class will be called. This is the polymorphism.  

But, things are not simply. There are some pitfalls like fields and static methods. They cannot be polymorphic.

```java
//the pitfall of the fields
class Super {
    public int field = 0;
    public int getField() { return field; }
}
class Sub extends Super {
    public int field = 1;
    public int getField() { return field; }
    public int getSuperField() { return super.field; }
}
public class FieldAccess {
    public static void main(String[] args) {
        Super sup = new Sub(); // Upcast
        System.out.println("sup.field = " + sup.field +
            ", sup.getField() = " + sup.getField());
        Sub sub = new Sub();
        System.out.println("sub.field = " +
        sub.field + ", sub.getField() = " +
        sub.getField() +
        ", sub.getSuperField() = " +
        sub.getSuperField());
    }
} /* Output:
sup.field = 0, sup.getField() = 1
sub.field = 1, sub.getField() = 1, sub.getSuperField() = 0
*///:~

```

**static** methods are associated with the class, and not the individual objects.
