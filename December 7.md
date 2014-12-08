# Design notebook for week ending December 7, 2014

## Description

This week was spent primarily on documentation (in the form of comments in my code, and a huge update coming soon to the readme - I haven't yet committed it but will soon).

First I focused on getting SBT working, since during user testing my partner was having trouble running my code, so he ended up having to use my computer. Hopefully now this isn't necessary, as SBT is at least working when I try it. This also involved a refactor of where my code is stored - samples now have their own directory near the top, and are an independent SBT project from the RuleBook code.

My next goal, still along the lines of helping people set up RuleBook, was figuring out how to build and work a ```jar``` file. I'm not particularly scala or java fluent, so that took me a fair amount of Googling and experimenting to get working.

I then went on to code organization/documentation, particularly in the ```implicits.scala``` file (now renamed to ```globals.scala``` since it has more global definitions than it does implicit ones). I went through, sorted all the functions by what area of a game they were related to, and added more comments.

I made another sample fairly quickly, since Tic-tac-toe and connect four are almost the same game.

As I said, I'm in progress updating the readme into a how-to. I've done setup and playing games, and am in progress on writing games. 


## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

At this point, any more cleanup/commenting I can do would be great. Definitely in wrap up mode though.

**What questions do you have for your critique partners? How can they best help
you?**

What _one_ thing would be most important to do if I had time?

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

All said, I've spent about 8 hours on the project this week (including anticipated 30 mins - 1 hour finishing the how-to).

## Post-critique summary

Sarah agreed with most of my preliminary evaluation from last time. She reassured me that my syntax looks reasonably human readable, but also agreed that some of it is rather verbose. She agrees that documentation and testing are a good idea for this week.

## Post-critique reflection

Seems like I'm on the right track. Documentation and testing it is!
