# Hi, I'm Mahshid 👋

C++ and Python engineer with a PhD background in large-scale scientific computing, now moving into applied AI and deep learning. My PhD was about turbulence, diffusion, and dispersion, and the mathematics behind it turned out to map directly onto quantitative finance: mean drift plus random noise, the same structure underneath Black-Scholes. I made that connection while studying for my MSc in Financial Engineering — and the same discipline (build from first principles, test rigorously, trust nothing until it's validated) is what I'm now bringing to C++/PyTorch and AI framework work.

**My approach to any model:** build it from first principles, calibrate it against real data, stress-test its assumptions, and validate it independently before trusting its output. That's the discipline my PhD trained into me, and it's what I bring to the projects below — spanning simple to advanced in both languages.

### 🔍 Featured projects

#### C++

**[pytorch-parametric-swish](https://github.com/MahshidGolzar/pytorch-parametric-swish)** — advanced
A custom PyTorch C++ operator (learnable-β Swish activation), hand-derived forward and backward, registered via `TORCH_LIBRARY` and built with CMake. Mutation-tested: deliberately broke the backward pass, confirmed `gradcheck` caught it, then fixed it. The commit history shows the real 3-commit cycle, not a reconstruction after the fact.

**[quant_validator](https://github.com/MahshidGolzar/quant_validator)** — medium
A from-scratch int8 quantization validator — the float32-to-int8 conversion AI framework code uses to target hardware accelerators — with a hand-written test suite, also mutation-tested: removed the range clamp, confirmed two tests caught the resulting out-of-range value (20.0 silently wrapped to -56), restored it. The real commit history shows the mutant, then the one-line fix.

**[mini_tensor](https://github.com/MahshidGolzar/mini_tensor)** — simple
A small, dependency-free 2D matrix ("tensor") class: a flat buffer plus a shape, with elementwise ops and real matrix multiplication. Built to understand what a `Tensor` actually is underneath a framework like PyTorch, before extending one.

#### Python

**[black_scholes_pde_greeks](https://github.com/MahshidGolzar/black_scholes_pde_greeks)** — advanced
A European option pricer built two independent ways, closed-form analytical and numerical PDE, specifically to cross-validate each other. Implements all five Greeks and three finite-difference schemes (explicit, implicit, Crank-Nicolson), and includes a test that deliberately proves the explicit scheme is unstable on a naive grid, an intentional validation finding, not a bug.

**[risk_engine_monte_carlo](https://github.com/MahshidGolzar/risk_engine_monte_carlo)** — advanced
A modular Python risk engine implementing Historical, Parametric, and Monte Carlo VaR alongside Expected Shortfall, validated through Kupiec and Christoffersen backtesting.

**[simple_historical_var](https://github.com/MahshidGolzar/simple_historical_var)** — simple
A single-method, single-asset historical VaR calculation, deliberately stripped down to something explainable on a whiteboard — the simple counterpart to the risk engine above.

### 🎓 Background

- PhD in Civil Engineering (Computational Fluid Dynamics), University of Sheffield, six peer-reviewed publications
- MSc in Financial Engineering, WorldQuant University, graduated with an 85% average
- Seven years teaching Python, data science, and engineering

### 📫 Find me

[LinkedIn](https://www.linkedin.com/in/dr-mahshid-golzar) · mahshidgolzar@gmail.com
