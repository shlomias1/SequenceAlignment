# Sequence Alignment Analysis

This project demonstrates sequence alignment between genetic sequences of various species using two alignment methods: `globalxx` and `globalms`. It includes the comparison of sequence identity, gap handling, and mutation penalties, with a focus on evolutionary similarities between different species.

## Table of Contents

- [Overview](#overview)
- [Methods](#methods)
  - [GlobalXX](#globalxx)
  - [GlobalMS](#globalms)
- [Results](#results)
- [Setup](#setup)
- [Usage](#usage)
- [Contact](#contact)

## Overview

This project compares genetic sequences from multiple species, including baboon, cat, macaque, orangutan (Pongo), chimpanzee (Pan troglodytes), and human (H. sapiens). The goal is to assess sequence alignment using two different alignment methods and evaluate the results in terms of identity percentage, gaps, and transitions or transversions.

## Methods

### GlobalXX

The `globalxx` method performs global alignment without taking into account mutations (transitions or transversions) or penalizing gaps. This method focuses primarily on the matching bases between sequences and calculates the identity based on exact matches.

### GlobalMS

The `globalms` method performs global alignment while considering gap penalties, and also penalizes mutations such as transitions and transversions between bases. This approach provides a more accurate reflection of evolutionary differences and similarities by accounting for sequence changes.

## Results

**Identity Comparison:**

In the analysis of the genetic sequences, the highest identity was observed between the baboon and cat sequences, showing an identity percentage of 86.04%. This result is somewhat surprising, as evolutionary expectations suggest that animals that are closer genetically, such as baboons and macaques, should exhibit higher identity percentages. However, certain genetic features or shared genes between the baboon and cat could explain this result despite the evolutionary distance.

When comparing mitochondrial DNA sequences between different species, the highest identity was found between humans and chimpanzees (83.19%), which is consistent with their close evolutionary relationship.

**GlobalXX Alignment:**

The `globalxx` alignment method resulted in high sequence matching percentages but did not account for mutations or gaps. The presence of gaps reflects variations in sequence length and alignment precision.

For example, the comparison between the baboon and cat sequences showed a high number of matches, but no transitions or transversions were detected. This method does not penalize for gaps or sequence variations, providing a simpler comparison of the sequences.

**GlobalMS Alignment:**

The `globalms` alignment method, which accounts for gap penalties and mutations, provided more accurate results, including the consideration of transitions, transversions, and gaps. This approach reflects a more detailed evolutionary relationship between the species.

For example, when comparing the baboon and cat sequences using `globalms`, there were 169 transitions and 32 transversions detected, in addition to a small number of gaps. These results are more aligned with the evolutionary expectations for these species.

## Setup

To run the sequence alignment analysis, you'll need to have the following dependencies installed:

- Python 3.x
- Biopython library (for sequence parsing and manipulation)

### Installation

You can install the required libraries using pip:

```bash
pip install biopython
```

## Usage

1. Clone this repository:
```bash
git clone https://github.com/yourusername/sequence-alignment.git
```

2. Navigate to the project directory:
```bash
cd sequence-alignment
```

3. Run the analysis script:
```bash
python alignment_analysis.py
```

This will execute the sequence alignment and output the results for each method (`globalxx` and `globalms`), along with the identity percentages and other relevant statistics.

## Contact

If you have any questions or need further assistance, feel free to contact me at:

- Email: shlomiasi1@gmail.com
