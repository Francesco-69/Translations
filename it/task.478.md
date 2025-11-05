_This problem was kindly created for us by [**Clive Fraser**](/index/user_profile/csfpython) - many thanks!_

Alfie the robot works in a large factory complex. The complex is a square of side 5 km. Alfie's job is to collect partially or completely finished items from one collection/delivery point in the complex and to deliver them to another point. The factory complex has a number of lanes running parallel to the sides of the square; one set going from east to west and the other from north to south. So these lanes always cross each other at right angles. The lanes run above the working area of the factory so that Alfie can move without interfering with any of the work areas. The collection/delivery points are all placed at intersections of the two sets of lanes. Alfie will always choose the shortest distance between two points but is constrained to follow the lanes; so he must always be travelling parallel to one of the edges of the square. The collection/delivery points are distinguished by their (x,y) coordinates, where x and y are the distances (in metres) east and south respectively, of one of the corners of the square which has the coordinates (0,0).

Alfie has his docking station at the point (0,0). When at the docking station, Alfie is sent a list of deliveries which he has to make. Each of these gives the coordinates of the collection/delivery point where he is to pick up a package, and the coordinates of the point where the package is to be delivered. In order to improve efficiency, each delivery is sent in a standard sized crate. There may be many items inside the crate but Alfie regards a crate as a single delivery. If a collection/delivery point needs to send multiple crates to the same destination, each of these has to be listed as a separate delivery. Alfie is designed to be able to carry two crates (at most) at any one time.

When Alfie gets a list of deliveries he uses a specially designed software package to work out the optimum route for the collection and delivery of all of the crates. The route takes him from his docking station, through all of the collections and deliveries and then back to the docking station. The software ensures that Alfie will never need to be carrying more than 2 crates. The software also ensures that the total distance travelled by Alfie is a minimum.

In this problem you will be given a delivery list for Alfie and are asked to find the distance travelled by Alfie in making all of the deliveries, after starting from the docking station and finally returning to the docking station.

The first line of the problem will be a single integer N denoting the number of collections and deliveries to be made. Each of the following N lines will consist of four integers X1, Y1, X2 and Y2, separated by spaces. (X1,Y1) gives the location of the point from which a crate needs to be collected. (X2,Y2) gives the location of the point where the same crate needs to be delivered. Your answer is the length (in metres) of the optimum route taken by Alfie in completing the list of deliveries and returning to the docking station.

The Example below has N = 3, so there are 3 crates to be collected and delivered. The optimum route has a length of 18206 metres and is executed as described in the following table. (Note that Crates Carried refers to the number of crates being carried by Alfie, after reaching the given location)

	  Location	Total Distance	Crates Carried
	
	      (0,0) 		0 	       0	Start at docking station
	  (737,482) 	     1219 	       1	Collect crate number 2
	(3855,4069) 	     7924 	       2	Collect crate number 1
	(4230,4175)	     8405 	       1	Deliver crate number 2
	(4837,3926) 	     9261 	       2	Collect crate number 3
	(2127,1979) 	    13918 	       1	Deliver crate number 3
	(1542,2070) 	    14594 	       0	Deliver crate number 1
	      (0,0) 	    18206 	       0	Return to docking station

Example:

	input:
	3
	3855 4069 1542 2070
	737 482 4230 4175
	4837 3926 2127 1979
	
	answer:
	18206