# Evolving Soft Robots For Control Using a Gene Regulatory Network

<img src='screenshot.png' alt='Image of soft robots evolved with a GRN' width='500' />

This repository contains the Python code which accompanies my BSc Computer Science Dissertation, where I investigated how soft robots could be controlled and designed by an evolved Gene Regulatory Network (GRN) to complete locomotion and object-manipulation tasks.

For this research project, I used [EvoGym](https://evolutiongym.github.io/) to simulate Voxel-based Soft Robots (VSR). I also designed and implemented a developmental model and a decentralised controller in Python that uses a GRN to both design the robot's architecture and control its movements. In my application, populations of GRNs are evolved with an Evolutionary Algorithm, which I implemented with Python's multiprocessing library to take advantage of performing fitness evaluations in parallel on multiple CPU cores.

## Project Structure

This repository was forked from [EvoGym](https://github.com/EvolutionGym/evogym) so that my classes and methods can be integrated within EvoGym's simulator. My methods can be found under the "gene_regulatory_network" directory. Within this directory are three folders, each representing a different major iteration in the project's development:

- **[gene_regulatory_network/initial](https://github.com/nathanielbrookes/evogym/tree/a87a6e122471bc298f0995d47da1c85acd24663d/gene_regulatory_network/initial)** - Contains the initial code for conducting evolutionary experiments using a GRN to optimise the robot's movements with fixed designs.
- **[gene_regulatory_network/refinement pt.1](https://github.com/nathanielbrookes/evogym/tree/a87a6e122471bc298f0995d47da1c85acd24663d/gene_regulatory_network/refinement%20pt.1)** - Contains the code for the first refinement iteration, which builds upon the previous implementation to improve the model's results. This contains an updated Evolutionary Algorithm which implements a crossover operator to combine genetic information from parents, and Tournament Selection to select the best candidates. Experiments for this iteration are still concerned with optimising the robot's controller only.
- **[gene_regulatory_network/refinement pt.2 (co-evolution)](https://github.com/nathanielbrookes/evogym/tree/a87a6e122471bc298f0995d47da1c85acd24663d/gene_regulatory_network/refinement%20pt.2%20(co-evolution))** - Contains the code for the final iteration of the project, where a different approach is considered to improve the model's performance. This includes an implementation of a developmental model and a decentralised controller, which allows the GRN to be co-evolved to both control the robot's behaviour and specify its design.
