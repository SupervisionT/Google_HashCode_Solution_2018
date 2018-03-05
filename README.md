# Google HashCode Solution 2018

![alt text](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/hashcode_hero.max-1000x1000.png)

Hey everyone!
In this repo I'll talk about my experience in [Google HashCode challenge](https://hashcode.withgoogle.com/), how to think in the problems and how to solve the Pizza problem and the scheduling problem as well.

[Hash Code](https://hashcode.withgoogle.com/) is a programming competition organized by Google in Europe, Middle-East and Africa. The problems are real engineering problem from Google and that what make it special so you may learn more how to recruit your skills in math, programming, data structure and more to solve a real problem.

You may check the [**past editions**](https://hashcode.withgoogle.com/past_editions.html) to learn more about what real problem Google has.

The challenge has three rounds:
  1. __Practice Round__
  2. __Online Qualification Round__
  3. __Final Round__

### What Google expect from you?
Google is not looking after your code! They are looking for the way you analyze the problem, how you are going to build your algorithm and what data structure techniques that you are going to use.

They are expecting two types of solutions, classic and modern.
* The classic solution should work fine in a small dataset but not for big one. Also don't expect the get out with the optimum solution. 
* The modern solution focus on the performance and to reduce the complexity so it'll work fast for any dataset size. Also it works to optimize the solution and to minimize the error.

In this repo we'll talk about the first and second rounds. The third round will be held in *Dublin* for the top scoring teams.
We'll show a classic solution and a modern solution for each round.

## __Practice Round.__

The practice round is about slicing pizza, easy!
Google is asking you to slice the pizza to get the maximum number of slices with a condition. Each slice should have a certain number from each ingredient

![alt text](http://codeforces.com/predownloaded/a3/6f/a36fd2408b59da01e83298660645137c095a04c9.png)

You may read the problem statement and check the data from [here](https://github.com/SupervisionT/Google_HashCode_Solution_2018/tree/master/Pizza)

So how to solve it? let us go through both solutions, classic and modern.

* *__Pizza Classic Solution__*

Classic solutions are fine for small scale, small datasets and small projects as well. At the end you'll have what you need and it works. In the Classic solutions we'll use loops, nested loops and more loops!! and most of the times the big O notation will not be happy because it'll have exponential complexity as the data grow things will get more complex and costly.

Let's go with the flow and see where things will lead us ...

To solve the problem, we'll loop over all the items and check for all possible combinations for each cell, choose one combination then move to the next point. That simple !!

This algorithm called *The Greedy Algorithm*. It is easier to code and makes the choice that looks best at the moment. In our case we hope that the local optimal choice will lead to a global optimal solution. But that is not true in this because there are no guarantees that your local choice will be the optimal for the next cell. Also you blocked a group of choices by your decision.

To avoid this we may find all the possible combinations for each cell then iterate over all the possible combinations to find the best solution. And this is a solid plan.

For small pizza this will work like a charm. But if you move to medium pizza mostly will code will take a very long time before it may crush! Your memory will not be able to handle it. As a quick eyeliner, break down your pizza into many small pieces and run your algorithm on each piece and it'll work. The thing is you'll lose the possible combinations at edges for each slice. There are some solutions to improve this method but at the end this is not the optimal solution.

Finally, to avoid nested loops there are a couple of methods that can be used. For example, you can convert the 2d array (x, y) into a single row array (1, Number_Of_All_Elements) then loop over them. But you need to find the right formula to get the combinations for each cell. Another way is to us a shifted version from the original 2d array then you can multiply them to get the combinations.

* *__Pizza Modern Solution__*

![alt text](http://cucsa.org.uk/wp-content/uploads/2015/10/Work_In_Progress-300x269.png)

## __Online Qualification Round.__

![alt text](http://cucsa.org.uk/wp-content/uploads/2015/10/Work_In_Progress-300x269.png)
