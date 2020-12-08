# deep-rl-bootcamp-lab03
Lab 3 of the Deep RL bootcamp from MIT


Task 1 & 2 Implemented
Task 3 not able to complete due to setup issues involving the Prelab Setup and Lab 3 Setup


## Alternative Solution
#### Based on the Repository [https://github.com/sagerpascal/deep-rl-bootcamp-lab3](https://github.com/sagerpascal/deep-rl-bootcamp-lab3)
Since it was not possible to get the implementation running on the current setup, the following results are based on the solution from Pascal Sager with additional Research.




| | Average Return | Average Discounted Return | Average Error |
|-|----------------|---------------------------|---------------|
|Baseline of Pong|<img alt="Average Return" src="/graphs/Baseline_Average_Return.png" width="500">|<img alt="Average Discounted Return" src="/graphs/Baseline_Average_Discounted_Return.png" width="500">|<img alt="Average Error" src="/graphs/Baseline_Average_Error.png" width="500">|
|||||
|Increased Discount Factor gamma (0.99 -> 0.995)|<img alt="Average Return Increased Discount" src="/graphs/Discount_Factor_Average_Return_Increased.png" width="500">|<img alt="Average Discounted Return Increased Discount" src="/graphs/Discount_Factor_Average_Discounted_Return_Increased.png" width="500">|<img alt="Average Error Increased Discount" src="/graphs/Discount_Factor_Average_Error_Increased.png" width="500">|
|Decreased Discount Factor gamme (0.99 -> 0.985)|<img alt="Average Return Decreased Discount" src="/graphs/Discount_Factor_Average_Return_Decreased.png" width="500">|<img alt="Average Discounted Return Decreased Discount" src="/graphs/Discount_Factor_Average_Discounted_Return_Decreased.png" width="500">|<img alt="Average Error Decreased Discount" src="/graphs/Discount_Factor_Average_Error_Decreased.png" width="500">|
||||
|Increasing the Fraction of Expl. Parameter epsilon (0.1 -> 0.2)|<img alt="Average Return Increased Epsilon" src="/graphs/Epsilon_Average_Return_Increasing.png" width="500">|<img alt="Average Discounted Return Increased Epsilon" src="/graphs/Epsilon_Average_Discounted_Return_Increasing.png" width="500">|<img alt="Average Error Increased Epsilon" src="/graphs/Epsilon_Average_Error_Increasing.png" width="500">|
|Decreasing the Fraction of Expl. Parameter epsilon (0.1 -> 0.05)|<img alt="Average Return Decreased Epsilon" src="/graphs/Epsilon_Average_Return_Decreasing.png" width="500">|<img alt="Average Discounted Return Decreased Epsilon" src="/graphs/Epsilon_Average_Discounted_Return_Decreasing.png" width="500">|<img alt="Average Error Decreased Epsilon" src="/graphs/Epsilon_Average_Error_Decreasing.png" width="500">|
||||
|Increasing the Update Frequncy (every 4 iters -> every 2 iters)|<img alt="Average Return Increased Update Frequency" src="/graphs/Update_Frequency_Average_Return_Increasing.png" width="500">|<img alt="Average Discounted Return Increased Update Frequency" src="/graphs/Update_Frequency_Average_Discounted_Return_Increasing.png" width="500">|<img alt="Average Error Increased Update Frequency" src="/graphs/Update_Frequency_Average_Error_Increasing.png" width="500">|
|Decreasing the Update Frequncy (every 4 iters -> every 6 iters)|<img alt="Average Return Decreased Update Frequency" src="/graphs/Update_Frequency_Average_Return_Decreasing.png" width="500">|<img alt="Average Discounted Return Decreased Update Frequency" src="/graphs/Update_Frequency_Average_Discounted_Return_Decreasing.png" width="500">|<img alt="Average Error Decreased Update Frequency" src="/graphs/Update_Frequency_Average_Error_Decreasing.png" width="500">|



### Analysis

#### Discount Factor
The increased discount factor includes more conditions of the future and leads to better results at first. The learning over time however is not continuously improving and fluctuates a lot more. If the discount factors is decreased, the learning rate improves the learning rate and over a shorter amount of time but also starts at a reasonable level. Therefore a reduction of the discount factor can be applied to this model, since the problem does not need to consider as many steps in the future as implemented in the baseline.

#### Fraction of the exploration parameter Epsilon
Epsilon is being reduced from 1 to 0.05 over time during the learning. The Fraction parameter determines the speed at which this reduction is being done. If this fraction parameter is being chosen bigger, the initial learning rate is also faster but with a drawback of having more random decisions and therefore it is not as stable as the baseline. Lowering the Fraction parameter leads to a more stable learning curve, but it might take longer to improve (based on if the random decisions are helpful or not). For the problem of Pong, epsilon can be increased for faster results.

#### Update Frequency of Q-Values
The amount of iterations it takes until an update of the Q-Values is being done, is chosen by this parameter. The parameters are updated after a fixed set of iterations (default is 4 iterations). If the frequency is lower, the initial learning is obviously lower. After the initial slow curve, the results improve and are better than the baseline implementation. Increasing the update frequency is leading to worse results, since bad decisions might be taken in consideration more often. Therefore it is adviced to decrease the frequency at which the Q-Values are updated for the problem of Pong. 

#### Final Conclusion
The three analyzed hyperparameters that determine the learning process of this model can be optimized in comparison to the baseline that was given by the excercise. They improve the speed at which the model is being trained, but also the result in the end and have to be chosen carefully to get the best model.
