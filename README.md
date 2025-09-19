# Enhanced Cuckoo Search Algorithm for Node Localization in Wireless Sensor Networks

This code is an implementation of the Enhanced Cuckoo Search algorithm for node localization in wireless sensor networks. The code is written in Python and requires the following libraries: 
- `numpy`
- `matplotlib`
- `scipy` 

The code was run on Google Colab.

The Cuckoo class contains the main function of the algorithm. The class has several constant parameters and variables for the **node density**, **anchor ratio**, and 
**transmission range**.

## Brief Overview of Functions:
1. `plot_graph()` - plots the test field containing labeled nodes
2.  `Alp()` - returns the step size used in Lévy flight
3.  `levy_flight()` - returns a random walk value
4.  `Limit_Nodes()` - prevents the node from exiting the test field.

The Cuckoo class implements the following steps:
- **Anchor Deployment:** The location of anchor nodes is randomly generated within the test field.
- **Unknown Nodes Deployment:** The location of unknown nodes is randomly generated within the test field.
- Backup of original coordinates of Anchor and Unknown nodes
- **Cuckoo search algorithm:** This involves the creation of **cuckoo nests** (each nest represents a candidate solution), **cuckoo egg** laying (new solutions are created by cuckoos and replace existing solutions with a certain probability), and **Lévy flight** (the movement of cuckoos towards better solutions).

## Usage:
To use the code, the user can instantiate an object of the Cuckoo class with the desired values for the parameters. The `plot_graph()` function can then be called to plot the test field. Then the main function is called through a cuckoo object to perform the **Cuckoo Search Algorithm** and obtain the estimated coordinates of the unknown nodes. The algorithm iterates through each node and attempts to localize it by creating cuckoo nests, laying eggs, and performing Lévy flight. The function returns a list of estimated coordinates of the unknown nodes and a list of iteration-wise optimum fitness values.

---
