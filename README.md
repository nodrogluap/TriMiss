# TriMiss
Evaluate mismatch sensitivity of every 3-mer context in a genome to PCR primer conditions

## The idea

Calculate the effect of three nucleotide ("Tri") contexts for every possible single nucleotide mismatch in a given sequence, at different cation concentrations. Useful for evaluating the potential for cation concentration sensitivity of melting temperature for mismatches ("Miss") in PCR primers.

## Quick Start
Requires that you have plain old Perl on your system.

To calculate a table with melting temperature drops for all 192 flanking base SNP contexts in the SARS-CoV-2 genome, with a primer length of 33, and cation (e.g. Na+, Mg+) concentrations of 8mM, 80mM, and 800mM:
```
./trimiss sars-cov-2.fa 33 1e-17 6e-10 8e-3,8e-2,8e-1 output_melting_tms_all_three_concs.tsv
```

In this case, 6e-10 represents the molar concentration of the primer (this is the average for TaqPath), and 1e-17 represents the lower detection limit for molar concentration of the template (viral genome in this case).
