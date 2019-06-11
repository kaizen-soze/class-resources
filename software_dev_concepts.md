# Essential Concepts in Software Development
While this is a very short list, the concepts in it can take you a long way if you keep them in mind while developing a software project.

## Naming things is hard
Anyone can name a variable `x`. The difficult part of naming variables is figuring out how to come up with a name that's clear and descriptive, even for someone who's never seen your code before.

Naming things is ultimately subjective, and what seems clear to one person may not seem clear to another. However, you owe it to your future self and your teammates to try.

Here are some solid rules of thumb:

### 1. Name variables after nouns
Variables are modified, changed, and passed around between methods. Give them a name that makes sense for them given their context in the code. Using a noun makes it easier for our brains to think of a variable as a thing to be modified.

### 2. Differentiate similar variables with adjectives
When you have a lot of variables serving the same function, it can be tempting to name them `thing1`, `thing2`, etc. However, when you're reasoning through the code, names like that tend to make it more difficult to keep things straight in your head. Using adjectives makes it easier to attach meaning to a variable as you write the code.

### 3. Name functions after verbs
A function is intended to **do** one thing. Verbs are the "doers" of the English language, so name your method after what it does.

### 4. Keep your names short, but not too short
Try to limit your variables and methods to one or two words unless there's a compelling reason not to. We tend to write variables and method names over and over, so the shorter the name is, the easier it is to type. When given the choice between short or descriptive, you should go with descriptive.

## Don't Repeat Yourself
`D`on't `R`epeat `Y`ourself, also known as DRY, is a methodology that aims to keep repetitive code to a minimum.

Anytime you have to use the same bit of code more than once, ask yourself if you can refactor the code by making it a method, and calling it as necessary.

It's possible to take DRY too far, so make sure that the changes you're making to the code will ultimately make your code easier to understand.

There's no point in following methodologies like this if they wind up making your code harder to understand.

## Code for the present
When you get caught up in the excitement of coding your project, it's possible to start planning how you'll shape the code in the future. 

Don't do that.

Code exactly what you need for right now. We all have our ideas for what we'd like to happen, but changes shouldn't be made to your codebase until it's actually time to make them.

Why?

Software is often very fast-moving. Pivots happen. Plans change. What seems very reasonable in one scenario could be completely unworkable in another. If you've added in a bunch of placeholder code (or worse, code you aren't using yet), you may wind up in a situation where you have to spend time refactoring or removing code.

The easiest way to avoid that is simply not to write code that isn't yet needed.

## Minimum Viable Product

Minimum Viable Product, or `MVP`, is related to the above concept of only coding what you need. When you first start on a project, you have a lot of ideas about what type of functionality needs to belong in it.

The problem is that we always have more ideas than we do time. It takes time to code. It takes time to test. It takes time to design. The more features you have in your initial concept, the longer it will take to finish.

A Minumum Viable Product is the most basic form of your project that delivers the essential features. This mindset means being ruthless when it comes to determining what your project is going to be able to do. If a feature doesn't contribute in a meaningful way, then it should be eliminated.

## Never trust the user

The code we're writing in class is all about optimizing for the best-case scenario. One real-world concept to keep in mind is that you should never, ever trust anything the user gives you.

When a user fills out a form, be sure to validate the information they give you. If you're expecting a string, check it to make sure it's a string. If you're expecting a phone number, check it to be sure it's in the appropriate format. If a user does the wrong thing, either accidentally or on purpose, will your application break? If you accept file uploads, check that the user is giving you the appropriate file type, and not a virus.

Hacking a web app is easy if the person who built it didn't think about how the user could be malicious. Do not assume that your users are benign.

Here's a very small list of things to keep in mind:

* Never store passwords in plain text
* Never store anything sensitive in sessionStorage/localStorage/cookies
* Never store API keys in your front end web app
* Never use javascript's eval() function to process input from the user
* Always look for best practices when implementing something you've never done before.