# Genetic Algorithm for Rock-Paper-Scissors Strategy Learning

Intelligent Systems – Practical Assignment  
University of Pretoria  
Completed: May 2021

---

## Project Overview

This project implements a **Genetic Algorithm (GA)** to discover an optimal strategy for a Rock-Paper-Scissors prediction problem using historical gameplay data.

Each chromosome represents a complete strategy consisting of **81 genes**, where each gene corresponds to the predicted move for a specific game history state (from RRRR to SSSS).

The algorithm evolves populations of strategies over multiple generations using genetic operators such as **selection, crossover, and mutation** to converge toward the optimal strategy derived from large datasets.

👉 **[View Full Project Report (PDF)](docs/EAI320_Practical_Assignment_2.pdf)**

---

## Objectives

- Implement a **Genetic Algorithm** for optimisation
- Derive an **optimal fitness solution** from large CSV datasets
- Evolve candidate strategies using:
  - selection
  - crossover
  - mutation
- Analyse the effect of:
  - population size
  - number of generations
  - crossover rate
  - mutation rate
  - culling
- Evaluate convergence speed and solution quality

---

## Methodology

### Chromosome Representation

- Each chromosome represents a **complete Rock-Paper-Scissors strategy**
- Chromosome length: **81 genes**
- Each gene represents the predicted move (`R`, `P`, or `S`) for a specific game history

### Genetic Algorithm Components

**Initialization**

- Random chromosomes generated using moves `{R, P, S}`

**Selection**

- Roulette selection with ranked probability weighting

**Crossover**

- Parent chromosomes combined using a random crossover ratio

**Mutation**

- Random gene replacement to introduce variation and prevent stagnation

**Fitness Function**

- Fitness determined by comparing chromosome predictions to optimal moves derived from historical datasets (`data1.csv` and `data2.csv`)

---

## Experiments

The GA was evaluated by analysing how different parameters influence convergence:

- Population size (10, 100, 500, 1000)
- Number of generations
- Crossover rate
- Mutation rate
- Cull rate
- Worst-case initialisation scenarios

Results showed that:

- Higher generation counts significantly improve convergence speed
- Mutation is essential to escape poor initial populations
- Higher crossover rates generally produce faster convergence

---

## Tools & Technologies

- Genetic Algorithms
- Evolutionary computation
- Data-driven optimisation
- CSV dataset analysis
- Rock-Paper-Scissors game modelling

---

## Notes

This repository contains the original academic report submitted for the course.

The implementation code and experimental results are included in the **appendix of the report**.
