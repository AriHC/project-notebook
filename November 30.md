# Design notebook for week ending November 30, 2014

## Description

This week I finished up my implementation of tic-tac-toe, such that you can play a full game, complete with wins and ties. In terms of language concepts, this meant implementing win/tie/loss conditions, and also relative spaces (you can now ask for the coordinate in any of the 8 relative directions to another coordinate). I also did my preliminary evaluation.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

Based on user testing/critiques, I need to write some sort of guide to my language. I also don't have unit tests, so I want to write those. My language is still much less clean than I would like it to be, but at least it will be unclean and well documented this way (whereas if I try to spend time fixing it first, I'll probably end up with a fairly unclean language still, and it will be completely ambiguous how to write in it without reading through all the (poorly organized) source code).

**What questions do you have for your critique partners? How can they best help
you?**

Now that my language is complete-ish (you can write a full game), what parts of the syntax could be improved (keeping in mind the bounds of Scala). What would you like to be able to say that you can't do without multiple lines of non-DSL code?

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

I spent about 5 hours on my project this week (Thanksgiving break means less work time, and I still worked more over break than I would have liked to).

## Post-critique summary

My critique partner requested a how-to guide, and has noticed some of the awkward syntax choices I had to make as an internal Scala DSL. Specifically, using curly braces where a colon might be nice, and using 3 words where 2 would suffice. She also agrees win/tie conditions need to be implemented, and wonders how a turn will be specified.

## Post-critique reflection
  * how to guide: this will be my focus next week
  * Curly braces where a colon might be nice: this is twofold - colon can't be used, and curly braces/parens are needed to enclose the argument.
  * 3 words where 2 would suffice: this is because of operator notation - I had a choice between ```Player number 1``` and ```Player (1)``` and decided the former was more readable/closer to English, as per my design goals.
  * win/tie conditions have been implemented now
  * turn specifications are something I wanted to do originally, but for the sake of scoping I decided a turn always consists of just a move.