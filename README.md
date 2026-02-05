# EpIC_generator_MC_samples
Location of EpIC generator input files to regenerate DVCS and some VM samples for simulation campaigns

Generator can be found here: https://github.com/pawelsznajder/epic/

## March 6th 2025

Only 10x130 GeV sample has been produced this way - others will follow.

## Feb 3rd 2026 

New `.xml` files added from EpIC (DVCS + Bethe-Heitler + interference), version 1.1.6-1.2, runs in October 2025, intended for the ePIC simulation campaign run 26.02.0. 

The `.hepmc` output files from the EpIC generator have then been passed through the [ePIC afterburner](https://github.com/eic/afterburner), adding a crossing angle and beam smearing; the output from which has been stored on the ePIC XRootD server, under `/volatile/eic/sjdkay/DVCS_Files_04_02_26/raw_sim`. Following this, output files have been passed through a `.hepmc3` to `.root` converter ready for use in the ePIC simulation campaign, and are stored under `/volatile/eic/sjdkay/DVCS_Files_04_02_26/DVCS/`, sorted by beam energy.

The syntax for running the `.hepmc3` to `.root` converter is as follows (using one of the generated samples as an example):
```
./hepmc3ascii2root /volatile/eic/sjdkay/DVCS_Files_04_02_26/raw_sim/dvcs_bh_int_5_41_m_1M_B.hepmc /volatile/eic/sjdkay/DVCS_Files_04_02_26/DVCS/EpIC_1.1.6/5x41/EpIC_1.1.6-1.2_DVCS_BH_5x41_q2_1_100_minus.hepmc3.tree.root
```



