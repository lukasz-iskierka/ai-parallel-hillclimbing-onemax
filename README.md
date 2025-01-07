## Parallel Hill Climbing for OneMax Problem

### Project Description

This project implements a population-based variant of the Hill Climbing algorithm to solve the OneMax optimisation problem. It includes comprehensive performance analysis and visualisation of the algorithm's behaviour across different problem sizes and population parameters.

### Problem Statement

The OneMax problem is a useful baseline to test the performance of algorithms in the AI field of Search and Optimisation. In practice, by finding a solution with ones only, e.g. "1111111111" for a 10 bit problem, we know that an algorithm has found an optimal solution. While simple in concept, it provides valuable insights into algorithm performance and scalability.

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
* Processing speed data
* Statistical analysis over multiple runs

### Results & Key Findings

* Optimal performance for small problem sizes (10-40 bits)
* Gradual performance degradation observed beyond 40-bit strings
* Limited impact of population size on solution quality
* Average fitness score of ~90% for 100-bit problems
* Increasing convergence time for larger problem sizes suggesting scalibility issues

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
    generations=100,
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
* Adaptive mutation

2. Explore hybrid approaches combining hill climbing with:

* Genetic algorithms
* Simulated annealing

3. Implement more sophisticated/alternative mutation operators

### Contributing

Contributions are welcome! Please read contributing guidelines before making a pull request.

### License

This project is licensed under the MIT License.
