# Design notebook for week ending November 16, 2014

## Description

**TODO:** Fill in this part with information about your work this week:
important design decisions, changes to previous decisions, open questions,
exciting milestones, preliminary results, etc. Feel free to include images
(e.g., a sketch of the design or a screenshot of a running program), links to
code, and any other resources that you think will help clearly convey your
design process.

This week I began implementing my code. I started with some basics - just defining two players, defining a board using the ```m x n``` notation, etc. Piece by piece, I built it up to it's current form, which is getting much closer to where I want it to be (I think I've definitely done at least the 1/4 of tic-tac-toe I wanted done by this week). For an idea of where my DSL currently is, check out my [sample program](https://github.com/AriHC/RuleBook/blob/ecfe40bb963eb9ca66c84e25391cb4fe94da9a37/src/samples/Tic_tac_toe.scala) (this link is to the program at the time of writing this). Notice that while I haven't yet designed the input functions, ```Legal_if``` is working; Running this version of the program will successfully reject all "moves" that aren't "heyo!".

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I think my biggest issue right now is figuring out how I will be implementing the more difficult pieces of my syntax - getting pieces from players, putting them on the board, getting user input, etc. These are my big challenges for the comming week.

**What questions do you have for your critique partners? How can they best help
you?**

I'd be happy to hear suggestions on how users should be able to specify valid moves or not in a more flexible manner, and how they should access specific pieces from a player (not that that's relevant to tic-tac-toe). For the former, my best idea is to give some sort of overrideable piece of get user input that parses the input, but I don't really want to make people parse themselves.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

This week I spent about 8 hours on the project.

## Post-critique summary

My critique this week seemed to focus mainly around my syntax, which makes sense since that's what I worked on last week. Specifically, there were concerns voiced about how certain pieces may be implemented - though it appears there was some confusion about me doing an internal language, as my critique partner mentions working on my parser. I'm not sure if that would address her concern about how easy/hard it is for my move legality syntax to work for chess. The way I see it, in chess the programer would probably subclass pieces, giving them some sort of "can move from a to b" method describing how each piece moves, then all you would need to do was say a move is legal if the piece at the first chosen location can move from that location to the second chosen location. The other main issue raised was that my variable scheme is not so great, which I completely agree with.

## Post-critique reflection

I will approach my language development with an open mind about syntax. My goal will be to get as much working as I can, working on the "IR" - in this case the underlying logic that cycles through turns, that way even if my syntax is not up to par, I can hopefully mess around with it later, but keep the IR implementation of the commands the same.
