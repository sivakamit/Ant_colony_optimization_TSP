# Ant colony Optimization TSP

This algorithm is introduced based on the foraging behavior of an ant for seeking a path between their colony and source food. Ant searches for food by roaming around colonies. While moving it will leave its organic compound known as pheromone on the ground. Ants communicate with each other via pheromone trails. When an ant finds some food, it carries as much as it can carry. When returning it leaves pheromone on the paths creating a trail based on the quantity and quality of the food. Ant can smell pheromone. Other ants can smell these and get the food. The higher the pheromone level has a higher probability of choosing that path and the more ants follow the path, the amount of pheromone will also increase on that path.

Ant Density & Ant Quantity: Pheromone is updated in each movement of an ant from one location to another.

Ant Cycle: Pheromone is updated after all ants completed their tour.

Pheromone update:

The formula used to update the pheromone will be as follows: 

<img width="176" alt="image" src="https://user-images.githubusercontent.com/38185827/187322682-729a3775-a486-4ad7-b59a-bea2f72a73c3.png">

 
When the levels are increased or decreased, the trail will be considered as “good” or “bad”
Where pheromone deposited will be xy, ρ is the pheromone evaporation coefficient, m is the number of the ants and Where l is the cost of the ants and Q is the constant

Here I have used three methods Ant colony systems, elitist, Maxmin

### Ant Colony System

In Ant Colony System (ACS), several artificial ants are initially placed at random cities. Each ant builds a tour (a feasible solution of the TSP). It chooses the next city by applying a state transition rule (greedy rule). This rule provides a balance between exploration of new edges and exploitation of accumulated knowledge. A constant amount of pheromone is deposited by each ant at each step on the most favorable route (best tour)

### Elitist

Using the Elitist approach, we try to control the learning parameters. The ants that find the best route (quality) are rewarded more than the other ants. More pheromone is deposited on better routes, giving importance to that tour, and reducing the time to get an optimal solution. The amount of pheromone deposited in based on the quality of the route.

### MaxMin

The MaxMin method aims to get the best of both worlds, a close to optimal solution with a quick execution time. This is achieved by varying the amount to pheromone deposited through the steps. Initially the weight is high, giving a quick learning rate. The weight gradually decreases till 75% completion. Then the model if fine-tuned by applying weights by comparing the results to the global best tour.
At the end of each step, the weights are bound within the max and min pheromone limits to prevent the solution to running astray. The amount of pheromone gradually decreases for the first 75% of iterations. Then amount depends on the quality compared to the best tour.

## Comparisons

### Case 1: 100 cities

<img width="363" alt="image" src="https://user-images.githubusercontent.com/38185827/187322920-abec1058-bd08-4bb5-b640-3c70fd4a7866.png">

<img width="367" alt="image" src="https://user-images.githubusercontent.com/38185827/187322937-1f5fc006-47ba-4d1e-9ce4-66b257e33f63.png">

<img width="366" alt="image" src="https://user-images.githubusercontent.com/38185827/187322948-ccd47a64-2c14-43ef-b1fa-96aadfc9cd1d.png">

### Case 2: 150 cities

<img width="363" alt="image" src="https://user-images.githubusercontent.com/38185827/187323005-f6d241bf-41dc-4513-95db-db338a1301b2.png">

<img width="360" alt="image" src="https://user-images.githubusercontent.com/38185827/187323028-ae2a34e6-b283-49c6-b486-bb5383f2b08d.png">

<img width="361" alt="image" src="https://user-images.githubusercontent.com/38185827/187323041-10a582a9-7a3c-4546-97ca-201b81776de2.png">

### Case 3: 200 cities

<img width="362" alt="image" src="https://user-images.githubusercontent.com/38185827/187323087-1ad301ec-ba84-4225-91ad-96b1bc493826.png">

<img width="361" alt="image" src="https://user-images.githubusercontent.com/38185827/187323103-e22714d6-21cd-4967-bd37-3a43edcc1509.png">

<img width="359" alt="image" src="https://user-images.githubusercontent.com/38185827/187323128-077707d0-9c94-4d02-9394-92bb09af8d84.png">


