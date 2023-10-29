# Week 10: Evaluating sample DG diagrams

Tags: `W10` `DG` `UML diagrams` 

# Q&As

**Q: In sequence diagram, we shouldn't have a method chain. How should we draw this part of the diagram?**

![91F604F2-C0AE-4749-8C4B-67FB70DAA43B](https://github.com/Punpun1643/ay2324s1-cs2103t-tutorial-materials/assets/60144099/4a4d5741-abc4-4877-808b-1519a6c41b90)

**A:** 
The correct diagram is as follow:

![E523098A-C4D4-4A92-B130-3034E4F2268F](https://github.com/Punpun1643/ay2324s1-cs2103t-tutorial-materials/assets/60144099/de07a1f3-93fa-4c75-b6f2-f58adb2215b0)


Since explicitly:

- Model is calling the `getDish` method of `Dummy` (a `Dish` is returned)
- Model is calling the `getCalories` method of Dish (a `MealLog` is returned)
- Model is calling the `getValue` method of `MealLog`


Note that this is **not correct**:

![2D11CB54-316D-43C9-9B8E-CB4E5F1CDC27](https://github.com/Punpun1643/ay2324s1-cs2103t-tutorial-materials/assets/60144099/a4f97f2a-131e-4e9c-8a3a-728d53f50505)


Since this would mean:

- Model is calling the `getDish` method of `Dummy`
- Inside the `getDish`, `getCalorie` is called, and so on.


**Q: In sequence diagram, is it possible to show that a method is called on the object returned by another method?**

**A:** You can give a name to the object e.g., `d: Dish` and show that `d` as the return value in the previous method. 

![3E07EF47-8EDE-4E3C-A5F9-F99DFB09F177](https://github.com/Punpun1643/ay2324s1-cs2103t-tutorial-materials/assets/60144099/ee6cf42b-e429-4171-9f09-5540229d9397)


**Q: In activity diagram, can a single join node represent multiple join nodes?**

![0CB7ADCB-DE1F-4B53-97FC-ECD85D488538](https://github.com/Punpun1643/ay2324s1-cs2103t-tutorial-materials/assets/60144099/4cc6b3f4-e191-4369-858e-42e256e6eec0)

**A:** Yes, ok to use a single join node to join multiple fork nodes.


**Q: Is it ok to have an additional layer of fork and join like in the example below?**

![CC2608AE-F240-4957-809C-5406E27F173C](https://github.com/Punpun1643/ay2324s1-cs2103t-tutorial-materials/assets/60144099/f241c61e-b1bb-4933-8d4a-01c079db7c62)

**A:** Yes, the behaviour is still the same, since the preparation task and payment task still start and end at the same point in time.

