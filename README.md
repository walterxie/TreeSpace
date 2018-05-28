# Tree Space

Display the topologies of 3-taxa tree sampled from MCMC 
under Kingman's coalescent model.

## 3 Taxa

There are 3 different topologies in this tree space:
1. `T=0`, where the tree is `(A,B),C`; 
2. `T=1`, where the tree is `(A,C),B`; 
3. `T=2`, where the tree is `(B,C),A` or `(C,B),A`. 

We define the tree interval _k<sub>1</sub>_ is the root height minus
internal node height, and _k<sub>2</sub>_ is the internal node height.
Both _k<sub>1</sub>_ and _k<sub>2</sub>_ are sampled by MCMC, where
the probability of genealogies in a population is:

P(k<sub>1</sub>, k<sub>2</sub>, T | Ne) = 
(1/Ne) * e<sup>(-k<sub>1</sub>/Ne)</sup> * (1/Ne) * e<sup>(-3*k<sub>2</sub>/Ne)</sup> 

Assuming Ne = 1, then simplify the above equation to:

P(k<sub>1</sub>, k<sub>2</sub>, T) = e<sup>-k<sub>1</sub></sup> * e<sup>(-3*k<sub>2</sub>)</sup>


The animation of 1000 samples is available from 
[here](https://walterxie.github.io/TreeSpace/).

<video src="note/TreeSpace3Taxa.mp4" width="640" height="600" controls preload>
  <source src="note/TreeSpace3Taxa.mp4" type="video/mp4">
</video>

## Code

The python 3 source code is available from the Jupyter Notebook file 
[TreeSpace3Taxa.ipynb](note/TreeSpace3Taxa.ipynb)

## Diagnose

* MovieWriter ffmpeg unavailable:

```bash
brew install ffmpeg
ffmpeg
```

