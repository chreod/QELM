# QELM

This repository is for the QOSF mentorship application. `notebook.ipynb` implements a very simple function for generating random Perceval photonic circuits.

The goal of the notebook is to implement the following steps to generate a quantum circuit:
- Generate a random diagram in the ZX calculus using PyZX.
- Export the ZX circuit in the QASM format and load as a Qiskit circuit.
- Convert the Qiskit circuit into a Perceval linear optics circuit.
   

The ZX calculus has recently been used to natively represent quantum linear optics protocols [1]. This notebook is a current workaround that converts a ZX diagram into a Perceval circuit using QASM and Qiskit as an intermediary.  The category theoretic approach in [1] will allow a direct translation of ZX diagrams into Perceval circuits.

Why focus on the ZX calculus?  The ZX calculus is a sound and complete diagrammatic language. Furthermore, by being a diagrammatic language it makes salient all the compositional features of quantum theory.  In fact, there's strong evidence that composition of words and sentences, and the composition of quantum systems share a similar mathematical structure [2], [3].  In [3], sentences in natural language are converted into ZX diagrams.  This suggests that ZX diagrams themselves may be the right data structure for large language models (LLM) to interact with.

How can an LLM be used with ZX diagrams?  One promising direction is to use the LLM as a mutation operator in a genetic algorithm.  This was demonstrated successfully in [4].  In fact, genetic algorithms have a long history of being used to generate quantum circuits.  See [5] for a review.  [4] brings together the unique combination of novelty search, LLM, and genetic algorithms.

Recently, an open source effort to reproduce the model of [4] was initiated [6]. A promising direction is to extend [4] by creating a 'quantum circuit' environment for the LLM to suggest mutations for.  This environment could be the space of possible ZX diagrams, which could be converted into optical circuits to run on generic photonic devices.

## References

[1] Giovanni de Felice, Bob Coecke. "Quantum Linear Optics via String Diagram"

[2] Bob Coeke et al. "Foundations for Near-Term Quantum Natural Language Processing". In: arXiv preprint arXiv:2012.03755 (2020)

[3] Amin Karamlou, Marcel Pfaffhauser, James Wootton. "Quantum Natural Language Generation on Near-Term Devices". In: arXiv preprint arXiv:2211.00727

[4] Joel Lehman et al. "Evolution through Large Models". In: arXiv:2206.08896

[5] Rafael Lahoz-Beltra "Quantum Genetic Algorithms for Computer Scientists" Computers (2016)

[6] https://github.com/CarperAI/OpenELM
