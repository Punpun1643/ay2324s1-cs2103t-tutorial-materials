# Week 3: Coding Standards

Tags: `W3` `coding standard`

# IMPORTANT: update for the coding standard
The coding standard was updated recently to **allow omitting javadocs for overridden methods**




**A:** Yes.


# Q&As

**Q: Can `@return` be omitted if the method does not return anything?**

**A:** Yes.

**Q: (Line 7) Must we give an access modifier?**  

```java
List<String> pastDescription = new ArrayList<>(); // a list of past descriptions
```

**A:** The coding standard does not require it. In any case, not having an access modifier is a legit choice in Java (it is called *private package* access). So, if that is the appropriate access level, it is fine to not have an access modifier. 

**Q: (Line 7) Is having comment at the end of the line ok?**

```java
List<String> pastDescription = new ArrayList<>(); // a list of past descriptions
```

**A:** It is fine to have a comment at the end of the line. But when the comment is put above a statement, it should be indented to match the statement. The coding standard disallows comments with mismatching indentation, but does not mention/disallow end-of-line comment. 

**Q: For names representing a collection of objects, for example a list containing names. Is it ok to use nameList? Would this be considered a violation (i.e. adding the word list as the lastword in the variable name)? (or should it be nameLists?)**

**A:** `nameList` is fine, but `nameLists` is not ok as there is only one list. `names` would work too.

# Noteworthy

- Some IDEs will use wildcard import if there are more than a certain number of classes from the same package. This is against our coding standard.

- Although coding standard doesn’t specifically say parameter names should not be single letters, it mentions that scratch variables can be single letters. It is OK if someone interprets this as other names should not be single letters.
 
```java
public Task(String d) {
    ...
}
``` 

- The coding standard says ‘this.’ should not be used unless necessary. But that is an advanced rule (optional to follow). Only basic and intermediate level guidelines are applicable to the module.
    
```java
this.important = true
```
    
- The style in `DESCRIPTION_PREFIX` (i.e. all capitals, separated by underscores) is sometimes called *screaming snake* style

# Something to think about

These are something that you could try to think about when you are revising this topic. Feel free to discuss with your team/forum/me if you are not sure 😄

1. Is there any difference between coding standards and code quality?
