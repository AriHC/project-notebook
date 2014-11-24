# Design notebook for week ending November 23, 2014

## Description

This week I kept hard at my tic-tac-toe features. I was held up trying to make my syntax nicer (dang operator notation), and then also spent a lot of time trying to figure out how developers specify user input/moves. Overall, tic-tac-toe features are mostly done, but the hold ups meant I didn't get to the win condition logic. But in my current version of the [sample program](https://github.com/AriHC/RuleBook/blob/59d56783d0af07cfc145d0df3be7d80b70654182/src/samples/Tic_tac_toe.scala), you'll notice I show how my syntax can be used to do cool things relatively easily - in this case, redefining a move to be either placing a piece, or moving an existing piece.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I think the most important thing right now is finishing up the win condition description. I realized as a cool example of what my game can do would be taking the rules of tic-tac-toe and converting them into connect four, since that's really a pretty small change. But having the game actually terminate would be pretty good. I think mostly I just need to spend time on this right now.

**What questions do you have for your critique partners? How can they best help
you?**

I'm reaching a point where I want to know what looks good/bad in my syntax. I think I've been staring at it for so long I've started to think "yeah, this is exactly what someone would want" when really I think it's probably pretty bad, inconsistent, and unclean. But it'd be helpful for someone to point out exactly where.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

About 9-10 hours this week.

## Post-critique summary

My critique this week was largly on different ideas of how I could specify moves. This was broken into two parts, one one ideas for user input and what might feel natural, and the other (much larger part) on how legal movment could be encoded. The suggestion was turning pieces into their own mini finite state machines, with states and legal movements for each state, and what state they end up in afterwards (kinda reminds me of picobot).

## Post-critique reflection

As far as user input goes, I'm trying not to spend a ton of time on that, since in the ideal world, there would be a GUI, and the user would click either a space or a series of spaces. So this week I built something to emulate this - you specify locations in a simple (row,col) manner, and as a developer you can ask for exactly x, up to x, or at least x spaces to be selected. The one downside to this approach is it doesn't currently extend into letting players select, say, specific pieces off the board (like in the player's hand/bank). 

On the encoding side, as I've mentioned before I think in chess it would be good to have pieces have a legal move method describing how it moves, then you can say that a move is legal if there is a piece at the first place (belonging to the current player), there is not a friendly piece at the second place (and it is within bounds) and that the piece at the first place can legally move to the second place. Castling\pawn upgrading may need to be independently described outside of this system. Currently, I don't really support this, but I am considering making some sort of abstract movable piece where this legal move checking is built in, such that people could inherit from it in their work.

Regarding the states, I don't believe that is appropriate for this game. A game piece is a physical thing, it doesn't really have states. In checkers, when you "king" a normal piece, it is now a different piece. Some games do have flippable pieces, but I leave it up to the developer to encode that, as I think that's game specific and not worth generalizing at the moment.
