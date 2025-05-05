# N-Puzzle Solver with Uninformed Search Algorithms

This repository contains implementations of various uninformed search algorithms to solve the classic 8-puzzle and 15-puzzle problems. The implementation is in Python and includes a comprehensive benchmarking framework to compare algorithm performance.

## Overview

The N-puzzle is a sliding puzzle that consists of a frame of numbered square tiles in random order with one tile missing. The puzzle exists in various sizes, with the 8-puzzle (3×3 grid) and 15-puzzle (4×4 grid) being the most common variants. The goal is to rearrange the tiles to reach a specific goal configuration by sliding tiles into the empty space.

## Features

- Implementations of 6 different uninformed search algorithms:
  - Breadth-First Search (BFS)
  - Depth-First Search (DFS)
  - Uniform-Cost Search
  - Depth-Limited Search
  - Iterative Deepening Search
  - Bidirectional Search
- Dataset generation for both 8-puzzle and 15-puzzle with solvability checking
- Performance evaluation metrics:
  - Number of nodes explored
  - Execution time
  - Memory usage
  - Solution length
- Visualization tools for puzzles and solutions
- Comprehensive benchmarking and statistical analysis

## Requirements

- Python 3.6+
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook

## Installation

1. Clone this repository:
```
git clone https://github.com/NguyenTheAnk/BTL_AI.git
```

Install the required packages:
```
pip install numpy pandas matplotlib seaborn jupyter
```

## Usage

### Running the Jupyter Notebook

1. Start Jupyter Notebook:
```
jupyter notebook
```

2. Open the `main.ipynb` file in your browser.

3. You can run all cells to execute the complete experiment, or run individual cells to test specific algorithms or functionality.

### Dataset Generation

The notebook will automatically generate datasets of different sizes (10, 100, 1000, 10000) for both 8-puzzle and 15-puzzle problems. These datasets are stored in `data8puzzle/` and `data15puzzle/` directories respectively.

### Running Experiments

The main function `comprehensive_main()` will:

1. Run all 6 uninformed search algorithms on various dataset sizes
2. Collect performance metrics for each algorithm
3. Generate visualizations and comparisons
4. Save results in the `results/` and `figures/` directories

### Customizing Experiments

You can modify the following parameters in the `comprehensive_main()` function:

- `dataset_sizes`: List of dataset sizes to test
- `max_puzzles`: Number of puzzles to test for each dataset size
- `time_limit`: Maximum execution time for each algorithm

## File Structure

- `main.ipynb`: Main Jupyter notebook containing all code
- `data8puzzle/`: Generated 8-puzzle datasets
- `data15puzzle/`: Generated 15-puzzle datasets
- `results/`: CSV files containing performance results
- `figures/`: Generated visualizations and comparisons

## Results

The experiments generate several result files:

- Individual CSV files for each algorithm, puzzle type, and dataset size
- Combined CSV files for overall comparison
- Visualizations of performance metrics
- Difficulty analysis of puzzle instances

## Algorithm Performance

In general, for the 8-puzzle problem:
- Bidirectional Search is typically the fastest and most efficient algorithm
- Iterative Deepening Search provides optimal solutions but explores more nodes
- BFS guarantees optimal solutions but has higher memory usage
- DFS is memory-efficient but doesn't guarantee optimal solutions

For the 15-puzzle problem:
- Most uninformed search algorithms struggle due to the much larger search space
- Depth-Limited Search with a small limit is the only algorithm that consistently terminates
- Memory requirements grow exponentially compared to 8-puzzle

## Visualizations

The code also includes visualization tools for:
- Puzzle states
- Solution paths
- Performance comparisons between algorithms
- Difficulty analysis of puzzles

## Notes

- The 15-puzzle is significantly more complex than the 8-puzzle, with a state space size of 16!/2 ≈ 10^13 compared to 9!/2 = 181,440 for the 8-puzzle.
- Uninformed search algorithms are generally insufficient for solving complex 15-puzzle instances; informed search algorithms (A*, IDA*) with good heuristics are recommended for larger puzzles.
- Timeout parameters are set to limit execution time, as some algorithms can run for a very long time on complex puzzles.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- This implementation is based on classical search algorithms from artificial intelligence.
- The puzzle generation ensures that all generated puzzles are solvable.