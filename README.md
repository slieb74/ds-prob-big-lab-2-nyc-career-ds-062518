
## Gambling and sports betting

## Exercise 1: Soccer World Cup

Belgium is planning on making it far in the soccer world cup. Currently waiting from the group phase and already knowing that they are qualified, Belgium knows that, there are 4 potential opponents they may face in the quarter finals. Projections for playing the following countries look as follows:

- Brazil, with a 30% chance.
- Colombia, with a 15% chance
- Sweden, with 35% chance
- Switzerland, with a 10% chance.

According to online betting company Ladbrokes, Belgium's chances of winning against these contries are given by the following probabilities:

- Against Brazil, Belgium has a 27% chance of winning.
- Against Colombia, Belgium has a 68% chance of winning.
- Against Sweden, Belgium has a 55% chance of winning.
- Against Switzerland, Belgium has a 73% chance of winning.


Fast forward, and turns out Belgium has won the quarter finals. What is the probability that they did NOT play against Brazil?

### Solution

$P(\text{not play against Brazil} \mid \text{win})= 1-P(\text{play against Brazil} \mid \text{win})$ 

$P(\text{play against Brazil} \mid \text{win})= \dfrac{P(\text{win} \mid\text{play against Brazil})P(\text{play against Brazil})}{\displaystyle\sum_i^{i \in 
\text{[Bra,Col,Swe,Swi]}} {P(\text{win} \mid\text{play against country }i)P(\text{play against country }i)}}$


```python
prob_Brazil_if_won = (0.3*0.27)/(0.3*0.27+ 0.15*0.68+0.35*0.55+0.1*0.73)
prob_not_Brazil=1-prob_Brazil_if_won

prob_not_Brazil # correct answer: 0.8193979933110368
```

## Exercise 2: Probability that each person has one ace

A deck of 52 cards is distributed between 4 people (so each player gets 13 cards). What is the probability that each player gets exactly one ace?

### Solution

probability that the first player gets exactly one ace.

$\dfrac{\displaystyle{{48}\choose{12}}\displaystyle{{4}\choose{1}}}{\displaystyle{{52}\choose{13}}}$

Then, on to the second player, only 39 cards are left in the deck, and exactly 3 aces.



$\dfrac{\displaystyle{{36}\choose{12}}\displaystyle{{3}\choose{1}}}{\displaystyle{{39}\choose{13}}}$

and so on. muliplying it all, this boils down to:

$\dfrac{4!\displaystyle{{48}\choose{12}}\displaystyle{{36}\choose{12}}\displaystyle{{24}\choose{12}}\displaystyle{{12}\choose{12}}}{\displaystyle{{52}\choose{13}}\displaystyle{{39}\choose{13}}\displaystyle{{26}\choose{13}}\displaystyle{{13}\choose{13}}}$


```python
import math
import scipy.special as prob

numerator = (math.factorial(4)* prob.comb(48,12)* prob.comb(36,12)* prob.comb(24,12))
denominator = (prob.comb(52,13)* prob.comb(39,13)* prob.comb(26,13))

everyone_one_ace = numerator/denominator

everyone_one_ace  # correct answer: 0.10549819927971187
```

## Exercise 3: Poker: four of a kind

If you're being dealt 5 cards, what is the probability for you to get four of a kind?

### Solution

$\dfrac{\displaystyle{{13}\choose{1}}\displaystyle{{4}\choose{4}}\displaystyle{{48}\choose{1}}}{\displaystyle{{52}\choose{5}}}$


```python
four_of_a_kind = (13*48)/prob.comb(52,5)
four_of_a_kind  # correct answer: 0.00024009603841536616
```

## Exercise 4: Poker: 3 of a kind

Now calculate the probability that you get three of a kind. This is harder!! you have to take two things into account:
- you want to get a three of a kind, and not "by coincidence" a full house.
- you want to get a three of a kind, and not "by coincidence" a four of a kind.

### Solution

$\dfrac{\displaystyle{{13}\choose{1}}\displaystyle{{4}\choose{3}}\times\displaystyle{{12}\choose{2}}\displaystyle{{4}\choose{1}}\displaystyle{{4}\choose{1}}}{\displaystyle{{52}\choose{5}}}$


```python
three_of_a_kind = (13*prob.comb(4,3)*prob.comb(12,2)*4*4)/prob.comb(52,5)
three_of_a_kind # correct answer: 0.02112845138055222
```

# sources

https://owlcation.com/stem/Cracking-Combinatorics-and-Probability-Card-Game-Problems
