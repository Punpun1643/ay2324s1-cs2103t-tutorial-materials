# Week 7: Project Requirements 

Tags: `W7` `DG` `requirements`

U3: add comments to mentee PRs | **Actor:** tutor | **Precondition:** logged in

**MSS:**
1. Tutor enters the 'list' command 
2. System shows PRs
3. Tutor performs <ins>U1. Sort PRs by criterion to sort by comments count</ins>
4. Tutor performs <ins>U2. Add comments to a PR</ins>

Repeat step 4 until satisfied

Use case ends.

**Extensions:**

2a. No PRs allocated to the tutor

Use case ends

*a. Connectivity lost

&nbsp;&nbsp;&nbsp;&nbsp;*a1. System informs the user

Use case ends

# Q&As

**Q: Should extension 2a be 1a instead?**

**A:** No. If we number it as 1a, this path does not include the system respond to the user action.

**Q: Is the extension '4a. Cancels the adding of comments after typing the comment halfway' correct?**

**A:** This is a valid extension. However, this extension should belong to U2.

**Q: In the MSS, can we add 'Tutor selects a PR to comment on' between 3 and 4?**

**A:** Yes, that is possible, unless selecting a PR is part of U2.

**Q: Where do we put scoping limits for functional requirements (i.e to defind what the application cannot do)?**

**A:** Normally they are placed under non-functional requirements.

# Noteworthy

## Specifying requirements

- It is more important to capture all requirements and following them in your implementation. Categorising NFRs correctly is not as important. However, do try your best to categorize the requirements correctly. In such unclear cases, do exercise your judegment as a team whether a requirment is an FR or NFR.

- As a matter of fact, some requirements can have both FR and NFR parts, and some may sit in the middle.

- In the tutorial, we went through an exercise to find the 'least well-defined' NFR. In practice, it is not important to find which one is least well defined. Instead, we should make everything as well defined as possible. (💡Tips: go through your NFRs and ask yourself questions like *'what does this term mean?' E.g. what does *'a lot of memory'* mean or what does *'authorized users'* mean. If you still find such questions relevant, there is a chance that your NFR can be made more specific.)

- Example of how you can better define your NFR:    
    - *'a lot of memory'* --> *'should not take more than 50MB when showing less than 20PRs'*

    - *'smooth and responsive'*, *'a resonable response time'* --> *'the system should respond to the user within 3s'*

    - Note: if you realise, these are when I could ask question like *what does responsive mean*, *what does smooth mean*, *what does reasonable response time mean*.


## User stories

- Including 'obvious' requirements such as *'As a tutor, I can login to the system, so that...'* or *'As a tutor, I can view the code in a PR, so that...'* is important. Omittimg them can throw off planning and estimation efforts.

- User stories should be as specific as possible. Ideally, user stories should be atomic such that they cannot be broken down any further. E.g. *'As a tutor, I can comment on PRs, so that...'* can be split as add/edit/delete.

## Glossary

- It is not a big deal to include more terms in the glossary than strictly necessary. Of course, try to be reasonable (i.e. do not include terms that are obvious e.g. *computers*)

## Use cases

- Use cases do not have a *standard* format. Here, we try to be consistent with the notation used in the textbook. If going strictly by the textbook:
    - precondition etc. should be in separate lines (it is just a cosmetic difference though)
    - for inclusions, use case number should be at the end (rather than infront) e.g. '<ins>Sort PRs by criterion (U1)</ins>'. This too is just a cosmetic difference

- Please do keep the format consistent throughout your DG.

- UI details are usually **omitted**. The idea is to leave as much flexibility to the UI designer as possible. The main purpose of use case is to capture the interaction between the user and the system. (Example of UI detials include but not limited to: *right click*, *text box*, *exact command names* etc.)
