# Week 9: OODMs, activity diagrams

Tags: `W9` `OODM` `UML diagrams` `activity diagram` 

# Q&As

![886A7CA2-F7A8-41D7-B81F-53719FB35C89](https://user-images.githubusercontent.com/60144099/195984858-9a12aae2-9690-4c00-9ad2-fa567896dd36.jpeg)

**Q: For this diagram, we are showing coordinator as a separate association. In the case where coordinator has its own fields/methods e.g. something different from a regular instructor like admin rights etc., would this diagram still be valid?**

**A:** In that case this design is not ideal. A better design is to introduce additional classes to represent the roles e.g., CoordinatorRole. It also depends on whether such information is common to all coordinator roles played by a person (e.g., total modules coordinated) or specific to the coordinator role of a given module (e.g., start/end dates of the role).

![3F90017D-0E44-4E4D-8B63-02ADC026241A](https://user-images.githubusercontent.com/60144099/195984897-cb593d23-b6e6-4d67-aa0c-0b79da2d9339.jpeg)

**Q: Does this multiplicity of `1` (for `Attempt`) mean that a `Student` can only be associated with one `Attempt` for a given `Task` (i.e. a `Student` S1 can only attempt `Task` T1 once)?**

**A:** This intepretation is not correct. Putting `1` means that a `Student` can only make **one attempt in total**, not one attempt **per task**. So it is not possible to use multiplicity to indicate 'x attempts per task' in this diagram. But can use a UML note to add that info.

# Noteworthy

- We use OODM to model the **problem domain**. Notations related to solution domain or implementation should not be shown in OODM.

- Although OODM is a diagram about the problem domain, it is OK to use common data types (e.g. `boolean`) to indicate the nature of an attribute. Can also use neutral data types (e.g. text, flag), OK to use language-specific data types too (e.g. `String`).

- During the tutorial, we check the validity of our proposed OODM diagrams by trying to come up with an object diagram of different situations (e.g. what if `Instructor` Tom teaches 2 courses, he is an `Instructor` of `Course` C1 but is a `Coordinator` of `Course` C2) based on said OODM. This is something that you could try doing too when checking your OODM.

# Something to think about

These are something that you could try to think about when you are revising this topic. Feel free to discuss with your team/forum/me if you are not sure 😄

- We have gone through several diagrams for the past tutorials: class, object, sequence, OODM, activity diagrams. Can you tell the **differences** between these diagrams? There are also some **notations** that are shown in certain diagrams but not in others, do you know what these notations are?

- Different diagrams can be used in different situations. In the tutorial, we went through the situation where we should aid our explanation using an object diagram ('The course CS101 is taught by Prof Lee. It has two optional assignments and one test'). You could think about the other situations where you could use other diagrams to aid your explanation. 