# Optimal-Stocking-Level
Compute the average inventory cost, which is defined as the average over all demand scenarios of the total underage cost plus the total overage cost

Write a function named optBaseStock with four input arguments:

levelList: a list of possible stocking levels to optimize over (which can be a range instead of a list).
demandList: a list of demand scenarios.
underage: the unit cost of having too little inventory to meet demand.
overage: the unit cost of having too much inventory.
For each possible stocking level, the function should compute the average inventory cost, which is defined as the average over all demand scenarios of the total underage cost plus the total overage cost. For example, if the stocking level is 10, the demand scenarios are [6,12,14], the underage cost is 9 and the overage is 5, then

The inventory cost for the scenario demand=6 is  (10−6)×5=20 , because the stocking level is 4 units too high. (The overage cost of 5/unit is applied when the inventory is too high.)
The inventory cost for the scenario demand=12 is  (12−10)×9=18 , because the stocking level is 2 units too low. (The underage cost of 9/unit is applied when the inventory is too low.)
The inventory cost for the scenario demand=14 is  (14−10)×9=36 , because the stocking level is 4 units too low.
The average inventory cost for stocking level 10 is  (20+18+36)/3=74/3≈24.67 .

The function should return two objects:

bestLevel: the stocking level in levelList that achieves the minimum average inventory cost (if there is a tie, return the smallest stocking level that yields the minimum cost).
avCost: a dictionary that maps each stocking level to the corresponding average inventory cost.
