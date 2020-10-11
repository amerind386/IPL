# IPL
IPL playoff simulator

The repository has 3 files:

1. ipl.py - This is a python based playoff probability simulator. Tested with python 2.7 on windows 64 bit computer
2. ipl.xlsm - This is an excel based macro which does the same as the python script.
3. ipl playoff probability deltas.xls - This excel needs to be manually populated and shows the jump/drop in probability before and after a game

Difference between the python and excel version:

- The python version is scalable and can be run when a lot of games are left in the tournament. 
- I have tested the python version when 24 games were left which results in about 16 million combinations. Excel cannot handle this.
- Excel is more suited when the number of games left is 14 or less, ie, 8K+ combinations.
- Why excel then?
  - I wrote the excel macro 4 years ago when I didn't know python
  - The excel can allow you to filter the probabilities and actually look at the sequence of combinations
  
 
How to read the deltas excel:

- Rows 18-26 show the number of possible scenarios for each bucket
- Rows 3-10 converts this number to % by dividing the number of scenarios / total possible scenarios
- I populate rows 18-26 manually by running the python script for before the game scenario. I then remove the next game from pending matches list and then manually increment points for each team to calculate the probability in either case.
- The deltas show the jump/drop in probability for either scenario. This is useful if you are watching a game where your team is not playing and you aren't sure whom to support. Choose the team which increases your team's net possibilities
- Impact of a game is calculated by the absolute sum of deltas for Top 2 and Top 4 scenarios. Higher the number, higher the impact of the game's result on the team's probabilities

[![Run on Repl.it](https://repl.it/badge/github/amerind386/IPL)](https://repl.it/github/amerind386/IPL)
