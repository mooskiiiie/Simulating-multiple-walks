# Simulating-multiple-walks

## Simulate multiple walks
A single random walk is one thing, but that doesn't tell you if you have a good chance at winning the bet.

To get an idea about how big your chances are of reaching 60 steps, you can repeatedly simulate the random walk and collect the results.
### Instructions
-Fill in the specification of the for loop so that the random walk is simulated 10 times.
-After the random_walk array is entirely populated, append the array to the all_walks list.
-Finally, after the top-level for loop, print out all_walks.


## Visualize all walks
all_walks is a list of lists: every sub-list represents a single random walk. If you convert this list of lists to a Numpy array, you can start making interesting plots! matplotlib.pyplot is already imported as plt.
## Instructions
-Use np.array() to convert all_walks to a Numpy array, np_aw.
-Try to use plt.plot() on np_aw. Also include plt.show(). Does it work out of the box?
-Transpose np_aw by calling np.transpose() on np_aw. Call the result np_aw_t. Now every row in np_all_walks represents the position after 1 throw for the 10 random walks.
-Use plt.plot() to plot np_aw_t; also include a plt.show(). Does it look better this time?

### Instructions 
-Change the range() function so that the simulation is performed 250 times.
-Finish the if condition so that step is set to 0 if a random float is less or equal to 0.001. Use np.random.rand().

## Plot the distribution
All these fancy visualizations have put us on a sidetrack. We still have to solve the million-dollar problem: What are the odds that you'll reach 60 steps high on the Empire State Building?

Basically, you want to know about the end points of all the random walks you've simulated. These end points have a certain distribution that you can visualize with a histogram.
### Instructions
-To make sure we've got enough simulations, go crazy. Simulate the random walk 500 times.
-From np_aw_t, select the last row. This contains the endpoint of all 500 random walks you've simulated. Store this Numpy array as ends.
-Use plt.hist() to build a histogram of ends. Don't forget plt.show() to display the plot.


## To get the probability of reaching 60 steps high:
Get the number of integers in the last index of "ends" that are greater or equal to 60 and divide it to 500 (number of walks taken)
