---
layout: project
type: project
image: img/sudoku.png
title: "Sudoku"
date: 2023-04-21
published: true
labels:
  - Java    
summary: "Created a Sudoku Solver for one of my homework assignments for ICS 211."
---
It was my second semester learning Java and in this assignment we were practicing using recursion. We were given two java files, Sudoku.java and SudokuTest.java. Our objective was to finish the fillSudoku function that would fill in the sudoku table. Recursion is one of those topics that is initially challenging to grasp but becomes an enjoyable and interesting subject the more it is practiced and applied.

This assignment allowed us to dive deeper into applications of recursion in Java. Recursion involves a function calling itself to solve smaller instances of the same problem, making it a perfect fit for a puzzle like Sudoku, the solution involves filling out a grid based on specific rules. The task of completing the fillSudoku function was not just about writing code, but also about thinking recursively, visualizing the steps, and understanding how each recursive call contributes to the overall solution. It tested my logical thinking and patience. 

As I worked through the assignment, I found myself getting more comfortable with the concept of recursion. Each recursive call in the fillSudoku function brought me closer to understanding this approach. It was cool to see how a complex problem could be broken down into simpler parts. This experience was rewarding as it reinforced the power of recursive thinking not just in programming, but in problem-solving in general. Although this assignment took me hours to complete, seeing the Sudoku grid filled in correctly felt great. 

Here is some of my fillSudoku() code:

```cpp
public static boolean fillSudoku(int[][] sudoku) {

		// keeps track if the puzzle has been fully filled or not
		boolean allFilled = true; 
		int row = -1;
		int col = -1;

		// write code that finds the next empty cell using a nested for loop
		// should be recursive
		for (int i = 0; i < sudoku.length; i++) {
			for (int j = 0; j < sudoku.length; j++) {
				if (sudoku[i][j] == 0) { // empty cell found, then row and col will be assigned to row and col
					row = i;
					col = j;
					allFilled = false; // set allFilled to false then break
					break; // first break, inner loop
					// basically, finds the location of the empty cell to be filled out
				}
			}
			if (!allFilled) { // the outer loop
				break; // second break, terminates the outer loop immediately once the first empty cell
						// is found
			}
		}
		if (allFilled) { // puzzle fully filled
			return true; // return true, after outer for loop completes
		}
		for (int num = 1; num < 10; num++) { // tries each number from 1-9 in an empty cell
			sudoku[row][col] = num; // assigns num to sudoku[row][col]
			if (checkSudoku(sudoku, false)) { // sees if resulting grid is valid
				if (fillSudoku(sudoku)) { // checks the rest of the grid can be filled recursively
					return true;
				}
			} // check sudoku does NOT verify that all the cells are filled
				// it verifies that none of the rules are broken
				// loop continues to try next number
		}
		//
		sudoku[row][col] = 0; // resets the cell to zero and returns false
		return false; // backtrack and try a different value,
	}
```
