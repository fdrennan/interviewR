# interviewR
An R repo with questions for a Quantum interviewee. The questions are specified below but any data required to solve the problem is either in `Quantum_Assessment.Rmd` or `daily_data.rda`.

Please return you solution in a well organized and clean RMarkdown file. Clean and well documented code is highly encouraged. Extensive use of tidyverse tools is recommended.  


# The Birthday Problem

Assumptions:

1. Birthdays are equally likely between Jan 1 and Dec 31. 
2. Leap years are ignored
3. $n$: people in a room
4. $p$: the probability that at least two people in the room share a birthday

Using ggplot, display the value of $p$ against $n$. 

# The Advertising Problem

You are running an advertising campaign with Facebook and have data available to make decisions about the allocation of your budget. You are tasked to allocate $500 dollars of budget among three advertisments which have historical performance data by writing a linear program. 

Data Available from February.

+ $s_n$ - Dollars spent for advertisements in the prior month for advertisement $n$. Called `amount_spent`.
+ $i_n$ - Impressions obtained with $s$ dollars in the prior month for advertisement $n$. Called `impressions_obtained`.
+ $c_n$ - Clicks obtained with $s$ dollars in the prior month for advertisement $n$. Called `clicks_obtained`.
+ $k_n$ - The Key Performance Indicator: $\frac{i_n}{s_n}$ 
+ $x_n$ - Budgets for the new month. Your decision variables.

You have 500 dollars to spend this month and three advertisments, while maximizing impressions. The budget allocated to each advertisement is $x_1...x_3$ respectively. 


## Bonus 1:
Add a constraint to keep expected clicks above 1350

## Bonus 2:
Add a constraint to force $x_3$ to always receive at least thirty percent of the total budget allocated to $x_2$ and $x_3$. 

For example, if the sum of advertisment 2 and 3 is 250 dollars, then $250 = x_2 + x_3$ and $x_3 >= .3 (x_2 + x_3)$

# EDA

Take the file from the repo called `daily_data.rda` and do an EDA. What do you find? The lowest level of an advertisment is an adgroup id. 
