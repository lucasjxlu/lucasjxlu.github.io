---
title: 'The Hidden Structure of The Rubik’s Cube'
subtitle: 'An Intuitive Introduction to Group Theory'
date: 2026-01-10
permalink: /blogs/abstractalgebra1/
tags:
  - Mathematics
  - Abstract Algebra
  - Group Theory
---

<p align="center">
  <img src="/images/rc2.jpg"
       alt="A Rubik's Cube, originally known as a Magic Cube"
       width="750">
</p>

Rubik’s Cubes are among the most popular puzzles in the world. A standard Rubik’s Cube has six faces, each painted a different color. The most common version is the 3 × 3 × 3 cube, meaning it is three-dimensional, with three layers along each axis that can be independently rotated.

I’ll assume you already have a basic, intuitive understanding of how a Rubik’s Cube works physically. With that in mind, the image below illustrates the seven basic types of moves you can perform on the cube.

<p align="center">
  <img src="/images/rc_generatingset@2x.jpg"
       alt="Generating set"
       width="400">
</p>

The labels $R$, $L$, $U$, $D$, $B$, and $F$ stand for right, left, up, down, back, and front, respectively. Each label simply indicates which face of the cube is being turned, with each move representing a 90-degree rotation (as you can tell from the colors).

The move labeled $E$ at the top is a special case: it represents *not turning the cube at all*. This may feel a bit strange —- why include a move that doesn’t do anything? We’ll return to this question shortly.

You might also wonder why only these seven moves appear here, when there are clearly many more “interesting” sequences of moves one could perform. After all, a standard 3 × 3 Rubik’s Cube has **43 quintillion** possible configurations —- that’s 43,252,003,274,489,856,000 distinct states, an almost absurdly large number. Why, then, do we start with such a small and simple set of moves? The answer will become clear as we begin to build the theory step by step.

If you’ve ever learned how to solve a Rubik’s Cube, you may remember following a collection of formulas —- or *algorithms* -- for each step of the process. But have you ever stopped to ask why those formulas work? Or whether there are certain states of the cube -- in other words, certain permutations of its pieces -- that can never be reached by legal moves?

Answering questions like these requires mathematics.

To study operations on the cube, we first need a way to *represent* them. The good news is that we already have such a representation, namely the symbols $E$, $R$, $L$, $U$, $D$, $B$, and $F$, which describe our basic turning operations. So now ...

**We are ready to build a mathematical model for the Rubik’s cube!**

The first thing we notice is that no matter how you combine these seven fundamental moves, the result is always *another valid operation on the Rubik’s Cube*. As long as you’re only turning faces —- and not, say, smashing the cube apart —- the cube remains a cube, and each sequence of moves simply transforms it from one state to another.

This means the following: if we let $𝒪$ denote the collection of all possible operations on the cube (in math we call such a collection a set), then whenever $X$ and $Y$ are operations in $𝒪$, performing $X$ followed by $Y$ is still an operation in $𝒪$. Formally, we write:

$$XY \in 𝒪 \text{ for all } X, Y \in 𝒪$$