# gobang_project
CS1356 (Yr 1 course) mini project 3 - goal: write a naive AI to defeat baseline gobang AI

## Project 目標

given package 裡有baseline (你的對手) 及player_random.cpp

player_random.cpp 會隨機下棋

功課目標： modify player_random.cpp 來打敗baseline，即要寫捉五子棋的algorithm


## Algorithm 設計指導
詳見gobang_algo_design_intro.pdf

### 設計步驗

### 1. 設定state value function

- 即計算邊一步落得比較好的公式

最簡單的state value function:

 Value = # of 3, 4 and 5 continuous player’s discs
-# of 4 and 5 continuous opponent’s discs

即我行完呢步之後，我有3/4/5粒連埋的數量- 對方有4/5粒連埋的數量

### 2. 用search tree 來推演未來幾步的state value function

search tree 模式: minimax, Alpha-beta pruning

minimax

- 推演未來n 步的state value function, 再揀n步後對自己最高分的choice,由後推返上前決定呢一步要點行

詳見gobang_algo_design_intro.pdf P.20-36

alpha-beta pruning

- 同minimax一樣,但多一步判斷冇用的branch提早斬走


詳見gobang_algo_design_intro.pdf P.37

### minimax and alpha beta pruning explain

https://www.youtube.com/watch?v=l-hh51ncgDI

## Environment Setting

如何compile -> 需要makefile, 詳見 document\gobang_env_setting.pdf




