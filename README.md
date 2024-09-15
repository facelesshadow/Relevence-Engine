# Relevance Engine

This repository contains an AI implementation for calculating PageRank using two distinct methods:

1. **Random Surfer Model**
2. **Iterative PageRank Algorithm**

## Table of Contents

- [Introduction](#introduction)
- [Random Surfer Model](#random-surfer-model)
- [Iterative PageRank Algorithm](#iterative-pagerank-algorithm)
- [Examples](#examples)
- [Contributing](#contributing)


## Introduction

PageRank is an algorithm used by Google Search to rank web pages in its search results. It works by measuring the importance of a webpage based on the number and quality of links to it. The algorithm was developed by Larry Page and Sergey Brin while they were Ph.D. students at Stanford University.

This implementation provides two methods to compute PageRank:

1. **Random Surfer Model**
2. **Iterative PageRank Algorithm**

Both methods offer insights into the importance of web pages in a network and can be used to understand how information propagates through a system.

## Random Surfer Model

The Random Surfer Model is a probabilistic approach to PageRank. It assumes that a user randomly surfs the web by following links from one page to another. The basic idea is that each page has a certain probability of being visited by a random surfer, and this probability distribution is used to rank the pages.

### Key Concepts

- **Random Surfer:** A hypothetical user who follows links at random.
- **Teleportation:** Occasionally, the surfer jumps to a random page instead of following a link. This helps ensure that all pages are reachable.
- **PageRank Formula:** The PageRank of a page is calculated based on the PageRank of the pages linking to it and a teleportation factor.

### Formula

The PageRank \( PR \) of a page \( i \) can be expressed as:

\[ PR(i) = \frac{1-d}{N} + d \left( \sum_{j \in M(i)} \frac{PR(j)}{L(j)} \right) \]

Where:
- \( d \) is the damping factor (usually set to 0.85).
- \( N \) is the total number of pages.
- \( M(i) \) is the set of pages that link to page \( i \).
- \( L(j) \) is the number of outbound links on page \( j \).

## Iterative PageRank Algorithm

The Iterative PageRank Algorithm is a numerical method used to compute PageRank by iteratively updating the ranks of pages until convergence. This approach involves repeatedly applying the PageRank formula until the values stabilize.

### Key Concepts

- **Initialization:** Start with an initial guess for the PageRank values (e.g., equal values for all pages).
- **Iteration:** Update the PageRank values based on the PageRank values from the previous iteration.
- **Convergence:** The algorithm continues iterating until the PageRank values converge to a stable distribution.

### Algorithm Steps

1. **Initialize:** Set initial PageRank values for all pages.
2. **Update:** For each page, calculate its new PageRank based on the PageRank of the pages linking to it and the teleportation factor.
3. **Check Convergence:** Determine if the PageRank values have stabilized (i.e., the change between iterations is below a predefined threshold).
4. **Repeat:** Continue the update process until convergence is achieved.



## Examples

Here are a few examples of how to use the implementation:

- **Random Surfer Model Example:**

   ```bash
   python pagerank.py corpus0
   ```

- **Iterative PageRank Algorithm Example:**

   ```bash
   python pagerank.py corpus0
   ```

*(Implementation of both is coded to show the results together at each execution of pagerank.py)*

## Contributing

Contributions to improve the PageRank implementation are welcome! Please fork the repository, make your changes, and submit a pull request. For major changes, please open an issue first to discuss what you would like to change.

