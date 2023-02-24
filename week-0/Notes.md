1st meet: In science we make model to predict future evolution of something.
All models are wrong but some are useful than others.

every Distribution is a model.

N ~(about) something 

N=Number o trial
P(x)=probability of an event x

for Discrete random variable->>

Binomial distribution: "summarizes the likelihood that a value will take one of two independent values "

PMF= N!/(K!(N-K)!) (P(success)**K * (1-P(success))**(N-K))
The formula can be understood as follows: K successes occur with probability p**k and N-K failures occur with probability (1-p)**(N-K)
 However, the k successes can occur anywhere among the n trials, and there are Combination(N / K) different ways of distributing k successes in a sequence of n trials

Asumptions: Each trial has only one outcome, Every outcome is indepedent(mutually exclusive),and probability of success doesn't change.
Average of an even = N*p(x)
std = sqrt(N*p(x)(1-p(x)))

Poissonian distri: Same as binomial except:: ""Probability->0, Trial->inf""
Avg=N*P(x)
std=sqrt(N*P(x))

Assignment:

```
import numpy as np

p_H = 0.5
p_T = 0.5
N = 200

head_50 = []

for j in range(50):
    heads = 0
    for i in range(N):
        x = np.random.rand(1)
        if x<= p_H:
            heads = heads + 1
    head_50.append(heads)

#Experiment
mean = np.mean(head_50)
std = np.std(head_50)
print("mean:",mean,"std:", std)

#binomial distribution model
mean_binomial = N*p_H
std_bionomial = np.sqrt(N*p_H*(1-p_H))
print("mean_binomial:", mean_binomial,"std_bionomial:", std_bionomial)
```
