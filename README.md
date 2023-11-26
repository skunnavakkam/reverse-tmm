# Reverse Transfer Matrix Method

This is an implementation of the reverse transfer matrix method in Python, which offers a way to find properties (r. index, thickness) of individual layers in multilayer stacks from a single Reflectance and Transmittance measurement at **any** incidence.

The transfer matrix method assigns one matrix per interface. Each layer has two interfaces.

$$
M_1 \cdot M_2 \cdot \ldots \cdot M_i \cdot M_{i+1} \cdot \ldots \cdot M_{n-1} \cdot M_n = \widetilde{M}
$$

Since the parts to the left and right of $M_i \cdot M_{i+1}$ are known, I just replace them.

$$
M_{left} \cdot M_i \cdot M_{i+1} \cdot M_{right} = \widetilde{M}
$$

$$
M_i \cdot M_{i+1} = M_{left}^{-1} \cdot \widetilde{M} \cdot M_{right}^{-1}
$$

Interestingly, we don't know what $\widetilde{M}$ is. Instead, we have the element-wise absolute value of $\widetilde{M}$. Thus, I currently only have the absolute value of refractive index.
