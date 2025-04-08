# Dynamic Priority Dining Philosophers — Inspired by Pantheon

This Java project implements a smart, deadlock-free solution to the classic Dining Philosophers Problem, inspired by the animated series Pantheon. In the show, Caspian challenges traditional static approaches to concurrency by proposing a dynamic system that evaluates priority in real time. This implementation brings that idea into practice.

Key Concepts
Dynamic Priority Scheduling
Each philosopher is assigned a hunger level and wait time. Their priority is dynamically calculated using the formula:
priority = waitTime + hungerLevel × weight.
Centralized Scheduler
A dedicated scheduler evaluates all pending philosopher requests and allows the one with the highest priority to proceed.
Non-blocking Fork Access
Forks are managed with ReentrantLock.tryLock() to ensure no blocking occurs, avoiding classic deadlocks.
Fairness and Adaptability
Philosophers who wait longer or have higher hunger levels are prioritized, ensuring fairness and preventing starvation.
Features
Multi-threaded, concurrent simulation
Adaptive decision-making with real-time priority adjustments
Deadlock-free and starvation-resistant design
Clean, extensible architecture for learning or experimentation
This project blends computer science fundamentals with modern scheduling logic, offering a practical demonstration of how dynamic systems can outperform rigid protocols in concurrent environments.
