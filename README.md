# Hi, I'm Mahshid 👋

Developer with a PhD background in large-scale scientific computing (CFD/HPC), moving into applied AI and C++/PyTorch framework work. Five years writing and debugging numerical C++, Fortran, and Python on university HPC Linux clusters during a PhD in Computational Fluid Dynamics, producing six peer-reviewed publications. Alongside seven years of technical teaching (ongoing since 2019), retrained in applied AI through a WorldQuant University MSc (2023–2025). The discipline is the same wherever I apply it: build from first principles, test rigorously, trust nothing until it's validated. That's what the projects below are for.

**My approach to any model:** build it from first principles, calibrate it against real data, stress-test its assumptions, and validate it independently before trusting its output. That's the discipline my PhD trained into me, and it's what I bring to the projects below.

### 🔍 Featured projects

#### C++

**[pytorch-parametric-swish](https://github.com/MahshidGolzar/pytorch-parametric-swish)**

A custom PyTorch C++ operator (learnable-β Swish activation), hand-derived forward and backward, registered via `TORCH_LIBRARY` and built with CMake. The first commit's backward pass had a one-line bug in it from the start; the `gradcheck`-based test suite added in the next commit failed against it immediately; a third commit fixed it.

**[quant_validator](https://github.com/MahshidGolzar/quant_validator)**

A from-scratch int8 quantization validator — the float32-to-int8 conversion AI framework code uses to target hardware accelerators — with a Catch2 test suite and GitHub Actions CI (build, plus ASan/UBSan and Clang implicit-conversion sanitizer builds as a general safety net). The first commit's missing range clamp was caught by its own test suite (20.0 at scale 0.1 silently wrapped to -56); I checked whether the sanitizers would also have caught it and documented the honest answer in the README (they don't — it's a logic bug, not a rule violation).

**[mini_tensor](https://github.com/MahshidGolzar/mini_tensor)**

A small, dependency-free 2D matrix ("tensor") class: a flat buffer plus a shape, with elementwise ops and real matrix multiplication. Built to understand what a `Tensor` actually is underneath a framework like PyTorch, before extending one.

#### Python

**[black_scholes_pde_greeks](https://github.com/MahshidGolzar/black_scholes_pde_greeks)**

A European option pricer built two independent ways, closed-form analytical and numerical PDE, specifically to cross-validate each other. Implements all five Greeks and three finite-difference schemes (explicit, implicit, Crank-Nicolson), and includes a test that deliberately proves the explicit scheme is unstable on a naive grid, an intentional validation finding, not a bug.

**[risk_engine_monte_carlo](https://github.com/MahshidGolzar/risk_engine_monte_carlo)**

A modular Python risk engine implementing Historical, Parametric, and Monte Carlo VaR alongside Expected Shortfall, validated through Kupiec and Christoffersen backtesting.

**[simple_historical_var](https://github.com/MahshidGolzar/simple_historical_var)**

A single-method, single-asset historical VaR calculation, deliberately stripped down to something explainable on a whiteboard — the simple counterpart to the risk engine above.

### 🎓 Background

- PhD in Civil Engineering (Computational Fluid Dynamics), University of Sheffield, six peer-reviewed publications
- MSc in Financial Engineering, WorldQuant University, graduated with an 85% average
- Seven years teaching Python, data science, and engineering

### 📫 Find me

[LinkedIn](https://www.linkedin.com/in/dr-mahshid-golzar) · mahshidgolzar@gmail.com
