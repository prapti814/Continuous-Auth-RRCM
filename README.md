# Continuous User Authentication via R-RCM
**Implementation of IEEE Access (2020) Research by Kiyani et al.**

### Project Overview
This project implements a session-long security framework that validates user identity on every keystroke. It moves beyond static login by using a **Robust-Recurrent Confidence Model (R-RCM)**.
## Reference Paper
This implementation is based on the following research:
* **Title:** Continuous User Authentication Featuring Keystroke Dynamics Based on Robust Recurrent Confidence Model and Ensemble Learning Approach
* **Authors:** Anum Tanveer Kiyani, et al. (2020)
* **Published in:** IEEE Access
* **Link:** [Read the paper here](https://doi.org/10.1109/ACCESS.2020.3019467)

### Data Source
This project utilizes the CMU Keystroke Dynamics Benchmark Dataset. 
**Link:** [The dataset link](https://www.kaggle.com/datasets/carnegiecylab/keystroke-dynamics-benchmark-data-set)

### Key Features
* **Ensemble Learning:** Uses a Weighted Classifier Fusion of SVM, Random Forest, and MLP to generate a "Probability of Genuineness" ($\hat{y}_t$).
* **Asymmetric Security Logic:** Implements **Algorithm 1** from the paper, featuring a dual-threshold system ($T_{alert}$ and $T_{lockout}$).
* **Hard Mode Detection:** When confidence drops below the alert line, the system doubles the penalty for suspicious actions to trigger a rapid lockout.

### Results
* **Imposter Lockout:** Successfully detected and terminated imposter sessions within **9 actions**.
* **Robustness:** Maintained high confidence (>0.95) for genuine users despite simulated typing variance.

### Tech Stack
Python, Scikit-Learn, NumPy, Matplotlib (for trajectory analysis).