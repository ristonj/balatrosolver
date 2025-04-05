# Balatro Solver
## Introduction
[Balatro](https://store.steampowered.com/app/2379780/Balatro/) is a rogue-like deck builder based on poker. Here is the basic premise:

1. You win by completing 8 "antes", or levels.
1. Each level consists of a small blind, a big blind, and a boss blind.
1. The goal of each level is to score a certain number of points (chips) within four of hands.
1. You start with a standard 52-card deck. Each hand is dealt from this deck.
1. For each hand you are dealt eight cards. You can play up to five of them to make a poker hand.
1. Each poker hand is worth a number of chips and a multiplier. Each card within that poker hand is also worth a number of chips (A = 11, KQJ = 10, all other cards face value).
1. The hand is scored by the number of chips for the poker hand plus the value of cards within that hand. That sum is then multiplied by the multiplier to get the final score for the hand.
1. If the player gets a number of points greater than or equal to the blind value before running out of hands, they advance to the next blind. Otherwise, they lose and have to start over.
