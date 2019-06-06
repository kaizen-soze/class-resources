# How to Debug Your Code
Debugging software is a part of any developer's life. There are a couple of techniques you can use to ensure that you're wasting as little time as possible.

## 1. Reproduce the issue
This is something you'll run into when people report bugs to you in code you've written. While you're developing a feature it's expected that you test it as you're developing...otherwise how will you know when you've accomplished what you've set out to do?

Unfortunately, when we're building a feature we usually don't test every edge case so bugs can slip through the cracks.

If someone reports a bug to you, before you just jump into fixing it, be sure to do the following: **MAKE SURE YOU CAN REPRODUCE THE ERROR**.

It's impossible to fix a bug if you can't reproduce the problem.

## 2. If you're getting an error, understand the message

When a computer spits out an error message, it's usually very terse and unhelpful. The best way to figure it out is to copy/paste the error into a search engine and see what other people have to say about it.

> Note: Do not simply copy/paste code from StackOverflow. Be sure to UNDERSTAND what is happening in the code before copy/pasting things from the Internet.

If the compiler gives you a line where an error is occurring, be sure to look at the line in question. It can give you important clues about what is going on.

## 3. Understand the code along with its intent

When you encounter unfamiliar code ([or code you haven't touched in six months](http://www.quickmeme.com/img/de/de9d8cec8389bbd175908ab5558a1b4b7179fa450d54a53f3ef0f6906b73e216.jpg)), it can be really hard to figure out what's going on.

This is why it's important to leave a lot of comments when you're writing code. It can help you to understand what's happening a lot faster.

When should you add comments? As a general rule, comments need to be added anytime you do something unorthodox.

If you don't understand what the code is supposed to do, how can you fix it?

## 4. What was the last thing you changed?
One extremely common issue is that your code is working fine, and then it's suddenly NOT working fine.

If this happens, the culprit is usually the very last thing that you changed.

## 5. Comment out blocks of code
This can help narrow down where an error is occurring. If you have five blocks of code, and you aren't sure where the bug is, comment out half your code and see if you get the output you're expecting to that point. If you do, then go to the commented-out code and un-comment half of it. Check the output. If everything is fine, then repeat the process until you find where things are going wrong.

## 6. Rubber Duck

When you encounter a bug you can't figure out, pull out a rubber duck (or some other stuffed animal) and somberly explain your problem to it.

Yes, this is a real thing.

There's something about being forced to explain a problem out loud that forces you to see the problem from another perspective. More often than not, you'll have a light bulb moment and solve the problem.

If you don't want to be seen having serious conversations with a stuffed animal, you can always grab a friend or coworker :)

## 7. Take a damn break

Brains need rest. You can't solve an intellectual problem with brute force. If you are making absolutely no progress, just...stop. Work on something else. Anything else. Take a walk. Have some coffee.

Your subconscious will keep working on the problem. When you're not focused on the code, the solution can often come to you while you're doing something completely unrelated.

If nothing else, coming back to the problem in a refreshed state makes you better-equipped to solve the problem on the next go-round.

## 8. Ask for help

No one knows everything. We all have gaps in our knowledge. Many times a friend or coworker will have suggestions that can help you crack the problem.

> Note: If someone makes you feel bad or infers that you're a terrible programmer for not knowing the solution on your own, they are an asshole

Having another person look at your code can provide some insight into the nature of the problem. Any time you spend more than 30 minutes stuck on an issue, seriously consider asking for help.