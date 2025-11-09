# Z3 Solver

# Preface:

Before talking about SMT solvers, let's solve a variety of interesting puzzles to get acclimated for the next steps.

## Problem 1 (8-queens)

<img src="media/8x8_chessboard.png" alt="ramsey" width="256"/>

You're given $8$ queens to place on a $8 \times 8$ chessboard. Can you find an arrangement of the 
queens on the chessboard so that no queen attack one another?



## Problem 2 (Hooks)

<img src="media/hooks1.png" alt="ramsey" width="256"/>

In the grid above, enter nine 9’s in the outermost hook, eight 8’s in the next hook, then seven 7’s, six 6’s, and so on, down to the one 1 (already entered), so that the row and column sums match the values given along the border. Once all 
numbers are placed the answer is the sum of the values in the shaded square.

## Problem 3 (SEND MORE MONEY)

There is an assignment of unique digits to letters such that the equation `SEND + MORE = MONEY` holds. Find an assignment of the digits to make this true.