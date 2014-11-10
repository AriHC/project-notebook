# Design notebook for week ending November 9, 2014

## Description

This week I spent quite a while thinking about syntax and semantics (syntax_idea.txt and semantic_idea.txt, in my project repository's documents folder). Specifically, I began by trying to write what I would want the syntax to be. As I was doing this, I was thinking how I would implement this behind the scenes. I ran into a lot of issues, particularly around I/O, where I'm still not sure I like my system. I also spent a fair amount of time thinking about how pieces would be defined, allocated, and moved. Obviously, we want a system where each piece does not need to be defined separately when there are duplicates. I'm pretty happy with where this has ended up, but I'm also worried that my syntax is not actually implementable in scala, so I may have to go back to the drawing board.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I'm currently most concerned about defining subclasses, specifically pieces, with a custom syntax ("a is b" to mean "a extends b"). It may be that this isn't possible, in which case developers would still have to use the less layman readable form. Though my personal design thoughts have been leaning such that this may be OK. The way I think about it, as long as everything not in the "definitions" section is human readable, and the language is clear enough that the game can be understood based on that, then I'm happy. In other words, I want to make sure that anything done in the definitions section is named well enough that a regular human knows what it means and doesn't need to read that code. In my rulebook analogy, a set of rules might say "you can move straight or diagonally". A human would know what "straight" and "diagonal" are, but the developer may still need to describe those in the definitions. But again, if they were used in, say, the "move" section, a human would be understand and not need to look at the formal definition.

**What questions do you have for your critique partners? How can they best help
you?**
I want feedback on the syntax thus far. Specifically, if they have ideas relating to getting user input in a useful way, or using variables without actually using variables (what my "take"/"taken" is aiming for), that would be awesome. I really want a nice way to let the users specify moves a sequences of spaces, but I'm not sure how well that would fly. I could potentially try something like getting an input, then different moves have different parsers, and it basically does signature matching by trying letting move types try to parse the input. But I'd like something less complex if possible. That's why for now I'm sticking to only taking in one input at a time - but then I had to add variables to keep them straight; previously I had the idea of "choose/chosen" as getting input, then accessing said input.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

I spent about 7 hours on the project this week. It looks like less, but as I said I was thinking hard about how I would actually implement bits of my syntax, so there were several periods where I would write down a syntax idea for a small part of the picture, then either stare at it unsure how it might work, or stare at it and realize it didn't mesh well with other parts of my syntax, so there was a lot of development there.

## Post-critique summary

By spending more time on the design, I might be able to speed up implementation. At the very least, it should ensure I don't head deep into an implementation only to decide I don't like the way it looks. Also, checkers is probably a better goal than chess as it still only uses one piece type. I need to think about visuals as well.

## Post-critique reflection

I like the idea of checkers instead of chess. Originally I was thinking it might be harder because I don't understand it quite as well, plus it's less ambitious, but I probably need that. It technically has two pieces, because of kings, but I could make kingless checkers (much more likely to stalemate, so I could make sure whatever logic I have for that that works for tic-tac-toe still works). My other reservation was checkers has forced moves. I could begin without that though, and then see how I might implement it. This feedback is a great idea to really help push me back in the direction of limited scope.

As it currently stands, I have this whole week set aside for design. Hopefully that should be enough, but we'll see. I hadn't thought of my language as particularly engineering heavy, but I suppose it might be. I will take this into consideration in my design, and after I have my ideal syntax down, spend some time thinking about the semantic interpretation, and how I can simplify it to make the coding easier.

