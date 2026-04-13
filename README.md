# Single-Photon Advantage in Quantum Cryptography Beyond QKD

Welcome! I am sharing my project for the Light Matter Interaction (PH 530) course at IIT Bombay, guided by Professor Anshuman Kumar. In this executable paper, I explore the critical role of single-photon sources in distrustful quantum cryptography protocols.

## Introduction & Motivation
While Quantum Key Distribution (QKD) provides unconditional security between *trusted* parties against an outside eavesdropper, many practical cryptographic tasks (e.g., randomized leader election, secure multi-party computation, online casinos) involve parties who **do not trust each other**. 

This project focuses on **Quantum Strong Coin Flipping (QSCF)**, a cryptographic primitive that allows two spatially separated, distrusting parties to agree on a perfectly random, unbiased binary bit. 

We specifically tackle the "hardware loophole" inherent in traditional setups that use Weak Coherent Pulses (WCPs) from attenuated lasers. Because laser light follows a Poisson distribution, it occasionally emits multi-photon pulses, leaving the protocol vulnerable to photon-splitting attacks from a dishonest receiver. Our work demonstrates why a deterministic **Single-Photon Source (SPS)** is mandatory to close this loophole.

## Key Features & Simulations
In this notebook, I have included:
* **Security Framework:** Mathematical definitions of honest winning probabilities, cheating probabilities ($P_A^*$ and $P_B^*$), bias, and honest abort probability ($P_{abort}$) to evaluate the protocol's fairness.
* **Hardware Comparison:** Python simulations comparing the photon-number probabilities and multi-photon risks of WCP Lasers, Realistic Quantum Dot SPS, and Ideal SPS.
* **Input-Output Modeling:** Visualization of the theoretical ideal baseline matrix (using the Born Rule) versus real-world experimental implementations under varying levels of channel loss.
* **Security Metrics:** Demonstrating a ~7.6x cheating-risk reduction when transitioning from WCP to a Realistic SPS.

## Final Conclusion
The models and experimental results confirm that a single-photon source provides significantly better security and successfully suppresses multi-photon events. Most importantly, the experimentally obtained cheating probability lies strictly below the classical limit, confirming a genuine quantum advantage in distrustful cryptographic protocols. Single-photon sources are not merely an improvement over weak coherent pulses, but a necessary resource for achieving secure and fair quantum coin flipping.
