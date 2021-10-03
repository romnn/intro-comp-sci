## Introduction to Computational Science

#### Usage

```bash
pipenv install --dev
pipenv shell
jupyter-lab
```

#### Basic definitions

What is a model?
  - a Model (M) for a system (S) and an experiment (E) is anything to which E can be applied in order to answer a question about S (Marvin Minski)
  - in this course the focus is only on models that can be expressed as computer programs
  - model's usefulness should be determined by model validation

What is a Simulation?
 - Simulation is an experiment performed on a mathematical model

Types of models:
  - (the actual system is not a model but could be used of course)
  - mathematical model
    - there might exist an analytical solution, otherwise simulation must be used
  - physical model

Types of mathematical models:
  - Continuous time models (state changes continually over time)
    - state changes are usually represented by sets of differential equations
  - Discrete time models (state changes continually but time axis is discretized)
    - states changes are usually represented by difference equations
  - Discrete event models (like discrete time models, but the intervals between time steps does not have to be constant)

Types of simulations:
  - Time-Driven Simulations
    - the time advances in fixed intervals of delta t
    - most often used for natural systems (continuous time models)
    - not ideal for discrete time models because delta t has to be small enough to capture every event in the discrete system
      - delta t could have to be infinitely small
  - Event-Driven Simulations
    - the time advances whenever a new event occurs to account for the occurrence for that event
    - trade efficiency for precision

What are differential equations?
  - Equations that describe changes rather than absolute values
  - Often used when describing the change of values is easier than the formulation of a function that describes the absolute values
  - Why do we need initial conditions?
    - Well, when we have a derivative and try to solve for a function that has this derivative, there can be multiple solutions
    - because of the constant term C
  - usually a form of y' = f(x, y)
  - g1(x) is a solution of y' = f(x,y)
    - <=> graph of g1(x) is an integral curve in the direction field associated with y' = f(x,y)
    - y'(x) = f(x, g1(x))

Types of differential equations:
  - Orinary Differential Equations (ODE)
    - single independent variabele
  - Partial Differential Equations (PDE)
    - multiple variables, e.g. the tempterature at each point in space

Types of solvers:
  - solvers take a conceptual model (e.g. mathematical model) and map it to a virtual machine model to find solutions
  - Numerical Solvers
  - Direct Solvers
  - Natural Solvers

#### Introduction on diseases
- Epidemic
  - affecting many persons at the same time, and spreading from person to person in a locality where the disease is not permanently prevalent
- Pandemic
  - epidemic that has spread over a large area, that is, it’s “prevalent throughout an entire country, continent, or the whole world
- Endemic
  - disease that is prevalent in or restricted to a particular location, region, or population
