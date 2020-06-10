# APS1070_Anomaly_Detection
Anomaly Detection using Gaussian Mixture Models

### Anomaly Detection Algorithm
Given that there are $m$ training examples and $n$ features 
1. Choose features that you think might be indicative of anomalous examples. 
2. Fit Parameters $\mu_1, \mu_2 ..., \mu_n$ as well as $\sigma_1^2, \sigma_2^2, ...\sigma_n^2$

<a href="https://www.codecogs.com/eqnedit.php?latex=\mu_j&space;=&space;\frac{1}{m}&space;\sum_{i=1}^{m}x_j^{(i)}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\mu_j&space;=&space;\frac{1}{m}&space;\sum_{i=1}^{m}x_j^{(i)}" title="\mu_j = \frac{1}{m} \sum_{i=1}^{m}x_j^{(i)}" /></a>

$$
\mu_j = \frac{1}{m} \sum_{i=1}^{m}x_j^{(i)}
$$

where $\mu_j$ is the average value of the $j$th feature. 

<a href="https://www.codecogs.com/eqnedit.php?latex=$$&space;\sigma_j^2&space;=&space;\frac{1}{m}&space;\sum_{i=1}^{m}(X_{j}^{(i)}&space;-&space;\mu_j)^2&space;$$" target="_blank"><img src="https://latex.codecogs.com/gif.latex?$$&space;\sigma_j^2&space;=&space;\frac{1}{m}&space;\sum_{i=1}^{m}(X_{j}^{(i)}&space;-&space;\mu_j)^2&space;$$" title="$$ \sigma_j^2 = \frac{1}{m} \sum_{i=1}^{m}(X_{j}^{(i)} - \mu_j)^2 $$" /></a>

3. Given new example $x$, compute $p(x)$: 

$$
p(x) = \prod_{j=1}^n p(x_j\; \mu_j, \sigma_j^2)=\prod_{j=1}^n \frac{1}{\sqrt{2\pi\sigma_j} }exp \left( \frac{-(x_j-\mu_j)^2}{2\sigma_j^2}\right)
$$

