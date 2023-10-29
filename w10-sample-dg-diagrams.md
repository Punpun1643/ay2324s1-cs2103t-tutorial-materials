# Week 10: Evaluating sample DG diagrams

Tags: `W10` `DG` `UML diagrams` 

# Q&As

**Q: In sequence diagram, we shouldn't have a method chain. How should we draw this part of the diagram?**

**A:** 
The correct diagram is as follow:


Since explicitly:

- Model is calling the `getDish` method of `Dummy` (a `Dish` is returned)
- Model is calling the `getCalories` method of Dish (a `MealLog` is returned)
- Model is calling the `getValue` method of `MealLog`


Note that this is **not correct**:


Since this would mean:

- Model is calling the `getDish` method of `Dummy`
- Inside the `getDish`, `getCalorie` is called, and so on.


**Q: In sequence diagram, is it possible to show that a method is called on the object returned by another method?**

**A:** You can give a name to the object e.g., `d: Dish` and show that `d` as the return value in the previous method. 

**Q: In activity diagram, can a single join node represent multiple join nodes?**

**A:** Yes, ok to use a single join node to join multiple fork nodes.


**Q: Is it ok to have an additional layer of fork and join like in the example below?**


**A:** Yes, the behaviour is still the same, since the preparation task and payment task still start and end at the same point in time.

