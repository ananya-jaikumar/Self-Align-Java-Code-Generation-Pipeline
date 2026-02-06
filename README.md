# Self-Alignment Instruction-Tuning Pipeline for Java using StarCoder2-15B

[![Python](https://img.shields.io/badge/Python-3.10.8-blue.svg)](https://www.python.org/)
[![StarCoder2](https://img.shields.io/badge/Model-StarCoder2--15B-orange.svg)](https://huggingface.co/bigcode/starcoder2-15b)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![arXiv](https://img.shields.io/badge/arXiv-Research%20Paper-red.svg)](https://arxiv.org/)



## 📋 Abstract

Large Language Models (LLMs) have demonstrated impressive ability in code generation but remain under-aligned for languages beyond Python. This research introduces a **Self-Alignment Instruction-Tuning Pipeline for Java** using StarCoder2-15B, designed to produce executable and validated instruction-response datasets aligned with BigCode's open-source methodology.

The pipeline achieves:
- ✅ **85%+ code compilation success rate**
- ✅ **1,153 validated Java samples** from 5,954 extracted methods
- ✅ **Automated three-stage transformation** from raw code to instruction-response pairs
- ✅ **Executable validation** with compilation and runtime testing

## 🎯 Key Features

### 🔄 Three-Stage Pipeline Architecture

1. **Seed Gathering (S→C)**: Tree-sitter-based extraction of Java methods from Stack v2 dataset
2. **Concept & Instruction Generation (C→I)**: StarCoder2-15B generates programming concepts and natural language instructions
3. **Response Generation & Validation (I→R)**: Creates executable code with embedded test cases and validates through compilation

### 🚀 Technical Highlights

- **Tree-sitter Parsing**: Automated AST-based Java method extraction
- **vLLM Inference**: Efficient batch processing with StarCoder2-15B
- **Compilation-Driven Filtering**: Eliminates non-executable samples using `javac`
- **Runtime Validation**: Tests execution correctness with embedded test cases
- **Multiprocessing**: Parallel processing for large-scale dataset handling

## 📊 Results

| Metric | Value |
|--------|-------|
| Initial Methods Extracted | 5,954 |
| Filtered Samples | 2,286 |
| Validated Instruction-Response Pairs | 1,153 |
| Compilation Success Rate | 85.4% |
| Deep Validation Pass Rate | 46% (23/50 samples) |

