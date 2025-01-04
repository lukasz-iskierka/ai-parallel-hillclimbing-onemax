## Parallel Hill Climbing for OneMax Problem

### Project Description

This project implements a population-based variant of the Hill Climbing algorithm to solve the OneMax optimisation problem. It includes comprehensive performance analysis and visualisation of the algorithm's behavior across different problem sizes and population parameters.

### Problem Statement & Objectives

The OneMax problem is a benchmark in optimisation, requiring an algorithm to find a bitstring containing only ones (e.g., "111111"). While simple in concept, it provides valuable insights into algorithm performance and scalability.

### Objectives:

* Implement a parallel hill climbing algorithm to solve OneMax
* Analyze algorithm performance across different bitstring lengths (10-100 bits)
* Investigate the impact of population size on solution quality
* Evaluate convergence patterns and computational efficiency

### Methodology

The algorithm's implementation uses:

* Population-based parallel search with multiple solution candidates
* Bitflip mutation with configurable probability
* Fitness evaluation based on number of ones in bitstring
* Performance tracking across generations
* Statistical analysis over multiple runs

### Results & Key Findings

* Optimal performance for small problem sizes (10-30 bits)
* Performance degradation observed beyond 30-bit strings
* Limited impact of population size on solution quality
* Average fitness score of ~80% for 100-bit problems
* Increasing convergence time for larger problem sizes

### Installation

```bash
# Clone the repository
git clone https://github.com/lukasz-iskierka/ai-parallel-hillclimbing-onemax.git

# Install required packages
pip install numpy
pip install seaborn
pip install matplotlib
```

### Usage

```python
# Example: Run algorithm with custom parameters
solution, fitness, generation = parallel_hill_climbing(
    generations=100,
    L=50,  # bitstring length
    population=10,
    p=0.05  # mutation probability
)

# Run performance tests
avg_fitness_scores, avg_convergence = test_parallel_hill_climber(
    population_size=10,
    runs=10
)
```

### Technologies Used

* Python 3.x
* NumPy (numerical operations)
* Seaborn & Matplotlib (visualisation)
* Random (stochastic operations)

### Future Improvements

1. Implement adaptive mutation rates based on:

* Population diversity
* Generation number
* Fitness progression

2. Explore hybrid approaches combining hill climbing with:

* Genetic algorithms
* Simulated annealing

3. Optimise performance for larger problem sizes
4. Add parallelisation for performance testing
5. Implement more sophisticated/alternative mutation operators

### Contributing

Contributions are welcome! Please read contributing guidelines before making a pull request.

### License

This project is licensed under the MIT License.