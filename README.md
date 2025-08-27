# ResPlan2: Solver for Resilient Planning Problem

[![License](https://img.shields.io/badge/license-MIT-blue)]() [![DOI](https://img.shields.io/badge/DOI-10.3233%2FFAIA230252-blue)](https://doi.org/10.3233/FAIA230252)

---

## 📑 Table of Contents
- [Overview](#overview)
- [Academic Reference](#-academic-reference)
- [Build](#-build)
- [Examples](#-examples)
- [Usage](#-usage)
- [Contact & Issues](#-contact--issues)
- [License](#license)

---

## Overview

In many real-world scenarios, agent plan execution may fail unpredictably. The **Resilient Planning** paradigm (and the RESPLAN framework) introduces the notion of *k-resilient plans*: strategies that achieve goals despite up to *k* execution failures.

This repository presents an enhanced version of the RESPLAN algorithm with:
- **Landmark-based pruning**
- **E-planning with regression-based strategies**

---


## 📄 Academic Reference

If you use this software, please cite the following article:
> "**Action-Failure Resilient Planning**".  
> Aineto Diego; Gaudenzi Alessandro; Gerevini Alfonso; Rovetta Alberto; Scala Enrico; Serina Ivan.  

**BibTeX:**

```bibtex
@inbook{inbook,
author = {Aineto, Diego and Gaudenzi, Alessandro and Gerevini, Alfonso and Rovetta, Alberto and Scala, Enrico and Serina, Ivan},
year = {2023},
month = {09},
pages = {},
title = {Action-Failure Resilient Planning},
isbn = {9781643684369},
doi = {10.3233/FAIA230252}
}
```
---

## 🚀 Build

```
./src/build_all
```

---

## 💡 Examples
```
/src/resplanner /benchmarks/IPC/zenotravel/domain.pddl /benchmarks/IPC/zenotravel/pfile1 --resilient 1 --dump-resilient-policy 1
/src/resplanner /benchmarks/Res/rocket/domain.pddl /benchmarks/Res/rocket/pfilep1.pddl --resilient 2 --dump-resilient-policy 1 --pruning 1 --adaptive_replan 1
```

---

## ⚙️ Usage

| Option                         | Description                                 |
|---------------------------------|---------------------------------------------|
| `--resilient K`                 | Number of maximum faults allowed            |
| `--pruning 1/0`                 | Enable pruning technique                    |
| `--adaptive_replan 1/0`         | Enable the adaptive replanning technique    |
| `--verbose 1/0`                 | Verbose mode                               |
| `--max-iterations N`            | Limit the iterations of the algorithm       |
| `--plan-to-file 1/0`            | Dump the resilient plan to a file           |
| `--dump-branches 1/0`           | Print branches of the replan to JSON file   |
| `--dump-resilient-policy 1/0`   | Print resilient policy to JSON file         |
| `--dump-resilient-nodes 1/0`    | Print all resilient nodes found             |

---

## 📬 Contact & Issues

For questions, bug reports or feature requests, please open an Issue or contact the maintainers.

---

## License

Distributed under the MIT License.
