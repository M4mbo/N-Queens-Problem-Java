# N-Queens-Problem-Java
This is my attempt on constructing a visual solution for the NP-complete N Queens problem using Java.

The N Queens problem is an extension of the famous 8 Queens problem. A solution for this problem requires to place N queens on an NxN chessboard without any two queens attacking each other. This program in particular gives an iterative solution to said problem by using the stack ADT.

If you can't see the queen images appear on screen, please change the relative path of the png file.

Approach:
The problem is solved in a non-deterministic manner, because it is NP-complete. This is done by "guessing" possible Queen configurations and only advancing if there are available Queen position on the next column. A boolean type matrix(NxN) was created to hold the validity of previous attempts. Furthermore, a "Queen" type stack ADT was implemented (each layer would have its own row and column). The program will continue pushing new Queens into the stack until it didn't have any tiles per column left. After we reach this state, we pop the last added Queen (column i) and mark the matrix cell as false, making every other cell marked as false from column i+1 true (because these values can change if we create a new Queen in position i). Then we repeat the process until we reach the desired output. The space complexity of this solution is in O(N^2).
