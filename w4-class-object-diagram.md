# Week 4: Interpreting UML class/object diagrams

Tags: `W4` `UML diagrams` `class diagram` `object diagram`

# Q&As

## Association

**Q: Is bidirectional association equivalent to two unidirectional associations?**

**A:** No. Please refer to [this section](https://nus-cs2103-ay2324s1.github.io/website/schedule/week4/topics.html#design-modelling-modelling-structure-class-diagrams-basic) (scroll to navigability section) on the module website for more explanation/example on this.

[Example taken from the module website]
In the code below, there is a bidirectional association between the `Person` class and the `Cat` class i.e., if `Person` `p` is the owner of the `Cat` `c`, `p` it will result in `p` and `c` having references to each other.

```java
class Person {
    Cat pet;
    //...
}

class Cat {
    Person owner;
    //...
}
```
The code below has two unidirectional associations between the `Person` class and the `Cat` class (in opposite directions) because the breeder is not necessarily the same person keeping the cat as a pet i.e., there are two separate associations here, which rules out it being a bidirectional association.

```java
class Person {
    Cat pet;
    //...
}

class Cat {
    Person breeder;
    //...
}
```

## Composition & Aggregation

**Q: Can we use Aggregation to model the relationship between `Book` and `Chapter`**

**A:** Composition would be more appropriate in this case. It does not really make sense for a `Chapter` to exist without a `Book`. In this case, it is more accurate to model this relationship as *whole-part*.

**Q: Should we describe composition as 'when *whole* gets destroyed, *part* gets destroyed'**

**A:** This is the *side effect*. Conceptually composition is a *whole-part* relationship. 

**Q: Is it correct to say that both composition and aggregation have "has-a" relationship, because they both has something (e.g. `Category` has `Book`, `Book` has `Chapter`)**

**A:** It's not incorrect, but less informative (because it doesn't tell us how one differs from the other). We can also say they are both 'is associated with' relationships, which is not incorrect either, but even less informative (it doesn't tell us how these two differ from all other associations).

It's more accurate to describe that composition is *whole-part* and aggregation is *container-containee* since it also captures that composition is stronger than aggregation, and also captures the side effect (cascading deletion).

## Navigability

**Q: When class A has a reference to class B, the association between these two classes should be presented with the solid line and the arrow head indicating from A to B in the class diagram? Can there be any case just presenting the reference with the solid line without the arrow head (navigability)?**

**A:** Navigability is optional to show. If not shown, the diagram does not tell us which class has the reference. We only know that there is an association between the two classes.

**Q: If there is no navigability sign in an association, does this imply bidirectional navigability by default?**

**A:** As per UML, it can mean bidirectional but can also mean 'unspecified'. Need to decide based on the rest of the diagram e.g. if no navigability is shown anywhere in the diagram, it is more likely 'unspecified'. So, it is a bit confusing. To minimize such confusion, in this module we interpret the absence of arrow heads as 'navigability unspecified'.

## Multiplicity

**Q: What does it mean when multiplicity is not specified?**

**A:** It just means that multiplicity has been omitted due to reasons such as multiplicity has not been confirmed.

# Something to think about

These are something that you could try to think about when you are revising this topic. Feel free to discuss with your team/forum/me if you are not sure 😄

1. Differences between association and dependency?

2. Differences between bidirectional association and 2 unidirectional associations?

3. Differences between composition and aggregation?

4. Differences between association role vs association label?

5. What is the purpose of association class?

6. Differences between object and class diagram? (hint: which one can change over **time**)
