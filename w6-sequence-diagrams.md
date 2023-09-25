# Week 6: Interpreting UML sequence diagrams

Tags: `W6` `UML diagrams` `sequence diagram`

# Q&As
![9B287FEF-D13C-41C6-BBFE-D67DE0CB0429](https://user-images.githubusercontent.com/60144099/190624024-3447bced-9dec-42a0-bb89-6e262c9c8e14.png)

**Q: Is it correct to interpret that the `main` method calls the `producePrototype()` method of m?**

**A:** No. We do not know who is calling the `producePrototype` since it is not specified in the diagram. 

The precise way of describing this should be: an *unspecified object* calls the `producePrototype()` method of m.

**❌ Common misconception:** The `main ` method calls the `producePrototype()` method.

![4C405176-D998-46A4-87E8-320D7EA126B5](https://user-images.githubusercontent.com/60144099/190624123-65f37e9e-59bb-435d-a16e-7a317d29263c.png)

**Q: Are there any differences between the first and second activation bar?**

**A:** Yes. The first one is attached to the box, representing a constructor of a class. 

The second one is just a normal activation bar. 

They both represent something being activated though.

**❌ Common misconception:** No difference, just one is called before the other.

**Q: Does italics in sequence diagram represent abstact method?**

**A:** No. Italics does not mean anything in sequence diagram. It does not represent *abstract method*. 

Italics does represent abstract method in *class diagram* though. You can revise your *class diagram* [here](https://github.com/Punpun1643/cs2103t-tutorial-materials/blob/master/week4-object-class-diagrams.md#week-4-interpreting-uml-classobject-diagrams).

**❌ Common misconception:** It represents *abstract method*.

**Q: Is it OK to omit the *return arrow*?**

**A:** Yes. It does not affect anything, and does not change the meaning of the diagram. The *return arrow* is optional in sequence diagram.

**❌ Common misconception:** Omitting means the method does not return anything. 

![37A2585E-3EFC-43C3-9DEF-A3BEE73FFC4E](https://user-images.githubusercontent.com/60144099/190624664-253af920-6ba3-4193-bac7-e97c7c0a86d8.png)

**Q: If we omit the return arrow, does it mean that `stressTest()` method return nothing?**

**A:** We do not know. Since nothing is being written at the return arrow, it could be that it is retuning something, or it could be that it does not return anything.

**Q: So since in this case we have a return arrow, does it mean that the `stressTest()` method return something?**

**A:** Same answer as above.

**❌ Common misconception:** Return arrow *must* mean the method is retuning something.

**Q: In the sequence diagram, for any void type of method, can we use a return arrow?**

**A:** Yes.

![9356DACA-DC60-4DD5-98A7-1D3304BE5AB8](https://user-images.githubusercontent.com/60144099/190624284-6dc4c310-07b1-47cd-81a1-a601c8aa076c.png)

**Q: In this diagram, the return arrow at the bottom shows which value will be returned. In this case, is the return arrow omittable?**

**A:** No. As the text is an add-on to the arrow, the text should not appear without the arrow.

- Omit everything: OK
- Show arrow only: OK
- Show arrow and text: OK
- Show text but not arrow: not OK

**Q: Although the use of a return arrow is technically optional, are there any situations where it becomes necessary? Alternatively, would it be advisable to include it for enhanced clarity in the sequence diagram?**

**A:** As is the case for all optional elements, they are to be used if they add value to the purpose of the diagram and can be omitted when it results in a simpler diagram without affecting the purpose of the diagram. For example, the return arrow needs to be included if there is a return value AND the return value is relevant to the purpose of the diagram.

**Q: Is it possible to show exceptions in a sequence diagram**

**A:** It is not possible (and not expected) to do so within the scope of the notation covered in this course. Normally, this kind of in-depth details (e.g., exceptions, lambdas) are not relevant for the purpose we use sequence diagrams for (i.e., to communicate important interactions, not to represent code in a diagram format). But can use a UML note to add this kind of additional information to a diagram if really needed.



# Noteworthy
- In UML diagrams, many things are *optional*. Just because the diagram does not show something does not mean that those things do not exist. It just means that who ever drew the diagram was not interested in showing all those details that have been omitted because they may not be relevant for the purpose of the diagram.

- Time travels from top to bottom in the sequence diagram.

# Something to think about

These are something that you could try to think about when you are revising this topic. Feel free to discuss with your team/forum/me if you are not sure 😄

1. Other than the *abstract method* is there any other differences between how things are represent in sequence diagram and other UML diagrams (e.g. object/class diagram)?