# :memo: Assignment 3

## Objective

In this assignment, you are required to solve the TSP using the branch and cut method. Add the following types of cuts

- Connectivity cuts
- 2-Connected cuts 
- Blossom inequalities using separation heauristics

In addition, you must compare your solutions with a heuristic using [[Google OR-tools]](https://developers.google.com/optimization/routing/tsp)
## Data 
The data on which your models must be run is in folder STSP. Note that the data formats are either in the form of the lower triangle, upper triangle, or full distance matrix.
- STSP [[Description]](http://comopt.ifi.uni-heidelberg.de/software/TSPLIB95/) 

## Problems
- Set a time limit of 120 s and report the following information by uploading a PDF response file in your repository. 

| Problem Class  | Instance | Best LP Bound | Best IP solution with cuts | Best IP solution without user/lazy cuts | Nodes explored (with cuts) | User cuts added | Lazy cuts added | GAP | Time | Google OR-tools solution |
| ------------- | --- |------------- | ---------------- | ------------------------ |----|---- | ---- | ---- | ----|--------|
| STSP  |  |  |     |        |    | | | | | |


## Rules and Dos and Don'ts
- Run the problem without cuts for 120s as well. Apply the 120s limit to OR-tools as well.
- The time for your codes must include importing the LP file, preprocessing, and B&B code.
- You can use NetworkX for all graph-based subroutines that help identify relevant cuts.
