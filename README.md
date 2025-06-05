# Quantum Fourier Sampling over Conjugacy Classes in Nilpotent Non-Abelian Groups: A Case Study in the Heisenberg Group

We explore quantum Fourier sampling over conjugacy classes in the discrete Heisenberg group \$H\_3(\mathbb{Z}\_p)\$ using Qiskit's statevector simulations. Seven experiments demonstrate sampling distributions from ideal and noisy quantum states. We compare with classical FFT and hidden subgroup cosets, avoiding Aer-based simulation for compatibility with Google Colab.

## Use Cases

* **Quantum Chemistry**: Analyze symmetries in molecular structures.
* **Quantum ML**: Feature encoding via non-Abelian states.
* **Post-Quantum Cryptography**: HSP-based cryptanalysis.
* **Quantum Tomography**: Use conjugacy structure for noise learning.
* **Lattice Gauge Simulation**: Model discretized non-Abelian fields.

## Methodology Summary

1. **Group Encoding**: Define \$H\_3(\mathbb{Z}\_p)\$ elements and conjugacy classes.
2. **State Preparation**: Uniform superposition over a selected conjugacy class.
3. **QFT Simulation**: Apply 5-qubit QFT and measure outcomes.
4. **Manual Noise**: Simulate decoherence using NumPy transformations.
5. **Scaling**: Extend to \$\mathbb{Z}\_5\$ using 7-qubit systems.
6. **FFT Comparison**: Classical FFT on the same vectors.
7. **Coset Sampling**: Identify hidden subgroup structures using QFT.

## Experiments Conducted

* **Exp 1**: Baseline QFT on uniform \$|000\rangle\$ state
* **Exp 2**: Apply QFT on uniform superposition over one conjugacy class of \$H\_3(\mathbb{Z}\_3)\$
* **Exp 3**: Visualize output amplitudes of Fourier-transformed conjugacy class
* **Exp 4**: Apply random noise via NumPy and observe degradation in QFT peaks
* **Exp 5**: Increase \$\mathbb{Z}\_p\$ to \$\mathbb{Z}\_5\$ with 7-qubit system
* **Exp 6**: Classical FFT comparison using NumPy FFT
* **Exp 7**: Coset state QFT for a hidden subgroup in \$H\_3\$, comparing distribution spread

Each experiment includes measurement histograms and outcome statistics. Manual state injection avoids AerSimulator issues on Colab.

## Key Results

* **Ideal QFT**: Reveals sharp peaks tied to conjugacy structure.
* **Noisy QFT**: Peaks degrade but structure remains partially visible.
* **FFT vs QFT**: Classical FFT is smoother; QFT exhibits stronger interference.
* **Coset Signatures**: Clear separation of coset states post-QFT.
* **Scaling**: Quadratic gate cost limits to \~7 qubits.

| Property     | QFT Ideal | QFT Noisy | FFT |
| ------------ | --------- | --------- | --- |
| Sharp Peaks  | ✓         | \~        | ✗   |
| Noise Robust | ✗         | ✓         | ✓   |
| Group Info   | ✓         | \~        | ✗   |

## Conclusion

Quantum Fourier sampling over the Heisenberg group reveals unique structural features not visible classically. Manual noise injection offers an Aer-free way to study decoherence effects. The experiments demonstrate feasibility for group-based quantum algorithms and resource-aware simulation.

---

## References

1. Childs et al. (2010). *Quantum Algorithms for the Hidden Subgroup Problem*. SIAM J. Comput.
2. Moore & Russell (2005). *Symmetric Group & Fourier Sampling*. STOC.
3. Bacon et al. (2005). *Semidirect Products & Quantum Algorithms*. FOCS.
4. Watrous (2018). *The Theory of Quantum Information*.
5. Aharonov & Ta-Shma (2003). *Adiabatic State Generation*. STOC.


