# ABM-NetLogo-assignment
This repository contains the code from the “Introduction to Agent-Based Modeling” course by Complexity Explorer, part of the Santa Fe Institute. The course focused on coding with NetLogo for agent-based modeling. This code is the final assignment. Note that this model is not based on a theory but is intended for educational purposes.

The assignments were peer-reviewed by fellow students, providing valuable feedback for improvement. One reviewer recommended Bryan Caplan’s book, “The Myth of the Rational Voter.”

## WHAT IS IT?

The model is designed to simulate the decision-making process of voters in an election. The focus is specifically on a subset of voters who are uncertain whether to vote or not.

## HOW IT WORKS

In this model, there are three principal types of agents involved, each representing a different type of voter in an election. Here’s a description of each agent type:

1. Definite Voters: They will definitely vote in the election. Their decision to vote is not influenced by any other factors in the model.
2. Definite Non-Voters: They will definitely not vote in the election. Similar to the Definite Voters, their decision is fixed and not influenced by any other factors in the model.
3. Uncertain Voters: These agents represent the remaining population that is uncertain about whether to vote or not. Their decision to vote or abstain is influenced by their perception of the turnout percentage and the strategy they employ.

Each Uncertain Voter can employ one of these two strategies:
1. Strategy 0: An agent with this strategy assumes that the turnout percentage will remain the same in the next tick.
2. Strategy 1: An agent with this strategy has a more complex evaluation: He sees the difference between the turnout percentage and the desired one:

1. If the turnout percentage is less than the desired turnout percentage, and the difference is more than 20%, the agent assumes that non-voters will worry about the turnout percentage, so at least 60% of them will vote.
2. If the turnout percentage is less than the desired turnout percentage, but the difference is equal to or less than 20%, the agent assumes that non-voters will not worry too much about the turnout percentage, so at most 5% of them will vote.
3. If the turnout percentage is equal to or more than the desired turnout percentage, and the difference is more than 20%, the agent assumes that voters do not intend to keep this gap, so many will not vote (at least, as much as 130% of the difference between these two numbers).
4. If the turnout percentage is equal to or more than the desired turnout percentage, and the difference is less than or equal to 20%, since the voters do not want to take a risk, they are unlikely to abstain from voting. Therefore, the agent assumes that the turnout percentage will remain the same.

In this model, we observe how employing these strategies by agents can influence the turnout percentage of an election

## HOW TO USE IT

In this model, you can determine what percentage of the total agents will definitely vote and what percentage will not vote. Plus, you can determine the desired turnout percentage, and it is also possible to determine what percentage of undecided agents will employ strategy 1, which is the more complex strategy. Then, it shows you how many agents decide to vote and what the real turnout percentage will be.

## THINGS TO NOTICE

The sum of the percentages of the agents who definitely vote and those who do not vote must be less than 101. However, if you unintentionally determine them incorrectly, the model will notify you.

## THINGS TO TRY

We suggest that by changing the inputs, you can see if the people of a society can bring the turnout percentage in an election closer to what they want without coordinating with each other and only by making decisions based on announced statistics (similar to polls in the real world). Also, check if people are more inclined towards one of these two strategies, and whether this inclination has an effect on the turnout percentage.

## EXTENDING THE MODEL

By making the strategies that can be adopted by agents more complex, more realistic results can be achieved. Especially if the adopted strategy becomes dynamic and according to the past experience, the strategy can be modified.
