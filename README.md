# SIR Model Simulation with Cellular Automaton

In this lab, we will implement a simulation of an SIR model using a cellular automaton. The goal is to design a simulation of the Kermack and McKendrick system of ordinary differential equations (ODEs) for the SIR model:

\[
\frac{dS}{dt} = -\beta SI,
\]

\[
\frac{dI}{dt} = \beta SI - \gamma I,
\]

\[
\frac{dR}{dt} = \gamma I.
\]

## Simulation Overview

The simulation will be carried out on a rectangular grid of size \(M \times N\), where each cell \((i, j)\) on the grid can be in one of the following states at any time during the simulation:

- **0: Susceptible** - The cell \((i, j)\) belongs to the susceptible population \(S\).
- **1: Infected** - The cell \((i, j)\) belongs to the infected population \(I\).
- **2: Recovered** - The cell \((i, j)\) belongs to the recovered population \(R\).

Additionally, we will use a temporal grid \([0, T]\), where \(T \in \mathbb{N}\) is a parameter that marks the end time of the simulation.

## Parameters

Your function for the simulation should accept the following parameters:

- `M`, `N`: Size of the grid to be used.
- `T`: Temporal limit for the simulation.
- `I0`: Initial number of infected cells.
- `rad`: Interaction radius (neighborhood radius to consider interactions).
- `β`: Infection probability parameter, \(0 \leq \beta \leq 1\).
- `γ`: Recovery probability parameter, \(0 \leq \gamma \leq 1\).

## Simulation Process

At the start of the simulation, there will be `I0` infected cells (state 1), which should be randomly placed within the grid. The rest of the cells will start in the susceptible state (state 0). The simulation will evolve based on the interaction parameters and the differential equations governing the SIR model.

This setup allows us to observe the spread of infection, recovery rates, and the dynamics of the susceptible, infected, and recovered populations over time within the defined grid space.

## Goals

The primary goal of this simulation is to visualize the spread of an infectious disease in a population modeled by a cellular automaton. By adjusting parameters such as grid size, initial infections, interaction radius, infection probability, and recovery probability, we can explore various scenarios and their impact on disease dynamics.

## Instructions

1. Set up your grid with the desired parameters.
2. Initialize the infected cells randomly within the grid.
3. Run the simulation for the given time limit \(T\).
4. Analyze the results and observe the changes in the population states over time.

Feel free to adjust the parameters and experiment with different settings to better understand the behavior of the SIR model in a spatial context.

## Video

[Video](inciso_3.mp4)
