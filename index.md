---
title: "Probability and Statistics Problems"
---

<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    tex2jax: {inlineMath: [['$','$'], ['\\(','\\)']], displayMath: [['$$','$$'], ['\\[','\\]']]}
  });
</script>
<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML">
</script>


---
### Problem 1: Conditional Probability with Poisson and Exponential Distribution

#### Word Problem
A civil engineer is monitoring traffic flow at a busy intersection. The number of vehicles passing through the intersection follows a Poisson distribution with an average rate of $\lambda = 5$ vehicles per minute. The time between consecutive vehicles passing through the intersection follows an exponential distribution. What is the probability that exactly 4 vehicles pass through the intersection in the first minute, given that no vehicle has passed in the first 10 seconds?

#### Step-by-Step Workflow
1. **Identify the known parameters:**
   - $\lambda = 5$ vehicles per minute for the Poisson distribution.
   - The time between arrivals follows an exponential distribution with rate parameter $\lambda = 5$ per minute.

2. **Calculate the probability of no vehicles passing in the first 10 seconds:**
   - Use the Exponential distribution's CDF to find the probability.

3. **Determine the probability of exactly 4 vehicles passing in the first minute:**
   - Use the Poisson distribution to calculate this probability.

4. **Use conditional probability:**
   - Apply the definition of conditional probability to combine the two probabilities.

5. **Solution:**
   - Compute the final probability.

#### Math Steps

$$
P(X = 4 \mid T > 10) = \frac{P(X = 4 \text{ and } T > 10)}{P(T > 10)}
$$

Where:
- $T$ is the time until the first vehicle arrives.
- $X$ is the number of vehicles in 1 minute.

1. **Exponential Distribution for $P(T > 10)$:**

$$
P(T > 10) = e^{-\lambda \cdot t} = e^{-5 \cdot \frac{10}{60}} = e^{-\frac{5}{6}}
$$

2. **Poisson Distribution for $P(X = 4)$:**

$$
P(X = 4) = \frac{e^{-\lambda} \lambda^4}{4!} = \frac{e^{-5} \cdot 5^4}{24}
$$

3. **Final Probability:**

$$
P(X = 4 \mid T > 10) = \frac{e^{-\frac{5}{6}} \cdot \frac{e^{-5} \cdot 5^4}{24}}{e^{-\frac{5}{6}}} = \frac{e^{-5} \cdot 625}{24}
$$

#### Solution

$$
P(X = 4 \mid T > 10) = \frac{e^{-5} \cdot 625}{24} \approx 0.1755
$$

### Problem 2: Hypothesis Testing and Confidence Interval

#### Word Problem
A construction company claims that the average compressive strength of concrete used in their projects is at least 5000 psi. A sample of 30 concrete specimens is tested, yielding a sample mean of 4900 psi and a standard deviation of 200 psi. Test the company’s claim at a 5% significance level and construct a 95% confidence interval for the true mean compressive strength.

#### Step-by-Step Workflow
1. **State the null and alternative hypotheses:**
   - $H_0: \mu \geq 5000$ psi
   - $H_A: \mu < 5000$ psi

2. **Choose the significance level:**
   - $\alpha = 0.05$

3. **Calculate the test statistic:**
   - Use the t-distribution formula.

4. **Determine the critical value:**
   - Use a t-table or calculator to find the critical value for $\alpha = 0.05$ and $n-1$ degrees of freedom.

5. **Compare the test statistic to the critical value:**
   - Decide whether to reject or fail to reject $H_0$.

6. **Construct the 95% confidence interval:**
   - Use the sample mean, standard deviation, and t-distribution to calculate the interval.

7. **Solution:**
   - Present the conclusion of the hypothesis test and the confidence interval.

#### Math Steps

$$
t = \frac{\bar{x} - \mu_0}{\frac{s}{\sqrt{n}}} = \frac{4900 - 5000}{\frac{200}{\sqrt{30}}}
$$

$$
t = \frac{-100}{\frac{200}{\sqrt{30}}} = \frac{-100}{36.51} \approx -2.74
$$

- Critical value $t_{\alpha, n-1} = t_{0.05, 29} \approx -1.699$
- Since $t < t_{\alpha, n-1}$, reject $H_0$.

**Confidence Interval:**

$$
\bar{x} \pm t_{\alpha/2, n-1} \cdot \frac{s}{\sqrt{n}} = 4900 \pm 2.045 \cdot \frac{200}{\sqrt{30}}
$$

$$
CI = 4900 \pm 74.5
$$

$$
CI = [4825.5, 4974.5] \text{ psi}
$$

#### Solution
- The null hypothesis is rejected, indicating that the true mean compressive strength is likely less than 5000 psi.
- The 95% confidence interval for the true mean compressive strength is $[4825.5, 4974.5]$ psi.

### Problem 3: CDF and PMF

#### Word Problem
A geotechnical engineer is analyzing soil sample data to determine the probability distribution of particle sizes in a specific region. The particle sizes (in millimeters) are modeled as a discrete random variable $X$ with the following probability mass function (PMF):

$$
P(X = x) = \begin{cases} 
0.2 & \text{if } x = 1 \\
0.3 & \text{if } x = 2 \\
0.4 & \text{if } x = 3 \\
0.1 & \text{if } x = 4 
\end{cases}
$$

Determine the cumulative distribution function (CDF) $F(x)$, and calculate the probability that the particle size is less than or equal to 3 mm.

#### Step-by-Step Workflow
1. **Define the PMF for $X$:**
   - Assign the probabilities to each particle size value.

2. **Calculate the CDF $F(x)$:**
   - Sum the PMF values for all $x \leq X$.

3. **Evaluate the CDF at $X = 3$:**
   - Calculate $F(3)$ to determine the probability that $X \leq 3$.

4. **Solution:**
   - Present the CDF and the probability that $X \leq 3$.

#### Math Steps

1. **PMF:**

$$
P(X = 1) = 0.2, \quad P(X = 2) = 0.3, \quad P(X = 3) = 0.4, \quad P(X = 4) = 0.1
$$

2. **CDF:**

$$
F(x) = P(X \leq x)
$$

$$
F(1) = P(X = 1) = 0.2
$$

$$
F(2) = P(X \leq 2) = P(X = 1) + P(X = 2) = 0.2 + 0.3 = 0.5
$$

$$
F(3) = P(X \leq 3) = P(X = 1) + P(X = 2) + P(X = 3) = 0.2 + 0.3 + 0.4 = 0.9
$$

$$
F(4) = P(X \leq 4) = P(X = 1) + P(X = 2) + P(X = 3) + P(X = 4) = 0.2 + 0.3 + 0.4 + 0.1 = 1.0
$$

3. **Probability that $X \leq 3$:**

$$
P(X \leq 3) = F(3) = 0.9
$$

#### Solution
- The CDF $F(x)$ is:

$$
F(x) = \begin{cases} 
0 & \text{if } x < 1 \\
0.2 & \text{if } x = 1 \\
0.5 & \text{if } x = 2 \\
0.9 & \text{if } x = 3 \\
1.0 & \text{if } x \geq 4 
\end{cases}
$$

- The probability that the particle size is less than or equal to 3 mm is $P(X \leq 3) = 0.9$.

