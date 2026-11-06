**PISOCORE**: Normality Evaluation Framework <br>
*Technical Reference Series, First Edition*

**Experiment ID**: REP-003-law-large-numbers-simulation <br>
**Domain**: Monte Carlo Simulation <br>
**Type**: Convergence <br>

**Objective Statement**<br>
This experiment uses Monte Carlo simulation of independent observations from an Exponential distribution with rate $\lambda$ to demonstrate the <mark>Law of Large Numbers (LLN)</mark>. It examines how the sample mean approaches the population mean, $\mu=1/\lambda$, as sample size increases, and how the standard error decreases as $\sigma/\sqrt{n}=1/(\lambda\sqrt{n})$.

**Hypothesis**<br>
As the sample size $n$ increases, the sample mean will become more concentrated around the population mean $\mu$. Equivalently, for any fixed $\epsilon>0$, the probability that the sample mean differs from $\mu$ by more than $\epsilon$ will approach zero: $P(|\bar{X}_n-\mu|>\epsilon)\to 0$ as $n\to\infty$.

## Purpose
To give researchers and students a hands-on, reproducible illustration of:
- How the sample mean converges to the population mean
- How the standard error $\sigma/\sqrt{n}$ shrinks as sample size,$n$,  grows

This experiment is conducted using simulated data that follows an Exponential Distribution,<br>
$X \sim \exp(\lambda)$
### What is the exponential distribution?
Exponential distribution is a continuous probability distribution that models the time and space between independent events occuring at a constant avarage rate. In practicality, it is often used to measure tings like lifespan of electronic components or the waiting time between phone calls.

**Mathematical Representation:**
- The distribution is defined by a single parameter, λ (lambda), which represents the rate (average number of events per unit time) 
- The parameter can alternatively be represented by, β=1/λ , which represents the scale (average time between events).

            f(x)=λe^(-λx), x>0

- **Expected value:** E(X)=1/λ
- **Variance:** V(X)=1/(λ^2)

### Baseline Summary: Sampling Theory
The Sampling Theory allows us to explain the distribution of the sample mean using two key properties:
1. **Expected Value**: Expected value of the sample mean = Population mean, μ.
2. **Variance**: Variance of the sample mean = Square of the population standard deviation divided by the sample size (σ^2/n)

### Law of Large Numbers
The Law of Large Numbers then explains how the variance behaves as we increase the number of observations, n in a single sample:

**Mathematically**:

            (lim)(n→∞)⁡Var(X ̅ )
            =(lim)(n→∞)⁡σ^2/n
            =0

This explains to us that as you increase the number of observations, n, the sample means become less variant. The sample mean ( X ̅ ), converges to the true population mean, μ in probability.


### Quick Start
```bash
pip install -r requirements.txt
jupyter notebook notebooks/01_lln_simulation.ipynb

```

### Reference
PISOCORE. (2026). Normality Evaluation Framework: A Technical Reference Guide for Distribution Diagnostics. Technical Reference Series, First Edition. Document ID: PSC-STAT-001.