# TP-TeoriaDeLaInfo

This repository contains practical assignments (Trabajos Practicos) for an Information Theory course. The projects implement various concepts from information theory including entropy calculation, code analysis, data compression, and communication channels.

## Projects Overview

### TP1 - Information Sources and Entropy Analysis
Analyzes information sources by calculating entropy, conditional probability matrices, and stationary vectors. This tool helps understand the information content of binary sources and their memory properties.

**Features:**
- Reads binary data files
- Calculates conditional probability matrices
- Computes entropy of information sources
- Determines if sources have null or non-null memory
- Calculates stationary vectors for memory sources
- Supports N-order entropy calculations

### TP2 - Code Analysis
Analyzes binary codes to determine their properties and efficiency. Implements verification of code compactness and instantaneousness according to information theory principles.

**Features:**
- Analyzes code properties from text files
- Verifies Kraft inequality compliance
- Determines if codes are instantaneous
- Checks code compactness
- Calculates entropy and average code length
- Creates alphabet from input data

### TP3 - LZW Compression/Decompression
Implements the Lempel-Ziv-Welch (LZW) compression algorithm for text file compression and decompression. Calculates compression metrics including compression ratio, efficiency, and redundancy.

**Features:**
- Encodes text files using LZW algorithm
- Decodes compressed binary files
- Calculates compression ratio
- Measures compression efficiency
- Computes redundancy percentage

### TP4 - Communication Channels and Error Detection
Simulates binary communication channels with noise and implements parity checking methods for error detection and correction. Analyzes information transmission through noisy channels.

**Features:**
- Generates random binary messages
- Simulates message transmission through noisy channels
- Implements crossed parity checking
- Detects and corrects single-bit errors
- Calculates channel entropies (a priori and a posteriori)
- Computes equivocation and mutual information
- Analyzes error rates in message transmission

## Requirements

The projects require Python 3 with the following dependencies:

- numpy
- pandas

## Installation

1. Clone the repository:
```bash
git clone https://github.com/NahuelBarriga/TP-TeoriaDeLaInfo.git
cd TP-TeoriaDeLaInfo
```

2. Install required dependencies:
```bash
pip install numpy pandas
```

## Usage

### TP1 - Information Sources Analysis

Navigate to the TP1 directory and run:

```bash
cd TP1
python3 Tp1.py <binary_file> [N]
```

**Parameters:**
- `<binary_file>`: Path to the binary file to analyze (located in Samples directory)
- `[N]` (optional): Order for N-order entropy calculation

**Example:**
```bash
python3 Tp1.py Samples/tp1_sample0.bin
python3 Tp1.py Samples/tp1_sample0.bin 2
```

### TP2 - Code Analysis

Navigate to the TP2 directory and run:

```bash
cd TP2
python3 tp2.py <input_file>
```

**Parameters:**
- `<input_file>`: Text file containing code words separated by spaces

**Example:**
```bash
python3 tp2.py tp2_sample0.txt
```

### TP3 - LZW Compression

Navigate to the TP3 directory and run:

**To compress a file:**
```bash
cd TP3
python3 Tp3.py <original.txt> <compressed.bin> -c
```

**To decompress a file:**
```bash
python3 Tp3.py <original.txt> <compressed.bin> -d
```

**Parameters:**
- `<original.txt>`: Original text file (must be in Samples directory)
- `<compressed.bin>`: Output/input compressed binary file
- `-c`: Compress mode
- `-d`: Decompress mode

**Example:**
```bash
python3 Tp3.py tp3_sample0.txt compressed0.bin -c
python3 Tp3.py tp3_sample0.txt compressed0.bin -d
```

### TP4 - Communication Channels

Navigate to the TP4 directory and run:

```bash
cd TP4
python3 Tp4.py <probabilities_file> N M [-p]
```

**Parameters:**
- `<probabilities_file>`: Text file containing source probabilities and channel transition matrix (must be in Samples directory)
- `N`: Number of rows in the message matrix
- `M`: Number of columns in the message matrix
- `[-p]` (optional): Flag for additional parity checking mode

**Example:**
```bash
python3 Tp4.py tp4_sample0.txt 10 10
python3 Tp4.py tp4_sample0.txt 10 10 -p
```

**Probabilities file format:**
The file should contain:
- First line: Source probabilities (e.g., `0.5 0.5`)
- Second and third lines: Channel transition matrix rows

## Project Structure

```
TP-TeoriaDeLaInfo/
├── TP1/
│   ├── Tp1.py                    # Main program for entropy analysis
│   ├── Samples/                  # Sample binary files for testing
│   └── Trabajo Integrador 1.pdf  # Project specification
├── TP2/
│   ├── tp2.py                    # Main program for code analysis
│   ├── Samples/                  # Sample text files with code words
│   └── Trabajo Integrador 2.pdf  # Project specification
├── TP3/
│   ├── Tp3.py                    # Main program for LZW compression
│   ├── Samples/                  # Sample text files for compression
│   └── compressed*.bin           # Example compressed files
└── TP4/
    ├── Tp4.py                    # Main program for channel simulation
    ├── Samples/                  # Sample probability configuration files
    └── Informe TP4 - Grupo H.docx.pdf  # Project report
```

## Authors

Group H - Information Theory Course

## License

This project is part of academic coursework.
