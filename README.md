# Mod2 Week2 Assessment -Isiah Worsham

## Setup
1. Fork this repository.
1. Add ONE of the following GitHub profiles as a collaborator to your forked repo:
`memcmahon`, `rtillies`, `zoefarrell`
1. Clone your repo to your local machine.
1. Open your cloned repository in Visual Studio.
1. Insert your name on line 1 to replace `<YOUR NAME HERE>` above.

## Questions (10 Points Possible)
**Important** Answer these questions in this file on your `main` branch.  When finished with the questions, commit and push your main branch.  You do not need to create a pull request yet!

1. What does TDD stand for?
TDD stands for Test Driven Development
1. What are three benefits of using TDD?
Helps with refactoring your code by making a failing test that you mold to how you think the code should work then improving your code when you actually make it. Also helps with creating methods that you never thought of prior. Helps developers with accurately brainstroming how your code should work when its used in the real world. You are able to discover problems a lot faster, so it helps with debugging before those problems show up making it faster than manual testing.
1. Imagine you are in an interview.  The interviewer asks: How do you use TDD? How would you answer?
The way I use TDD is, I test all of the classes and their methods before I create them to better understand my code and identify any issues before they transpire.
1. For the class below, outline the tests you would need.  Try to use as much C# syntax as possible. The first test has been provided for you. (this question is worth 4 points)

```c#
public class Dog
    {
        public string Name { get; }
        public string Breed { get; }
        public bool IsHungry { get; private set; }

        public Dog(string name, string breed) ----//Create a test here to test if my Dog object gets created with correct properties
        {
            Name = name;
            Breed = breed;
            IsHungry = true;
        }

        public void Eat()-----//Test all three of these methods and assert that isHungry is true or false and that my Speak() method makes my Dog "Bark Bark"
        {                       
            IsHungry = false;
        }

        public void Sleep()-----
        {
            IsHungry = true;
        }

        public string Speak()------
        {
            return "Bark Bark!";
        }
    }
```
```c#
// Add your tests here
[FACT]
public void DogMethod_EatAssertsIsHungryFalse()
{
    Dog dog = new Dog("Nile", "Golden Retriever");
    dog.Eat();
    Assert.False(False, dog.IsHungry);
    dog.Sleep();
    Assert.True(True,dog.IsHungry);
}
[Fact]
public void DogMethod_SpeakReturnsString()
{
    Dog dog = new Dog("Nile", "Golden Retriever");
   dog.Speak();
    Assert.Equal("Bark Bark",dog.Speak());


[
[Fact]
public void DogHasNameAttribute()
{
    Dog dog = new Dog("Nile", "Golden Retriever");
 

    Assert.Equal("Nile", dog.Name);
}
```

5. What is a merge conflict, and when might you encounter one?
A merge conflict happens when you try to merge two similar PRs and they overlap causing it to conflict with each other.
1. You and a partner are working on a project together.  Your partner is working on aa-branch; you are working on bb-branch.  In as much detail as possible, describe how you both would get your work combined onto the main branch.
We both would create PRs on Github merge them then pull back to VS where you will go to Git changes to merge both of yalls branches to the main branch then push it back up.
1. Why is it good practice to have someone else approve and/or merge your PR?  
  That way they have seen and analyzed your code before it was pulled into their repository.
**Before moving on to the next section, commit your work and push your main branch!**
  
## Git Exercise (6 points possible)

1. Create a new branch called `elephants` (1 point)

1. Add the following to the end of the Animal Tracker file:

```
Elephants
- African Savanna
- Asian
- African Forest
```

3. Commit this change to the Animal Tracker file with an appropriate message. (1 point)

1. Create the following files with the listed contents:

**African Savanna.txt**
```
Average shoulder height: 2.6-3.2 meters
Average mass: 3.3-6.6 short tons
```

**Asian Elephant.txt**
```
Average shoulder height: 2.4-2.8 meters
Average mass: 3.0-4.4 short tons
```

**African Forest Elephant.txt**
```
Average shoulder height: 1.8-3.0 meters
Average mass: 2,000-7,000 kilograms
```

5. Add and Commit these new files with an appropriate message. (1 point)

1. Push your `elephants` branch to GitHub. (1 point)

1. Create a Pull Request in GitHub. Write a short description of the changes you made to the repo. (1 point) 

1. Request a review from your collaborator. (1 point)
  
## Submission

Submit the Assessment Submission form linked in your cohort slack channel!

## Rubric

This assessment has a total of 16 Points. Earning 11 or more points is a pass and will indicate that you are progressing well with the material.

As a reminder, this assessment is for students and instructors to determine if there are any areas that need additional reinforcement!
