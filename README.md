# Balatro Solver
## Introduction
[Balatro](https://store.steampowered.com/app/2379780/Balatro/) is a rogue-like deck builder based on poker. Here is the basic premise:

1. You win by completing 8 "antes", or levels.
1. Each level consists of a small blind, a big blind, and a boss blind.
1. The goal of each level is to score a certain number of points (chips) within four of hands.
1. You start with a standard 52-card deck. Each hand is dealt from this deck.
1. Each deck also has a special ability.
1. For each hand you are dealt eight cards. You can play up to five of them to make a poker hand.
1. You may also discard up to five cards up to three times.
1. Each poker hand is worth a number of chips and a multiplier. Each card within that poker hand is also worth a number of chips (A = 11, KQJ = 10, all other cards face value).
1. The hand is scored by the number of chips for the poker hand plus the value of cards within that hand. That sum is then multiplied by the multiplier to get the final score for the hand.
1. If the player gets a number of points greater than or equal to the blind value before running out of hands, they advance to the next blind. Otherwise, they lose and have to start over.

The deck building aspects come in several forms:

1. Jokers which can change any of the above rules.
1. Planet cards which increase the chips and multipliers of certain hands.
1. Tarot Cards which change aspects of both cards and jokers. Some also let you draw additional cards/jokers/planets.
1. Spectral cards which act like Tarot Cards but are stronger.

## Purpose of this program

Given a hand, along with a set of jokers, what is the play that will lead to the most chips, both now and in the future? I'm going to analyze the following, and code it in this order:

1. Given an 8 card hand, what is the best 5 card poker hand we can make from these 8 cards?
2. For a poker hand with less than 5 cards, is it worth it to play extra cards that don't count to hopefully get better cards in the future?
3. Is discarding going to get you more points than playing your hand?
4. Make value of hands modifiable.
5. Include jokers in analysis.
6. Include traits on cards that can be added by tarot cards and spectral cards.

I'll add items to calculate as I think of them.

## Infrastructure

I want to use this program as a chance to practice my knowledge of Kubernetes. As such, I'm going to implement a front-end in Angular, a middle-tier in C#, and have a MongoDB backend for some NoSQL practice. I'll put these in separate pods and create a persistent volume for the MongoDB backend.
