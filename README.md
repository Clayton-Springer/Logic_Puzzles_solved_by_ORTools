## Introduction 

I have been fascinated by logic puzzles for a long time. Part of that is I am frequently stumped and not particulaly good at them. 

A couple years ago I picked up a book of puzzles [Logic Barron's Puzzle book][https://www.puzzlebaron.com/portfolio-item/puzzle-barons-logic-puzzles-vol-1/]. I have been working out by hand many of the easier puzzles in the book.

For change of approach, I have turned to computation to solve them. When I set out to solve them, I tried to code it up using the python standard library. This did not work well. Although I did improve my understanding of sqlite. 

After a bit of googling I found Raymond's Hettinger's Pycon 2019 talk how to use a SAT solver [https://www.youtube.com/watch?v=_GP9OpZPUYc&ab_channel=PyCon2019] to solve logic puzzles. I did not realize that SAT problems are proven to be NP-hard. Not that I was trying to solve puzzles with very large solution spaces. I believe a puzzles in the book have a solution space of 5! * 5! * 5! = 1,728,000 possiblies. Not so large by computer standards, but plenty large enough to stump my human mind.

## Solving the Puzzles

Inspired by Hettinger's approach, I decided to use a SAT solver.  These days the key challenge in tackling a software challenge is to find the correct library and use that.The one he used did not seem very appealing to me. I found ORTools and was rewarded with a clean way to describe puzzles and a fun way to learn about a useful library. I found this on-line book very helpful [https://github.com/d-krupke/cpsat-primer] to learn from. 

In his talk, Hettinger solves the "Einstein Puzzle" which this repository I call Zebra puzzle after its wikipedia entry [https://en.wikipedia.org/wiki/Zebra_Puzzle]. This is a nice entry level example. The Jupyter notebook that solves it is called "Zebra-many-solutions_cleaned.ipynb". The "many-solutions" in the title refers some code at the end that will print out all the solutions from the constraints. For the full puzzle there is 1 solution. However, if you comment out one or more constraints there will be more than 1 solution.
Moving on to an intermediate difficulty puzzle -- but which I was still able to solve this myself by hand -- I show the solution of the Puzzle Baron's "Robot Warriors" puzzle. This was less straightforward to code up and required a bit of cleverness to get ORtools to solve it. The Jupyter notebook that solves it is called "Robot_Warriors_cleaned.ipynb". Once again code at the end prints all the possible solutions. This is more interesting if you comment out constraints and rerun the notebook. Moving on to one of more difficult puzzles in that book, which I was not successful in solving by hand,  I show the solution of the "It's all about ratings" puzzle. To get a sense of my difficulty, I found Statement #2: "Channel #22 has fewer viewers than the channel that airs Top Chow, which has fewer viewers than TWL" tough to implement by hand. Of course ORTools does it easy. At the end of this notebook there is some unpretty code to format printing of the solution.


## Conclusion

It was satifysing (pun unintended) to learning to use the ORTools library to solve a puzzle I could not on my own. However, having done that I am ready to move on to non-logic puzzle challenges.

