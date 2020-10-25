# GitHub Manners

This is by no means a definitive document. It encompasses the experience I have with Github and my personal opinion on how projects should be run. Take everything I say with a grain of salt.

## Don’t push directly to main

On small project teams, this doesn’t matter too much, but it can start to cause problems as the team grows. When going about adding features to your project, you should instead create a new branch and write code there until the feature is finished. Once it is finished, you can create a pull request to merge your completed feature back into main. That way, main always contains a working build of your project.

## Avoid merge conflicts

A [merge conflict](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/about-merge-conflicts) comes about when you want to merge one branch into another, but the same piece of code has been edited in both branches. Github doesn’t know which changes are the right changes, and so it raises a merge conflict. Merge conflicts aren’t something you should be afraid of, but resolving them takes away valuable time that you could instead have spent working on other things. Lucky for you, there are some simple things you can do that eliminate 90% of merge conflicts that will arise.

1. **Don’t push directly to main.** Yes, it can be as simple as that.
2. **Encapsulation.** For all of you object-oriented programmers out there, this is one of the fundamental ideas of OOP. If you are able to isolate your code from the rest of the project, you never have to worry about editing code you shouldn’t be editing. Then, all you need to do is call functions you’ve written in another place, instead of cluttering up the main project file.
3. **Talk with your coworkers.** If you find yourself in a situation where you do have to edit code someone else wrote, let them know first. If they have outstanding changes they are still working on, wait for them to finish those changes before editing their code.

## Avoid duplicate code

In smaller teams, it seems easy enough to just deal out tasks and work on them. If there is code that may have already been written, you just look through the branches until you find it or message the group. This stops working with a surprisingly small number of people. Between naming things differently, and bad descriptions of what you are making, you may not even realize that one person is writing code that does that same exact thing as yours does. This can be a big problem but luckily has many simple solutions.

One is to use task management software like [Trello](https://trello.com), [Github Projects](https://docs.github.com/en/free-pro-team@latest/github/managing-your-work-on-github/about-project-boards), or [Jira](https://www.atlassian.com/software/jira). These allow you to see all the available work that must be done, and claim something so no one else can accidentally start working on it too. Using software like this also has a lot of other advantages that I won’t go into.

Another is to have a daily/weekly standup meeting. This can be as simple as one sentence on what you plan to work on, one sentence on what you previously finished, and one sentence explaining anything stopping you, like if you need someone else to finish their code before you can begin on yours. Since we are all online and likely won’t be working on the project every day, really all we need to do is just send these three sentences in the group chat every time we sit down to code. That way, everyone knows what everyone else is doing.

## Get someone to look over your code before merging to main

Writing your code in a separate branch can be a powerful tool, but if you still end up merging broken code into main, it kinda defeats the purpose of using branches. In order to make sure the code you merge to main is a-okay, just have someone else look over it and check for errors. On Github, you can even set permissions to [disallow merging without a peer review](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/about-pull-request-reviews#required-reviews), which is something I highly recommend using. At first it can seem like a useless waste of time, but when you actually do catch an error before merging to main, you understand why it’s worth the trouble.

## Write readable code

I’m sure you’ve heard it a million times, but code is not just for computers, and it should be easy for humans to read as well. No matter what it does, code is not “good” if no one else can read it. Here are some simple ways to make code more legible.

1. **Use descriptive variable names.** While some professors might say I’m wrong, I think that variable names should be as descriptive as possible. That means if it is ten words long, but requires no comment, I’d prefer that to a two word variable that is vague in it’s purpose. This is just my personal preference, but it really does help to make your code easier for others to understand.
2. **Comment your code.** That does not mean you should add a comment to every line, or even every function. Use your judgement. If the variable name describes the variable well enough, there’s no need to comment it. However, docstrings/javadocs/etc can be very useful because you can use functions without even having to look at their implementation.
3. **Write consistently.** Despite being third on this list, it is probably the most important thing on here. There are many shortcuts and different ways to do things with programming. All are right, none are wrong. However, if you want to write readable code, you must must must be consistent. That means if you used an if statement with curly braces, you shouldn’t then switch to using single line if statements. If you use camelCase for variable names, don’t start using kebab-case half way through your program. You get the gist. There are also automated tools that you can add to Github to look over your code formatting, that way it can remain consistent no matter who is pushing to main. While this is recommended, I’ve never used it before and it probably isn’t worth the trouble to set up for only a single quarter project. However, if you find yourself working on longer, larger scale projects, I would highly recommend using a code quality checker.

## Conclusion

The best part about these rules is that you don’t have to be a master coder to follow any of them. They are simple, and take very little time to do, but can make your code much much better. So just do them. Please. Even when working on projects on your own, practice some of these principles, and I can guarantee people will like working with you a lot more.
