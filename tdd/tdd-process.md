# TDD PROCESS

[User stories](#user-stories)&nbsp;&nbsp;|&nbsp;&nbsp;[Objects & Messages](#objects)&nbsp;&nbsp;|&nbsp;&nbsp;[Feature-test](#feature-test)&nbsp;&nbsp;|&nbsp;&nbsp;[Unit test](#unit-test)&nbsp;&nbsp;|&nbsp;&nbsp;[Refactoring](#refactoring)
## This diagram summaries the process we want to follow when building a test: 

![tdd process chart](/images/tdd-chart.jpg)

## <a name="user-stories"></a>1. User Stories

A **user story** is how we can describe in proper English one feature our program can do or is expected to do. We starting to build a test, it is really helpful to **break down** our program into small user stories.

Here is an example of a basic user story:
````
As a user,
So I can find customers,
I want to search for my customers by their surnames.
````

## <a name="objects"></a> 2. Objects and Messages

When we have our **user story** written, it is time to translate them into a functional system made up of **objects** and **messages**. Objects often refer to the *nouns* in our user story, while messages refer to the *verbs*.

If we go back to the above example, we can translate it into a functional representation like so:

Objects | Messages
------- | --------
User    |
Customer| find_by_surname


## <a name="feature-test"></a> 3. Feature-Test (irb)

## <a name="unit-test"></a> 4. Unit test

## <a name="refactoring"></a> 5. Refactoring
