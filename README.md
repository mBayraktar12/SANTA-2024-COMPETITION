# Kaggle Competition: Minimizing Perplexity with Simulated Annealing

## Overview

This repository contains my approach to a Kaggle competition where the goal was to minimize the perplexity of given sentences by shuffling words. The perplexity score was measured using the **Gemma-2-9B** model.

## Approach

Initially, I explored **brute force methods** for simple cases but transitioned to **simulated annealing** for more complex cases, leveraging heuristic-based optimizations. The computing power and GPU precision were crucial in achieving competitive results.

## Key Methods

### 1. Brute Force (for small cases)

- The first sentence consisted of **only 10 words**, allowing for an exhaustive search.

### 2. Simulated Annealing (for complex cases)

- Used to optimize word order to minimize perplexity.
- Applied different **heuristic techniques**:
  - **Swaps**: Swapping adjacent or random words.
  - **Shifts**: Moving a random subset left or right.
  - **Reversals**: Reversing a subsection of words.
  - **Partial Permutations**: Reordering small subsets of words.
  - **Stopword Sensitivity**: Noticing responsiveness to stopword placements.
  - **Alphabetical Sensitivity**: Adjusting orders for better perplexity reduction.

### 3. Experimentation with Parameters

- Tested **different starting temperatures** to balance exploration and exploitation.
- Used **varied starting points** for optimization to prevent local minima.
- Adjusted **samples per each temperature** to refine the search process.
- Implemented **multiple cooling schedules**, including exponential and logarithmic decay, to fine-tune annealing efficiency.

### 4. Lower Temperature Mode

- Used a **low-temperature mode** to exploit local refinements after major improvements.
- Stored promising solutions and revisited them for final adjustments in a controlled manner.

### 5. Sentence-Specific Observations

- **Sentences 2, 3, 4, and 5**: Required careful **simulated annealing** with a variety of heuristic moves.
- **Sentence 6**: Showed sensitivity to **stopword positioning** and **alphabetical order**, leading to unexpected perplexity changes.

## Challenges

- **Computational Efficiency**: Handling multiple simulated annealing runs efficiently required strong GPU support.
- **Precision Issues**: GPU variations in floating-point precision affected results.
- **Perplexity Calculation Nuances**: Some sentences had unexpected sensitivity to stopword reordering.

## Results

- Achieved a significant reduction in perplexity scores using simulated annealing.
- Leveraged heuristic methods for better sentence structuring.
- Improved optimization by fine-tuning cooling schedules and search techniques.

## Conclusion

Competing with the **top data scientists worldwide**, including **NVIDIA’s team**, was an exciting challenge. The competition was a great opportunity to apply **heuristic optimization techniques** and learn from the best in the field.
