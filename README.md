# Mod2 Week2 Assessment - <YOUR NAME HERE>

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
TDD stands for test driven development where you first write the tests to test what you want the program to be able to do. Then you write the program to match the tests.
1. What are three benefits of using TDD?
Some of the benefits of using TDD is that its an extra oportunity to plan what and how you want your program to do before you start. In a lot of ways its like psudocode that can tell you if you've written the code to your specifications.
1. Imagine you are in an interview.  The interviewer asks: How do you use TDD? How would you answer?
I use TDD as an opportunity to iron out my plans and upgrade my psudocode in its detail and structure. I also appreciate that I don't have to write the tests when im done because I got it out of the way at the start.
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
public void DogHasNameAttribute()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    Assert.Equal("Nile", dog.Name);
}
[Fact]
public void DogHasBreedAttribute()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    Assert.Equal("Golden Retriever", dog.Breed);
}
[Fact]
public void DogHasIsHungryAttribute()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    Assert.True(dog.IsHungry);
}
[Fact]
public void Dog_Eat_SetsIsHungryToFalse()
{
    Dog dog = new Dog("Nile", "Golden Retriever");
    dog.Eat();
    Assert.False(dog.IsHungry);
}
[Fact]
public void Dog_Sleep_SetsIsHungryToTrue()
{
    Dog dog = new Dog("Nile", "Golden Retriever");
    dog.Eat();
    dog.Sleep();
    Assert.True(dog.IsHungry);
}
[Fact]
public void Dog_Speak_ReturnsString()
{
    Dog dog = new Dog("Nile", "Golden Retriever");
    Assert.Equal("Bark Bark!", dog.Speak());
}
```

5. What is a merge conflict, and when might you encounter one?
A merge conflict ocurrs when trying to merge two branches that have changes in the same place in the same file. to resolve the conflict you have to decide which branches changes youd like to keep or how youd like to keep both.
1. You and a partner are working on a project together.  Your partner is working on aa-branch; you are working on bb-branch.  In as much detail as possible, describe how you both would get your work combined onto the main branch.
After compleating the work on the branches we would both push our branches to github. Next we would each create a pull request in github to merge the new work into the main branch. Finaly we would each review the other's PR and merge the other's work into the main branch, perhaps discussing how we'd like to resolve merge conflicts.
1. Why is it good practice to have someone else approve and/or merge your PR?  
It is good to have everyone who is working on a project to get their eyes on new code. It is also important to get fresh eyes that can pick out any errors or bugs you may have missed and use the PR as an oportunity for reveiw and revision.
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
