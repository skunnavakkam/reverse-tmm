# Reverse Transfer Matrix Method (TMM)

The transfer matrix method is a useful tool for the simulation of mutlilayer optical stacks based on their refractive index and thickness. 
What if we could extract the refractive index or thickness from Reflection and Transmission measurements?

I'll sketch a derivation at normal incidence for layer $j$:
$$
t_{j, j+1} = \frac{2 n_j}{n_j + n_{j+1}}
$$
$$
r_{j, j+1} = \frac{n_j - n_{j+1}}{n_j + n_{j+1}}
$$

The output of the transfer matrix method $\widetilde{M}$ is a matrix 
$$\left(\begin{matrix}a & b\\b & a\end{matrix}\right)$$
where the amplitude of reflection and transmission are $\frac ba$ and $\frac1a$ respectively.