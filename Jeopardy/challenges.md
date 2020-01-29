## Category is: Lazy Writers
Although each episode tends to feature unique categories, such as “¡HOLA TEQUILA!” and “‘80s BABIES”, there are some common recurring categories for clues on the board. A wise contestant will make sure to rock those categories.

What are the three most common categories of clues? Enter them in order from most common to least common, as a list of comma-separated categories. For example:

SCIENCE,ART,CLASSICAL MUSIC


_points_: 20

**Flag**

_flag_: `\s*AMERICAN HISTORY\s*,\s*NONFICTION\s*,\s*POTPOURRI\s*`

_flag type_: regex


## Category is: Education Standards
To get a competitive edge, the savvy contestant might decide to buff up on common categories that have proved to be harder for past contestants. 

Among the three repeating categories HISTORY, ASTRONOMY, and POP CULTURE, which category has proven the hardest for past contestants?

You're limited to two attempts for this challenge.

_points_: 20

_max\_attempts_: 2

_requirement_: Category is: Lazy Writers

**Flag**

_flag_: `ASTRONOMY`

_flag type_: static


## Category is: Hey Champ!
Each contestant is placed either on the left, the center, or the middle of the podium. 

Before you look at the data: do you expect the position on the podium to influence whether the contestant will win? 

Check your hypothesis against the data: enter the podium position with the highest number of winners as one of “left”, “middle”, or “right”.

You're limited to two attempts for this question.

_points_: 30

_max\_attempts_: 2

**Flag**

_flag_: `left`

_flag type_: static


## Category is: Buy Low, Sell High?
Past contestants have used pretty homogeneous strategies to move around the clue board. Each clue increases in value from the top row to the bottom row.

What clue row do they start from most often, for the very first clue?

The answer should be a number between 1 and 5.


_points_: 20

**Flag**

_flag_: `1`

_flag type_: static


## Category is: Preferred Direction
Clue values are constant left to right (across columns). In theory, there’s no advantage to starting on a specific column.

...But actually, what clue column do they start from most often, for the very first clue? 

The answer should be a number between 1 and 6.

_points_: 15

_requirement_: Category is: Buy Low, Sell High?

**Flag**

_flag_: `1`

_flag type_: static


## Category is: Difficult Choices
Clue values increase with the row number, top to bottom. On average, how many attempts are needed to solve a clue on the first row vs the last row? 

Enter the two numbers separated by a comma, and round to the first decimal digit.

Example: 0.1, 0.7


_points_: 20

**Flag**

_flag_: `\s*0.2\s*,\s*0.9\s*`

_flag type_: regex


## Category is: Daily Double
Daily Double are special hidden clues scattered throughout the clue board that let a contestant wager a sum and either get back double that amount (if answering correctly) or losing that amount.

Are Daily Doubles randomly scattered, or are there preferred positions? Find the clue row where Daily Doubles appear most often.


_points_: 20

_max\_attempts_: 3

**Flag**

_flag_: `4`

_flag type_: static


## Category is: Daily Double Part 2
You learnt that Daily Doubles are mostly located on Row 4. 

Are Daily Doubles harder than regular questions on Row 4? Enter yes or no.

Only one attempt allowed.

_points_: 30

_max\_attempts_: 1

_requirement_: Category is: Daily Double

**Flag**

_flag_: `no`

_flag type_: static


## Category is: Up, Up, Down, Down, Left, Right, Left, Right, B, A, Start
Contestants have a common pattern for moving around the clue board. On the second clue, how do contestants move relative to the most common position of the first clue (top left corner)?

Choose the two most common strategies:
(A) One clue above or one clue to the right
(B) One clue below or one clue to the right
(C) One clue below or two clues to the right

Enter A, B, or C as the flag.

_points_: 30

_requirement_: Category is: Preferred Direction

**Flag**

_flag_: `B`

_flag type_: static


## Category is: Payday Time
Assume that you can model the expected payout for a row as 

Expected payout = (probability of getting clue right on first attempt) x (value of clue)

For a contestant choosing the clue, what row yields the highest expected payout? The answer should be a number between 1 and 5.


_points_: 40

_max\_attempts_: 3

**Flag**

_flag_: `5`

_flag type_: static


## Category is: Be Like James
You can work on this challenge here, or on your own time. 

This is your chance to design a strategy to improve your expected winnings compared to the typical Jeopardy! contestant strategies you have looked at so far. 

Use the statistical regularities you learnt to answer questions such as:
* What clue position should you start from?
* How would you move about the clue board?
* What categories would you focus on relative to your personal trivia knowledge?
* When in the competition would you go fish for a Daily Double?
* When you hit a Daily Double, do you wage high or low?

You can decide on strategies that by poking more at the data, or designing a simulation that tries different strategies.


_points_: 10000

_requirement_: Category is: Buy Low, Sell High?

**Flag**

None
