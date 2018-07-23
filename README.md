
## Gambling and sports betting

## Exercise 1: Soccer World Cup

Belgium is planning on making it far in the soccer world cup. Currently waiting from the group phase and already knowing that they are qualified, Belgium knows that there are 4 potential opponents they may face in the quarter finals. Projections for playing the following countries look as follows:

- Brazil, with a 30% chance.
- Colombia, with a 15% chance
- Sweden, with 35% chance
- Switzerland, with a 10% chance.

According to online betting company Ladbrokes, Belgiums chances of winning against these contries are given by the following probabilities:

- Against Brazil, Belgium has a 27% chance of winning.
- Against Colombia, Belgium has a 68% chance of winning.
- Against Sweden, Belgium has a 55% chance of winning.
- Against Switzerland, Belgium has a 73% chance of winning.


Fast forward, and it turns out Belgium has won the quarter finals. What is the probability that they did NOT play against Brazil?

### Solution


```python
#
prob_not_Brazil = None
prob_not_Brazil # correct answer: 0.8193979933110368d
```

## Exercise 2: Probability that each person has one ace

A deck of 52 cards is distributed between 4 people (so each player gets 13 cards). What is the probability that each player gets exactly one ace?

### Solution


```python
import math
import scipy.special as prob

#
#
everyone_one_ace = None

everyone_one_ace # correct answer: 0.10549819927971187
```

## Exercise 3: Poker: four of a kind

If you're being dealt 5 cards, what is the probability for you to get four of a kind?

### Solution


```python
four_of_a_kind = None
four_of_a_kind # correct answer: 0.00024009603841536616
```

## Exercise 4: Poker: 3 of a kind

Now calculate the probability that you get three of a kind. This is harder!! you have to take two things into account:
- you want to get a three of a kind, and not "by coincidence" a full house.
- you want to get a three of a kind, and not "by coincidence" a four of a kind.

### Solution


```python
three_of_a_kind = None
three_of_a_kind # correct answer: 0.02112845138055222
```

# sources

https://owlcation.com/stem/Cracking-Combinatorics-and-Probability-Card-Game-Problems
