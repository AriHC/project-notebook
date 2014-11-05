# Design notebook for week ending November 2, 2014

## Description

This week I narrowed down my scope significantly, such as by restricting myself to grid-based games. This was partially achieved through meeting with Prof. Ben, and then later as I was writing up my project description and plan. Particularly when writing the plan, I realized how little time we have to work on this, so I wanted to make my scope as basic as possible. I found some DSLs similar to what I want to write, but with worse syntaxes. At least one of them is also limited to grid based games, I think both might be. So it's a shame that I'm not breaking out into new territory, but who knows, perhaps I'll continue this as a side project in some free time.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

My most pressing issue right now is deciding on a syntax. We use a lot of different words in English to describe games. I need to decide which ones I'll implement, and which ones would be up to developers. This is what I have planned for this comming week; by a week from now I'll have at least some idea of what the final language will look like.

**What questions do you have for your critique partners? How can they best help
you?**

Are there any other ways in which I can limit scope? I think my biggest problem right now is I'm having a hard time taking a step back and telling myself what pieces are unreasonable. Hopefully trying to write syntax will help me figure out what's too hard to describe.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**
Outside of classtime, about 30 mins meeting with Ben, 1.5 hours on the description (plus another hour looking into the similar languages I found), 1 hour on project plan. Off to a slow start, but things will pick up next week.


## Post-critique summary

By spending more time on the design, I might be able to speed up implementation. At the very least, it should ensure I don't head deep into an implementation only to decide I don't like the way it looks. Also, checkers is probably a better goal than chess as it still only uses one piece type. I need to think about visuals as well.

## Post-critique reflection

I like the idea of checkers instead of chess. Originally I was thinking it might be harder because I don't understand it quite as well, plus it's less ambitious, but I probably need that. It technically has two pieces, because of kings, but I could make kingless checkers (much more likely to stalemate, so I could make sure whatever logic I have for that that works for tic-tac-toe still works). My other reservation was checkers has forced moves. I could begin without that though, and then see how I might implement it. This feedback is a great idea to really help push me back in the direction of limited scope.

As it currently stands, I have this whole week set aside for design. Hopefully that should be enough, but we'll see. I hadn't thought of my language as particularly engineering heavy, but I suppose it might be. I will take this into consideration in my design, and after I have my ideal syntax down, spend some time thinking about the semantic interpretation, and how I can simplify it to make the coding easier.
