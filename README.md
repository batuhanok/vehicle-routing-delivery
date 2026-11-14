# Heuristic and Optimal Routing for a Delivery Company

Solving a delivery company's daily route as an asymmetric travelling salesman problem, first with heuristics and then exactly with Gurobi.

## Overview

A company serves 30 customers from one depot every day and wants the cheapest route. The distance matrix is asymmetric, so the same pair of locations can cost differently in each direction. We built a route with heuristics, improved it, and compared it with the true optimum.

## What I did

- Modeled the daily delivery route for a depot and 30 customers as an asymmetric travelling salesman problem in Python, building a tour with an insertion heuristic and improving it with 2-exchange and greedy 2-opt heuristics
- Solved the exact model in Gurobi with MTZ subtour elimination constraints to find the optimal tour, and showed that applying 2-opt right after insertion came within 1.4% of the optimum

## Methods and tools

Python, Gurobi, travelling salesman problem, insertion heuristic, 2-exchange, 2-opt, MTZ subtour elimination.

## Files

| File | Description |
|---|---|
| [code/delivery_routing_tsp.ipynb](code/delivery_routing_tsp.ipynb) | Notebook with the heuristics and the exact model |
| [docs/report.pdf](docs/report.pdf) | Printed notebook with the code, outputs and explanations |

The notebook reads the company's distance matrix from an Excel file that is not included here. Running the exact model also needs a Gurobi license.

## Team

Ogün Can Koç, Batuhan Ok, Doğa Güz, Melek Melisa Akay

ISE 316 Computer Applications for Industrial Engineers, Yeditepe University, Spring 2024. Dr. Sina Rastani.
