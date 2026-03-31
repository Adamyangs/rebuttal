# Table 1: Scaling Law Functional Form Ablation

Progressive rows show incremental modeling of architectural dimensions; Ablation rows remove individual terms from the full model; Variant tests alternative parameterizations. ΔEval is the difference in validation R² relative to Ours (Eq. 2).

| Category | Model | #Params | Train R² | Eval R² | ΔEval |
|---|---|---|---|---|---|
| Progressive | Chinchilla (κ_N/N^α) | 3 | 0.577 | 0.667 | -0.285 |
| | Depth + Width | 5 | 0.792 | 0.854 | -0.098 |
| | + FFN ratio r | 6 | 0.805 | 0.868 | -0.084 |
| | Linear reciprocal | 6 | 0.951 | 0.942 | -0.010 |
| Ablation | w/o ρ (MoE sparsity) | 8 | 0.810 | 0.870 | -0.082 |
| | w/o d_m (GQA) | 9 | 0.969 | 0.945 | -0.007 |
| | β₁ = β₂ (shared) | 10 | 0.954 | 0.938 | -0.014 |
| Variant | α_r₁ ≠ α_r₂ (separate) | 12 | 0.975 | 0.952 | +0.000 |
| Ours (Eq.2) | Full formula | 11 | 0.975 | 0.952 | --- |
