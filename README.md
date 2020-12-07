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
|Increasing the Update Frequncy (every 4 iters -> every 2 iters)|||
|Decreasing the Update Frequncy (every 4 iters -> every 6 iters)|||
