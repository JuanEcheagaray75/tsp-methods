# Traveling Salesman Problem

- [Traveling Salesman Problem](#traveling-salesman-problem)
  - [Mathematical Modelling](#mathematical-modelling)
  - [Solving the TSP](#solving-the-tsp)
    - [Exact solution through Or-Tools](#exact-solution-through-or-tools)
    - [Genetic Algorithm](#genetic-algorithm)
    - [Ant Colony Optimization](#ant-colony-optimization)
  - [Results](#results)
  - [Installation and usage](#installation-and-usage)
  - [Credits](#credits)
  - [License](#license)

## Mathematical Modelling

Given the sets and parameters:
$$\begin{gather*}
    I = \{1, 2, \dots, n\} \\
    J = \{1, 2, \dots, n\} \\
    c_{ij} := \text{cost of going from city } i \text{ to city } j \\
    c_{ij} \geq 0 \qquad \forall i \in I, \forall j \in J\\
\end{gather*}$$

Given the variables:
$$\begin{equation*}
    x_{ij} = \begin{cases}
        1 & \text{if the salesman goes from city } i \text{ to city } j \\
        0 & \text{otherwise}
    \end{cases}
\end{equation*}$$

Then:
$$\begin{equation*}
	\begin{aligned}
		\min \quad & \sum_{i \in I} \sum_{j \in J \setminus \{j=i\}} c_{ij} x_{ij}\\
		\text{st: }\quad &
		\begin{array}{c}
			\sum\limits_{i \in I \setminus \{j=i\}} x_{ij} = 1 \qquad \forall j \in J \\[10pt]
            \sum\limits_{j \in J \setminus \{j=i\}} x_{ij} = 1 \qquad \forall i \in I \\[10pt]
            \sum\limits_{i \in Q} \sum\limits_{j \in Q, j \neq i} x_{ij} \leq |Q| - 1 \qquad \forall Q \not\subseteq \{1, 2, \dots, n\}, |Q| \geq 2 \\
            x_{ij} \in \mathbb{B} \\
		\end{array}
	\end{aligned}
\end{equation*}$$

## Solving the TSP

### Exact solution through Or-Tools

### Genetic Algorithm

### Ant Colony Optimization

## Results

## Installation and usage

## Credits

## License
