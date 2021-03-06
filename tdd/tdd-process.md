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

Now we can feature test our methods and follow the errors like the following to build our unit test:

```
NameError: uninitialized constant DockingStation
  from (irb):1
  from /Users/username/.rvm/rubies/ruby-2.2.2/bin/irb:11:in '<main>'
```
> We now know that we have to define this DockingStation class

> Always check the **stack trace** where the error occurred, as well as the **nature** of this error

## <a name="unit-test"></a> 4. Unit test

It's now time to build our first unit test. To do so, we need a testing framework such as **RSpec**. 

To use RSpec (given that the gem is already installed), we need to initialize it in our directory with the command ```` rspec --init ````. This command initiliazes RSpec and generates for us a spec folder in which we will create all our test files. 

The next step is to ````cd````in the spec directory, and create our first ````file_spec.rb ````. 

Here is the basic structure of a spec file:

```
require '/lib/file.rb'

describe 'Our Class/Object' do
    it 'should return x' do
      expect(#our_method). to eq x
    end
end
```

> Always require the rb file associated with our test file

To see more about unit test and RSpec, see this [cheat sheet on rspec basics](./rspec_basics.md)

## <a name="refactoring"></a> 5. Refactoring
After having built our test, obviously there are some time where we got some errors related to our code. This is when we want to **refactor** our code accordingly !
Refactoring happens not once, but every time we don't pass a test.

