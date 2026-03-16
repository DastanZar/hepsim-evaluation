ML4SCI HEPSIM: GSoC 2026 Evaluation Task

Objective: To analyze quark and gluon jets by extracting kinematic observables, performing Lorentz boosts, and training a machine learning classifier to evaluate feature representations.

Approach & Findings: In this notebook, I implemented a highly optimized, fully vectorized NumPy data pipeline to process 100,000 jets without standard loops. I calculated Lab-frame features (Jet Mass, Width, and pT Dispersion) by masking zero-padded constituents, and subsequently boosted the four-momenta into the Jet Center-of-Mass (CM) frame. Finally, I trained Random Forest classifiers to distinguish quark from gluon jets using both reference frames.

The classifiers achieved identical predictive power (AUC ≈ 0.855 in both frames). This physically aligns with the extraction data: the most highly discriminating features for Quark/Gluon tagging specifically Constituent Multiplicity and Invariant Jet Mass (CM energy) are Lorentz-invariant. Therefore, boosting to the rest frame injects no new distinguishing information into the system.
