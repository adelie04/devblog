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

---

## Before Starting

Lets assume that the game starts with 5x5 grid.

- There are 5 types of tower with different height.
- Tower marked with '1' is the shortest, tower marked with '5' is the longest
- if we arrange them in a row in order of height, it would look like the image below
    ![tower1](/devblog/assets/Towers/tower1.png)
- Let's arrange them randomly
    ![tower2_up](/devblog/assets/Towers/tower2_up.jpg)
- if we change our point of view to face the tower starting with '1', the towers would look like the image below. As you could see, we could see 4 towers on this side: tower 2 is hidden by tower 5
    ![tower2_left](/devblog/assets/Towers/tower2_left.jpg)
- if we change our point of view to face the tower starting with '4', the towers would look like the image below. As you could see, we could only see 2 towers on this side: tower 1, tower 3, and tower 4 is hidden by tower 5
    ![tower2_right](/devblog/assets/Towers/tower2_right.jpg)

---

## How to play

First starting the game, you will be given a grid with numbers.

![towergrid1](/devblog/assets/Towers/towergrid1.png)
In this puzzle, you will fill out the blanks in the grid. Each number of the grid you fill in will mean the height of the tower.

**Additionally, There couldn't be same heights of towers in a same row or column.**

Each numbers shows the number of towers that could be seen in that position. It would be easier to understand with the image below.

![towergrid2](/devblog/assets/Towers/towergrid2.png)

> - towers shown on the front
    ![towers_front_num](/devblog/assets/Towers/towers_front_num.png)
> - towers shown on the right
    ![towers_right_num](/devblog/assets/Towers/towers_right_num.png)
> - towers shown on the left
    ![towers_left_num](/devblog/assets/Towers/towers_left_num.png)
> - towers shown on the back
    ![towers_back_num](/devblog/assets/Towers/towers_back_num.png)
> If we solve the given problem, it would look like
    ![towers_answer](/devblog/assets/Towers/towers_answer.png)
