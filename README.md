## What happens if we try to use genetic algoritm to classify text?

*Homework Topic:* Text Classification with Genetic Algorithm / Hill Climbing

Find a text classification dataset with at least 100 examples and 2 classes (positive/negative, sports/economy, etc.). Individuals will consist of a list of N words. The first part will represent the first class and the second part will represent the second class. For example, an individual can be represented as ["beautiful", "amazing", ..., "awesome"]["terrible", "bad", ..., "disliked"]. This individual will classify 100 examples according to whether they contain these words and achieve a classification success rate. This success value will be used as the fitness function. The number of words belonging to class 1 and class 2 in the text can be found, and the operation can be performed according to these values. In case of a tie, the class can be randomly determined. Initially, words will be randomly assigned to all individuals. Throughout the process, operations such as crossover and random word replacement will be applied to try to increase the fitness value of the individuals. The word lists of individuals will be optimized using genetic algorithm or hill climbing.


### General Evaluation

I believe that using "F1 score" for fitness has a positive impact on the overall process when evaluating the results. Although I haven't conducted a comprehensive experiment to share statistical information, my observation is in this direction. 

In almost all runs, when we increase the mutation, the results improve. However, the same is not true for crossover, sometimes it's effective, sometimes it's not. I kept the number of generations at 200 because we can already see the generations underneath in the graph. 

The population size is also one of the factors that significantly affect the results, generally, when we increase the population, the results also improve. I didn't use a "very" large population because it turned my process into incredibly long periods and wasn't appropriate for comparison. Using a very large population also negatively affected the performance in terms of time and results. 

Additionally, I used an approach that we can consider a bit of a cheat to improve the results. When I did some research, I learned about a method called "elitism." This method guarantees the transfer of the best individual to the next generation. Therefore, we don't lose points in the score. When we work completely randomly, the results naturally have more fluctuations and lower scores.

### Example Results

Elitizm and F1 fitness are used for Data1 (food)

<img width="700" alt="image" src="https://user-images.githubusercontent.com/44132720/236626092-61af2f92-3434-484d-94ad-9bdfc1c33601.png">
