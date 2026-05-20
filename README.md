# Awesome Haskell Course Projects

A curated list of project ideas for a Haskell course. All projects are accesible to undergrads and can be expanded to more involved projects as well. Projects span cryptography, algorithms, numerical methods, compilers, finance, and more.

---

## Contents

- [Numerical & Real Arithmetic](#numerical--real-arithmetic)
- [Cryptography & Security](#cryptography--security)
- [Data Structures](#data-structures)
- [Algorithms](#algorithms)
- [Compression & Encoding](#compression--encoding)
- [Language & Parsing](#language--parsing)
- [Machine Learning & Statistics](#machine-learning--statistics)
- [Simulation & Graphics](#simulation--graphics)
- [Mathematics & Linear Algebra](#mathematics--linear-algebra)
- [Finance](#finance)
- [Puzzles & Games](#puzzles--games)
- [Utilities & Tools](#utilities--tools)

---

## Numerical & Real Arithmetic

- **Real Number Calculator** — Implement a calculator that handles real numbers decently, fast, and accurately. Can range from basic real arithmetic to a full recreation of the Android calculator app. Based on [*Towards an API for the Real Numbers* — Hans Boehm](https://dl.acm.org/doi/10.1145/1133956.1133960).

- **Unsure Calculator (Uncertainty Arithmetic)** — A calculator that propagates uncertainty through computations, operating on intervals or probability distributions rather than point values.
  - [Unsure Calculator in 100 Lines of Haskell](https://alt-romes.github.io/posts/2025-04-25-unsure-calculator-in-100-lines-of-haskell.html)
  - [Gaussian Processes for Machine Learning (Sci et al., 2015)](https://mlg.eng.cam.ac.uk/pub/pdf/SciGhaGor15.pdf)

- **Automatic Differentiation** — Implement forward- and/or reverse-mode automatic differentiation.
  - [Automatic Differentiation Survey (arXiv)](https://arxiv.org/pdf/1804.00746)
  - [*Beautiful Differentiation* — Conal Elliott](http://conal.net/papers/beautiful-differentiation/beautiful-differentiation-slides.pdf)

- **Lazy Differential Equation Solver** — Symbolically solve and lazily evaluate ODEs.
  - [Calculus and Symbolic ODEs](https://iagoleal.com/posts/calculus-symbolic-ode/)

---

## Cryptography & Security

- **Cipher Breaker (Caesar / Monoalphabetic / Vigenère)** — Break classical ciphers. Caesar is straightforward; monoalphabetic and Vigenère require frequency analysis and careful interactive output to allow the user to guide the attack. Based on [*The Code Book* — Simon Singh](https://simonsingh.net/books/the-code-book/).

- **Hill Cipher and Breaker** — Implement the Hill cipher (matrix-based polygraphic substitution) and an attack against it.

- **Hash with Salt and Keys** — Implement a password hashing scheme using salting and key stretching.

- **Asymmetric Encryption (RSA et al.)** — Implement RSA and related asymmetric encryption schemes from scratch.

- **Digital Signing** — Implement a digital signature scheme (e.g. RSA or DSA signatures).

- **Generating Large Primes (Miller-Rabin / AKS)** — Efficiently generate cryptographically large primes using probabilistic (Miller-Rabin) or deterministic (AKS) primality tests.

- **Merkle–Hellman Knapsack Cryptosystem and the Shamir Attack** — Implement the Merkle–Hellman public-key cryptosystem and then break it using Shamir's lattice-based attack.
  - [Wikipedia: Merkle–Hellman knapsack cryptosystem](https://en.wikipedia.org/wiki/Merkle%E2%80%93Hellman_knapsack_cryptosystem)

---

## Data Structures

- **Fibonacci Heap** — Implement a Fibonacci heap with the standard heap operations and amortized complexity guarantees.

- **Treap** — Implement a treap (randomized BST combining a binary search tree and a heap).

- **Bitmask / Bloom Filter** — Implement bitmask operations and then use them to build a Bloom filter for probabilistic set membership testing.

- **Array via Tree Map** — Simulate an array in Haskell using a `Map` (tree-backed), supporting O(log n) random access.

- **Dynamic Array via Tree Map** — Extend the above with dynamic resizing, and explore optimal resize factors (analogous to amortized doubling in imperative arrays).

---

## Algorithms

- **MiniSAT Solver** — Implement a SAT solver. A naïve O(n² · 2ⁿ) approach is a starting point; the stretch goal is to approach DPLL or CDCL for meaningful speedups.

- **List Shuffling (Merge Shuffle)** — Implement an efficient, unbiased list shuffle in Haskell using a merge-based approach.

- **Hall's Marriage Theorem** — Implement an algorithm to find a perfect matching in a bipartite graph, verifying Hall's condition.

- **Genetic Algorithm for Travelling Salesman** — Apply a genetic algorithm to find approximate solutions to TSP.

- **GitHub Stats Grade & Roadmap** — Given a GitHub profile, compute its "grade" (see the [github-readme-stats ranking formula](https://github.com/anuraghazra/github-readme-stats/blob/master/src/calculateRank.js)) and use a knapsack or greedy algorithm to generate a roadmap to the next grade tier (commits, PRs, followers, repos, etc.), with distinct strategies for creators vs. maintainers.

---

## Compression & Encoding

- **Huffman Codes / QR Codes** — Implement Huffman encoding for optimal prefix-free compression; optionally extend to QR code generation.

- **Lempel-Ziv Compression** — Implement LZ77/LZ78 compression from scratch.
  - [Lempel-Ziv Explained (YouTube)](https://www.youtube.com/watch?v=XAVErTBr2Ik)

---

## Language & Parsing

- **Type Inferrer** — Implement Hindley-Milner type inference (Algorithm W or Algorithm J) for a small functional language.

- **Golf Language** — Design and implement a code golf language: minimal syntax, maximal expressiveness-per-character.

- **Esolang + Parser** — Design an esoteric programming language and write a parser and interpreter for it.

- **Infix Notation Evaluator** — Implement a correct, precedence-aware infix expression evaluator using the algorithm described in:
  - [Pratt (1973) — Top Down Operator Precedence (ACM)](https://dl.acm.org/doi/10.1145/366959.366968)

- **Pretty Printer** — Implement a pretty printer at three levels of difficulty:
  - *Easy*: basic indentation and line wrapping
  - *Medium*: layout-aware pretty printing
  - *Hard*: typeset to another language (e.g. Haskell → LaTeX)
  - Based on [*A Prettier Printer* — Philip Wadler](https://homepages.inf.ed.ac.uk/wadler/papers/prettier/prettier.pdf)

- **Mini Qiskit + Bernstein-Vazirani Algorithm** — Implement a minimal quantum circuit simulator and use it to run the Bernstein-Vazirani algorithm.
  - [Quantum Computing Intro (ivaniscoding)](https://ivaniscoding.github.io/posts/quantum1/)
  - [Bernstein-Vazirani Algorithm](https://ivaniscoding.github.io/posts/quantum6/)

---

## Machine Learning & Statistics

- **Spam Detector (Bayesian Analysis)** — Implement a Naive Bayes spam classifier similar to early approaches at Google. Based on [*A Plan for Spam* — Paul Graham](https://paulgraham.com/spam.html).

- **Authorship Testing** — Extend Bayesian analysis to attribute text to an author from a candidate set.

- **Forensic Statistics (Bayesian Search Theory)** — Given historical data on murder sites, construct F(x) = P(murderer's average distance from houses < x), derive the PDF f(x), and use Bayes' theorem to estimate the most probable home radius of an offender. This reflects real investigative techniques in Bayesian search theory.

- **Die Hard Tests** — Implement the Diehard battery of statistical tests to measure the quality of randomness of a given set of numbers.

---

## Simulation & Graphics

- **1D Cellular Automata & Pseudo-Random Generation** — Implement elementary 1D cellular automata (à la Wolfram) and explore their use as pseudo-random number generators.

- **Conway's Game of Life** — Implement Game of Life with efficient update rules.

- **2D Plane Collision Simulation** — Simulate collisions between more than two balls in 2D, with no elasticity and different masses.

- **Perlin Noise / Procedural Generation** — Implement Perlin noise and use it as a basis for procedural terrain or texture generation.
  - [Procedural Generation with Perlin Noise (YouTube)](https://www.youtube.com/watch?v=MMj3WU4gORI)

---

## Mathematics & Linear Algebra

- **Linear Algebra Library** — Implement a library supporting: row reduction (RREF), linear independence checking, and basis generation.

- **Palindrome Record Attempt** — Attempt to find or construct extremely long palindromes, following the approach described in [*Natural Language Palindromes* — Peter Norvig](https://norvig.com/palindrome.html).

- **Find Simpson: Fermat and Beal Solutions** — Search for counterexamples (or near-misses) to Fermat's Last Theorem and the Beal conjecture over bounded integer ranges.

---

## Finance

- **Financial Contracts (Composing Contracts)** — Implement a combinator library for describing and evaluating financial derivatives. Based on [*Composing Contracts: An Adventure in Financial Engineering* — Peyton Jones et al.](https://www.cs.tufts.edu/~nr/cs257/archive/simon-peyton-jones/contracts.pdf).

- **Kelly Criterion on Uncertain Data** — Apply the Kelly Criterion to bet sizing under uncertainty, incorporating concepts from ergodicity economics.

- **Pairs Trading Arbitrage** — Implement a pairs trading strategy, detecting and exploiting mean-reversion between correlated assets.
  - [Pairs Trading (arXiv)](https://arxiv.org/html/2412.12555v1)

---

## Puzzles & Games

- **Sudoku Generator** — Generate valid, uniquely-solvable Sudoku puzzles.
  - [Sudoku Generation Paper](https://zhangroup.aporc.org/images/files/Paper_3485.pdf)

- **Fast Sudoku Solver** — Implement an efficient Sudoku solver in Haskell.
  - Skeleton: [Jabenjy/Sudoku (GitHub)](https://github.com/Jabenjy/Sudoku)
  - [Fast Sudoku Solver in Haskell, Part 1 — Abhinav Sarkar](https://abhinavsarkar.net/posts/fast-sudoku-solver-in-haskell-1/)
  - [Fast Sudoku Solver in Haskell, Part 2 — Abhinav Sarkar](https://abhinavsarkar.net/posts/fast-sudoku-solver-in-haskell-2/)

- **Best Starting Wordle Words** — Find the optimal opening word(s) for Wordle by exhaustive or heuristic search.
  - [SIMD Wordle (Clayton Ramsey)](https://claytonwramsey.com/blog/simd-wordle/)

- **Pottermore Patronus Quiz Recreation** — Recreate the decision-tree quiz logic from the Pottermore Patronus quiz.
  - [Quiz Breakdown (Reddit)](https://www.reddit.com/r/harrypotter/comments/54hjcv/the_complete_pottermore_patronus_quiz_breakdown/)

---

## Utilities & Tools

- **Spell Checker** — Implement a spell checker using edit distance and a frequency-weighted dictionary. Based on [*How to Write a Spelling Corrector* — Peter Norvig](https://norvig.com/spell-correct.html).

- **Library Book Registration & Interpolation Search** — Build a book registration and lookup system using interpolation search for O(log log n) expected search time.
  - [Interpolation Search — Perl et al.](https://csaws.cs.technion.ac.il/~itai/publications/Algorithms/p550-perl.pdf)
  - [Understanding the Complexity of Interpolation Search](https://www.academia.edu/22235408/Understanding_the_complexity_of_interpolation_search)

---

## Contributing

If you have a project idea that fits this course's themes or a resource we didn't mention, feel free to open an issue or pull request. If you implement any of these, ideally in Haskell but any FP is fine, do send it our way.
