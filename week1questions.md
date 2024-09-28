Week 1 Lecture Notes
--------------------
+ Software Development Lifecycle
### 1. Who is on the software development team and what do they contribute?
-**Developer**
    - design the architecture
        - the overall design of a computing system and the logical interrelationships between its components.
        -  specifies the hardware, software, access methods and protocols used throughout the system.
        -  How the parts of the program will be organized
        -  Where persistent data is stored
        -  How data passes between the parts of the program
- **Product Manager** - mini-CEO for project
    - _HIGH LEVEL FOCUS _-> understands clients needs <br>
    -_ STAKEHOLDER MANAGEMENT _-> dev company, client, end users, dev team  <br>
    -_ PRODUCT SUCCESS _ -> define minimum viable product, measures success, fine tunes product  <br>
- **Project Manager** - in charge of day to day details
    -   _IDENTIFIES USE CASES_ -> what will users need to do with the app
    -   _UNDERSTANFS HIGH LEVEL REQUIREMENTS_ -> translated steo by step dev plan
    -   _LIAISING_-> between product manager, stakeholders and dev team
- **Designer**
    - UX —> how the user uses the app, navigating between screens
        - Draw high-level wireframes: focus on usability and user flow
            - No colours or other such details
        - Can the end user accomplish all the use cases?
        - Allows software developers to start planning
    - UI — Draw high-fidelity prototype
        - Based on wireframes, create fully-branded UI
        - Hand to devs to create
- **Quality Assurance**
    - product tester
    - review specifications and ensure adherence
    - test software on different browsers, screen sizes and network conditon
### 2. What are the main steps in the software development lifecycle? What is the goal of each one?
(1) - PLANNING & ANALYSIS  <br>
- evaluate feasibility of project, revenue potential, needs of end users  <br>
(2) - DEFINE REQUIREMENTS  <br>
- create clear requirements for the dev team <br>
(3) - DESIGN  <br>
- decide on tech needs and develop a prototype
(4) - DEVELOPMENT <br>
- develop the actual project <br>
(5) - TESTING <br>
- make sure it works <br>
(6) - DEPLOYMENT <br>
- deliver to end users <br>
(7) - MAINTENANCE <br>
- keep it going, address bugs, plan for new features <br>

### 3. What is the structure of a Java class? (declaration, variables, ...)

### 4. What are the possible accessibility modifiers and primitive types in Java?
### 5. What is the difference between the equals method and the == operator?
### 6. All Java classes are subclasses of "Object". We call Java classes "reference
types" as opposed to "primitive types". What is the difference between the two?
### 7. How is a constructor different from a method? Include information about what
each does as well as the difference in syntax.
<br>

+ Version Control and Git
### 8. What is version control and why do we use version control? How can we benefit from it? Give at least 7 features.
- software development teans need to track how their software changes over time
- a master repository of files exist on a server
- people can " clone" the repo to get their OWN local copy
- as progress is made people can "push" their changes to the master repo and "pull" other peoples changes from the master repo
- the repo keeps track of every change and people can revert to older versions
<br>
Why version control???
- **Backup and restore **- because accidents happen
•** Synchronization **- multiple people can make changes
• **Short term undo** - that last change made things worse?
• **Long term undo** - find out when a bug was introduced
• **Track changes **- all changes related to a bug fix
• **Sandboxing** - try something out without messing up the main code
•** Branching and merging** - (better defined sandboxes)

### 9. Repo??
- We have a repo that lives on another server -> this is called the origin
- We can CLONE this repo to have a local copy on our server
    - git clone <url>
- The **actual** repository is hidden. What you see and edit is the working copy of the files from the repository.
- You can create new files, make changes to files, and delete files
- When you want to **“commit”** a change to the local repository, you need to first “stage” the changes.
    - you need to tell git **which** files have changes that you want to add this time.
        - git add file
        - git commit -m "added features x"
    - **git add** does NOT add files to your repo
        - instead it marks a file as being part of the current changes
        - 
### 10. What do the four states in the "git status" report mean?
untracked -- YOU HAVE NEVER RAN A GIT COMMAND ON THE FILE
staged --
tracked --
dirty/modified --
### 10. What do these git commands mean?
clone --
pull --
add --
commit --
push --
branch --
merge --
status --
checkout --
### 11. A conflict is a set of characters you need to delete. Where do these characters
come from?
