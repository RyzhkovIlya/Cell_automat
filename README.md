# Cellular automaton
[Cellular automaton wikipedia](https://en.wikipedia.org/wiki/Cellular_automaton)

`Moore neighborhood`

![](https://miro.medium.com/max/376/1*6awbm7DQUsF-m0t01HewWw.png)

`Von Neumann neighborhood`

![](https://miro.medium.com/max/376/1*L7samnL35omszRTBvcXg-Q.png)

## Communication with recommender systems
If we are interested in whether this or that product will be of interest to a particular user?

Or find out which products are best shown to a particular user?

Or which users are best served with a particular product?

Then you can use the method based on cellular automata.
They are based on the method that Stephen Wolfram described in his works, and consists in determining the neighbors for the cell of interest. This method allows you to find out its next state.
This method is applied in this class.
Stages of the class:
- create a matrix of correlated users for the specified specific user;
- from the previous matrix, we correlate products for a specific product
- rearrange the cell we are interested in to the desired position (depending on the "number_layer" parameter - the number of counting layers)
- calculate the number of units that surround our cell
- compare the proportion of units with a given threshold
- if the value is greater than the threshold, then we can say that it is possible to recommend this product to the user; if it is less than the threshold, it is impossible.
- 
As an example, I will give a dataset with movie ratings movie_cell.jpynb.
But to use this class, I changed the ratings to "rated - not rated" and then applied the cellular automaton model.
