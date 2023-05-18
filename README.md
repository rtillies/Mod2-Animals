# Mod2 Week2 Assessment - <Alex Bukhmirov>

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
TDD is Test Driven Development. It is a strategy of programming that focus on writing tests before actually writing the code.
1. What are three benefits of using TDD?
-It makes writing test a necessity and therefore none of the code will go untested.
-It makes it easier to structure and plan your code before actually writing it.
-It helps you break down your code into smaller steps and helps you write code slower and more planned out.
1. Imagine you are in an interview.  The interviewer asks: How do you use TDD? How would you answer?
 I make sure that I understand the problem before me and then I create the Class Tests to show the logic I need to build the actual classes. I then make sure the tests work by building the actual code around them.
1. For the class below, outline the tests you would need.  Try to use as much C# syntax as possible. The first test has been provided for you. (this question is worth 4 points)


```c#
public class Dog
    {
        public string Name { get; }
        public string Breed { get; }
        public bool IsHungry { get; private set; }

        public Dog(string name, string breed)
        {
            Name = name;
            Breed = breed;
            IsHungry = true;
        }

        public void Eat()
        {
            IsHungry = false;
        }

        public void Sleep()
        {
            IsHungry = true;
        }

        public string Speak()
        {
            return "Bark Bark!";
        }
    }
```
```c#
// Add your tests here
[Fact]
public void DogConstructorHasAllAttributes()
{
Dog dog = new Dog("Nile", "Golden Retriever");
Assert.Equal("Nile", dog.Name);
Assert.Equal("Golden Retriever", dog.Breed);
Assert.True(dog.IsHungry);
}

[Fact]
public void DogEatMakesDogNotHungry()
{
Dog dog = new Dog("Nile", "Golden Retriever");
dog.Eat();
Assert.False(dog.IsHungry);
}

[Fact]
public void DogSleepMakesDogHungry()
{
Dog dog = new Dog("Nile", "Golden Retriever");
dog.Eat();
dog.Sleep();
Assert.True(dog.IsHungry);
}

[Fact]
public void DogEatMakesDogNotHungry()
{
Dog dog = new Dog("Nile", "Golden Retriever");
Assert.Equal("Bark Bark!",dog.Speak());
}


This test isn't need anymore because of the constructor test[Fact]
public void DogHasNameAttribute()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    Assert.Equal("Nile", dog.Name);
}
```

5. What is a merge conflict, and when might you encounter one?
A merge conflict is when two branches of a project have code on the same lines and are conflicting with each other for that space. You might encounter one when working on a branch of your project that edits code that is on the same line as code on your main branach or when you are working on a project with a team and your branches are conflicting with each other.
1. You and a partner are working on a project together.  Your partner is working on aa-branch; you are working on bb-branch.  In as much detail as possible, describe how you both would get your work combined onto the main branch.
First we both would save and commit our work localy. After that we would push our respective branches to the remote repository (GitHub). Then we would review and approve each other's branch. After that we would try to merge our branches into the main branch in GitHub by first creating a pull request for each branch and then seeing if they have any merge conflicts. If they do we would fix them and then merge. 
1. Why is it good practice to have someone else approve and/or merge your PR?  
  A second pair of eyes never hurts. That person can check that you worked on the correct problem, check if there would be any merge conflicts and also acquaint themselves with your new code and be more aware of it in the context of the whole project.
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
