###CS 312 Help Session - Project 2

#####Gist of the Project

The project page does an excellent example of detailing what is expected and gives tips on how to implement it:
* [CS 312 Winter 2015: Project 2](http://wiki.cs.byu.edu/cs-312/project-2)

Another resource that may be helpful is the project page from Dr. Martinez's class. This is given as a helpful resource only, so it may disappear at any time, and may conflict with Dr. Ringger's project page.
* [CS 312 Fall 2014: Project 2](http://axon.cs.byu.edu/~martinez/classes/312/Projects/Project2/project2.html) 

Anyways, the major steps of the problem are:

1. Recursively divide the set of points given until you reach a base case.
2. Sort the points in your base case set (you choose how you would like to order them)
3. As we return back up the stack with a left and a right hull, we recursively merge two hulls together, maintaining the order as we go through the merging process
4. By maintaining the order of the points as they form the hull, we can "move" up and down the hull and use that to find tangents between the two hulls.
5. If we find an upper and lower tangent between two hulls, we can use those to merge and then return one unified hull.

#####Demonstration
*Now we show a shiny version of the project to see the algorithm in action. Yay for coming to the help session! If you aren't here and there is enough interest, I can add some screen shots to these notes later. See the `More Info` section for how to contact us to demonstrate your interest.*

#####More Info

Always check the syllabus, project specs for help, try searching Google, then the Google Group for the class, and finally we are available through the TA Email, our office hours, and by appointment. Preferably in that order.

###Questions?
