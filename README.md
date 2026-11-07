**PISOCORE**: Normality Evaluation Framework <br>
*Technical Reference Series, First Edition*

**Experiment ID**: REP-003-law-large-numbers-simulation <br>
**Publication ID:** PSC-STAT-001
**Domain**: Monte Carlo Simulation <br>
**Type**: Convergence <br>

**Objective Statement**<br>
This experiment uses Monte Carlo simulation of independent observations from an Exponential distribution with rate $\lambda$ to demonstrate the <mark>Law of Large Numbers (LLN)</mark>. It examines how the sample mean approaches the population mean, $\mu=1/\lambda$, as sample size increases, and how the standard error decreases as $\sigma/\sqrt{n}=1/(\lambda\sqrt{n})$.

**Hypothesis**<br>
As the sample size $n$ increases, the sample mean will become more concentrated around the population mean $\mu$. Equivalently, for any fixed $\epsilon>0$, the probability that the sample mean differs from $\mu$ by more than $\epsilon$ will approach zero: $P(|\bar{X}_n-\mu|>\epsilon)\to 0$ as $n\to\infty$.

## Purpose
To give researchers and students a hands-on, reproducible illustration of:
- How the sample mean converges to the population mean
- How the standard error $\sigma/\sqrt{n}$ shrinks as sample size $n$ grows

This experiment is conducted using the primary distribution, Exponential Distribution,
$X \sim \exp(\lambda)$
### What is the exponential distribution?
Exponential distribution is a continuous probability distribution that models the time and space between independent events occuring at a constant avarage rate. In practicality, it is often used to measure tings like lifespan of electronic components or the waiting time between phone calls.

**Mathematical Representation:**
- The distribution is defined by a single parameter lambda, $\lambda$ which represents the rate (average number of events per unit time). 
- The parameter can alternatively be represented by,  $\beta=1/\lambda$, which represents the scale (average time between events).

    $f(x) = \lambda \exp(-\lambda x), \quad x > 0$

- **Expected value:** $E(X)=1/\lambda $
- **Variance:** $V(X)=1/(\lambda ^2)$

### Baseline Summary: Sampling Theory
This Monte Carlo simulation draws samples of different sizes over many repetitions, allowing us to explain the sampling distribution of the sample mean. The key properties are:
1. **Expected Value**: Expected value of the sample mean is the Population mean, $\mu$
2. **Variance**: Variance of the sample mean is the population variance divided by the sample size, $\sigma ^2/n$

### Law of Large Numbers
The Law of Large Numbers then explains how the variance behaves as we increase the number of observations, n in a single sample:
$P(|\bar{X}_n-\mu|>\epsilon)\to 0$ as $n\to\infty$.<br>
**Mathematically**:
 
$\lim_{n \to\infty}⁡ Var(\bar{X})$ <br>
$=\lim_{n \to\infty} \sigma ^2/n$ <br>
$=0$ <br>

This explains that as you increase the number of observations, $n$ the sample means become less variant. The sample mean ( $\bar{X}$), converges to the true population mean, $\mu$ in probability.


### Quick Start
```bash
pip install -r requirements.txt
jupyter notebook notebooks/01_lln_simulation.ipynb

```

### Reference
PISOCORE. (2026). Normality Evaluation Framework: A Technical Reference Guide for Distribution Diagnostics. Technical Reference Series, First Edition. Document ID: PSC-STAT-001.