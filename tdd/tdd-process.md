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


## <a name="feature-test"></a> 3. Feature Test (irb)

Now that we have our **Domain Model** representing our objects and the messages they use to communicate with one another, it's time to **Feature test** !

Feature testing allows us to think about how we expect our objects and messages to work together. What behaviour do we expect from our methods ?
To test this, we can use a **REPL** (Read-Eval-Print-Loop) such as ````irb````

### Small notes on irb ###
To start the ````irb```` REPL, we simply type irb in the command line. 

Then we have to ````require````our rb file like so:
````require './docking_station.rb' ````
or directly using the shorthand ````-r```` when launching irb like so: ````irb -r ./lib/docking_station.rb ````

Now we can feature test our methods and follow the errors to build our unit test !


## <a name="unit-test"></a> 4. Unit test

## <a name="refactoring"></a> 5. Refactoring
