---
layout: post
title: "The halting problem, or, why execution-based testing?"
date: 2026-03-14
categories: tech
---

There is a short list of ideas from early computer science that are (a) worth knowing and (b) just plain fun to think about. One of these is the Halting Problem. This is a landmark undecidability problem from computability theory - the field that describes what can and cannot be computed.  


![A physical implementation of a Turing machine](/Turing_Machine.jpg)

*Caption: A physical implementation of a Turing machine. Will it ever stop? Attribution: Creative Commons*

The problem centres around the question of whether or not any given program will ever stop running, or just get stuck in an infinite loop (assuming it is allowed to run forever by the hardware). The existence of an algorithm that could decide this for all programs is a proven impossibility. Whether a program will stop or not is mathematically undecidable. This is only the most well known undecidability problem in computing. It belongs to a branch of mathematical results developed by luminaries of early 20th Century mathematics and computing including Hilbert, Gödel, Church and Turing, and culminated in Rice’s theorem, proved in 1950. Rice’s theorem generalises the halting problem statement to say that all non-trivial semantic properties of programs are undecidable. Here, a non-trivial semantic property is a behaviour that some, but not all programs can have. For example, it is not possible to determine in general whether a program will produce a specific output for a given input or whether a program computes a particular function. 



This has some important consequences for software development and testing in the age of generative AI and coding agents. Static analysis of code can already be done with linters, type checkers, model checkers and formal verification (like TLA+), and these are very powerful tools. We would obviously want to enhance these methods by adopting new generative AI technologies. However, Rice’s theorem means that, impressive as they are, static analysis of code by LLMs, as with any other method, will always be unable to guarantee completeness of testing. Even if we reach the mythical AGI, no LLM can predict the behaviour of all or any given program just from reading their code, and “any given” may include yours. 
