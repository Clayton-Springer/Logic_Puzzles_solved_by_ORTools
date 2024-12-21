## Introduction 

I have been fascinated by logic puzzles for a long time. Part of the that is I am also stumped as I'm not particulaly good at them. 

A couple years ago I picked up a book of puzzles [Logic Barron's Puzzle book][https://www.puzzlebaron.com/portfolio-item/puzzle-barons-logic-puzzles-vol-1/]. I have been working out by hand many of the easier puzzles in the book.

For change of approach, I have turned to computation to solve them. When I set out to solve them, I tried to code it up using the python standard library. This did not work well. Although I did improve my understanding of sqlite. 

After a bit of googling I found Raymond's Hettinger's Pycon 2019 talk how to use a SAT solver [https://www.youtube.com/watch?v=_GP9OpZPUYc&ab_channel=PyCon2019] to solve logic puzzles. I did not realize that SAT problems are proven to be NP-hard. Not that I was trying to solve puzzles with very large solution spaces. I believe a puzzles in the book have a solution space of 5! * 5! * 5! = 1,728,000 possiblies. Not so large by computer standards, but plenty large enough to stump my human mind.

## Solving the Puzzles

Inspired by Hettinger's approach, I decided to use a SAT solver.  Of course, these days the key challenge in tackling a software challenge is to find the correct library and use that.The one he used did not seem very appealing to me. I found ORTools and was rewarded with a clean way to describe puzzles and a fun way to learn about a useful library. I found this on-line book very helpful [https://github.com/d-krupke/cpsat-primer] to learn from. 

In his talk, Hettinger solves the "Einstein Puzzle" which I call Zebra puzzle after its wikipedia entry [https://en.wikipedia.org/wiki/Zebra_Puzzle]. This is a nice entry level example. The Jupyter notebook that solves it is called "Zebra-many-solutions_cleaned.ipynb". The many solutions refers some code at the end that will print out all the solutions from the constraints. For the full puzzle there is 1 solution. However, if you comment out one or more constraints there will be more than 1 solution.
Moving on to an intermediate difficulty puzzle -- but which I was still able to solve this myself by hand -- I show the solution of the Puzzle Baron's "Robot Warriors" puzzle. This was less straightforward to code up and required a bit of cleverness to get ORtools to solve it. The Jupyter notebook that solves it is called "Robot_Warriors_cleaned.ipynb". Once again code at the end prints all the possible solutions. This is more interesting if you comment out constraints and rerun the notebook. Moving one of most difficult puzzles in that book, which I was not successful in solving by hand,  I show the solution of the "It's all about ratings" puzzle. Statement #2 "Channel #22 has fewer viewers than the channel that airs Top Chow, which has fewer viewers than TWL" was tough to solve by hand. Of course ORTools makes it easy. At the end there is some not elagate code to format printing of the solution.


## Conclusion

It was satifysing (pun unintended) to learning to use the ORTools library to solve a puzzle I could not on my own. However, having done that I am ready to move on to non-logic puzzle challenges.


### scratchpad below this

Embryo Outline

Background 

1. You		The protagonist is in their comfort zone

		I like python. I am intrigued by logic problems, but not particulaly good at solving them.   

2. Need		The protagonist wants something

		I viewed the video by Raymond and was inspired to try my hand at having the comuter to solve them by learning some new code 

3. Go		The protagonist enters an unfamiliar situation

		My initial failures to make any progresses, I found the ORTools library and decided to give them a try

4. Search	The protagonist adapts to the unfamiliar situation and searches for what they want

		After learning a bit about how the library works. 

5. Find		The protagonist finds what they want

		I was able to solve the Zebra puzzle. It is a relative simple puzzle.
		The "Robot Warriors" puzzle was a bit more difficult and required a bit of learning. I found the this on-line resource very helpful.
		The last puzzle was even more difficult and required new ORTools tricks to be learned. 

6. Take		The protagonist pays a price for achieving their goal

		I learned how to use the ORtools

7. Return	The protagonist returns to their familiar situation

		Now I am pleased to have the ability to solve logic puzzles

8. Change	The protagonist has changed fundamentally

		I have learned a bit on how to use the ORTools and having used software to solve logic puzzles I am ready to move on to other challenges


Story Embryo

Step	Description
You		The protagonist is in their comfort zone
Need	The protagonist wants something
Go		The protagonist enters an unfamiliar situation
Search	The protagonist adapts to the unfamiliar situation and searches for what they want
Find	The protagonist finds what they want
Take	The protagonist pays a price for achieving their goal
Return	The protagonist returns to their familiar situation
Change	The protagonist has changed fundamentally
