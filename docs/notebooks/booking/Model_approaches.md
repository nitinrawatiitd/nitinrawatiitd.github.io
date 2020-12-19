# Methods to modelling recommendation

There are two entities in a recommender system
1. The thing that has to be recommended - item, dish, trip, music etc
2. The person/event that the recommendation has to be present to

There are 2 main methods to creating a recommender system -   
1. **Collaborative filtering based** - the main idea that rules collaborative methods is that these past user-item interactions are sufficient to detect similar users and/or similar items and make predictions based on these estimated proximities. The class of collaborative filtering algorithms is divided into two sub-categories
* **Memory based** - Memory based approaches directly works with values of recorded interactions, assuming no model, and are essentially based on nearest neighbours search (for example, find the closest users from a user of interest and suggest the most popular items among these neighbours). So -
  * Large sparse vectors of past interactions
  * Recommendation done using nearest neighbours


* **Model based** - Model based approaches assume an underlying “generative” model that explains the user-item interactions and try to discover it in order to make new predictions.
  * new representation of users and items are built based on a model (small dense vectors)
  * recommendation are done using the model information


  **Advantages** - It requires no information about users or items. So can be used in many situations   
  **Disadvantages** - Suffers from the cold start problem in situations when you don't have the user item interaction. There are other recommendations that can be show in those situations (most popular items)

2. **Content based method** -
