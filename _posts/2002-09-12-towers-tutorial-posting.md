---
layout: post
title: "Towers Tutorial"
date: 2022-09-12 22:00:00 +0900
categories: puzzle
---

## Towers Tutorial

![image1](/devblog/assets/Towers/image1.png)

> You have a square grid. On each square of the grid you can build a tower, with its height ranging from 1 to the size of the grid. Around the edge of the grid are some numeric clues.
    Your task is to build a tower on every square, in such a way that:
    - Each row contains every possible height of tower once
    - Each column contains every possible height of tower once
    - Each numeric clue describes the number of towers that can be seen if you look into the square from that direction, assuming that shorter towers are hidden behind taller ones. For example, in a 5×5 grid, a clue marked ‘5’ indicates that the five tower heights must appear in increasing order (otherwise you would not be able to see all five towers), whereas a clue marked ‘1’ indicates that the tallest tower (the one marked 5) must come first.
    <instruction of the tower game from [Simon Tatham's Portable Puzzle Collection](https://www.chiark.greenend.org.uk/~sgtatham/puzzles/js/towers.html)>

