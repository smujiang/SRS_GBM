
# 1.1 Patient & Baseline Tumor Characteristics

| Var name        | Original column text                            | Description                                               | Type        | Coding / notes                                                        |
| --------------- | ----------------------------------------------- | --------------------------------------------------------- | ----------- | --------------------------------------------------------------------- |
| `center`        | Center                                          | Recruiting center/site                                    | categorical | String or factor                                                      |
| `patient_id`    | (add)                                           | Unique identifier (if not present, create)                | categorical | e.g. 1,2,3…                                                           |
| `diag_date`     | Date of first diagnosis (date of first surgery) | Date of initial diagnosis / first surgery                 | date        | `YYYY-MM-DD`                                                          |
| `age_dx`        | Age at diagnosis                                | Age at first diagnosis                                    | numeric     | years                                                                 |
| `sex`           | Sex (M/F)                                       | Biological sex                                            | categorical | `M`, `F`                                                              |
| `who_2021_dx`   | WHO 2021 Diagnosis (must be Glioblastoma)       | WHO 2021 tumor diagnosis                                  | categorical | Likely all “GBM”                                                      |
| `idh_status`    | IDH status (must be Wildtype)                   | Isocitrate dehydrogenase status                           | categorical | store but constant (IDH-wt)                                           |
| `mgmt`          | MGMT (methyl/unmethyl/n.a.)                     | MGMT promoter methylation                                 | categorical | `methyl`, `unmethyl`, `NA`                                            |
| `tert`          | TERT (mut/unmut)                                | TERT promoter mutation status                             | categorical | `mut`, `wt`                                                           |
| `egfr_amp`      | EGFR amplification (ampl/non-ampl)              | EGFR amplification                                        | binary/cat  | 1 = ampl, 0 = non-ampl                                                |
| `pten_mut`      | PTEN (mut/umut)                                 | PTEN mutation                                             | binary/cat  | 1 = mut, 0 = wt                                                       |
| `chr7_10`       | Chromosome 7+/10- (yes/no)                      | Presence of 7+/10− signature                              | binary      | 1 = yes, 0 = no                                                       |
| `dom_hemi`      | Dominant hemisphere (Yes/No)                    | Tumor in language-dominant hemisphere                     | binary      | 1 = yes, 0 = no                                                       |
| `deep_tumor`    | Deep Seated Tumors                              | Tumor in deep structures (thalamus/basal ganglia/midline) | binary      | 1 = yes, 0 = no                                                       |
| `multifocal_dx` | Multifocal (Yes/No)                             | Multifocal tumor at diagnosis                             | binary      | 1 = yes, 0 = no                                                       |
| `loc_code`      | Anatomic localization (1–6)                     | Primary anatomic lobe/region                              | categorical | 1=frontal, 2=parietal, 3=occipital, 4=temporal, 5=cerebellar, 6=other |
| `loc_frontal`   | Frontal                                         | Indicator for frontal involvement                         | binary      | 1/0                                                                   |
| `loc_parietal`  | Parietal                                        | Parietal involvement                                      | binary      | 1/0                                                                   |
| `loc_occipital` | Occipital                                       | Occipital involvement                                     | binary      | 1/0                                                                   |
| `loc_temporal`  | Temporal                                        | Temporal involvement                                      | binary      | 1/0                                                                   |
| `loc_cereb`     | Cerebellar                                      | Cerebellar involvement                                    | binary      | 1/0                                                                   |
| `loc_other`     | Others (deep midline structures)                | Other/deep midline                                        | binary      | 1/0                                                                   |



# 1.2 Initial Treatment
| Var name           | Original column text                          | Description                                     | Type        | Coding / notes           |
| ------------------ | --------------------------------------------- | ----------------------------------------------- | ----------- | ------------------------ |
| `surg_type`        | Type of surgery (biopsy/craniotomy)           | First-line surgery type                         | categorical | `biopsy` vs `craniotomy` |
| `surg_biopsy`      | Biopsy                                        | Indicator for biopsy                            | binary      | 1=biopsy performed       |
| `surg_craniot`     | Craniotomy                                    | Indicator for craniotomy                        | binary      | 1=craniotomy performed   |
| `rt_initial`       | RT                                            | Received initial radiotherapy                   | binary      | 1 = yes, 0 = no          |
| `tmz_initial`      | TMZ                                           | Temozolomide during initial therapy             | binary      | 1 = yes, 0 = no          |
| `bev_initial`      | Bevacizumab                                   | Bevacizumab during initial course               | binary      | 1 = yes, 0 = no          |
| `immuno_initial`   | Immunotherapy                                 | Any immune therapy (e.g. checkpoint inhibitors) | binary      | 1 = yes, 0 = no          |
| `ttf_initial`      | TTFields                                      | Tumor Treating Fields                           | binary      | 1 = yes, 0 = no          |
| `other_tx_initial` | Others                                        | Other systemic treatment                        | text/cat    | optional                 |
| `exp_tx_initial`   | Additional experimental treatment (yes/no)    | Any experimental agent at baseline              | binary      | 1 = yes, 0 = no          |
| `trial_initial`    | Patient enrolled in a clinical trial (yes/no) | Clinical trial participation at initial therapy | binary      | 1 = yes, 0 = no          |


# 1.3 First Recurrence & SRS / Re-RT
| Var name            | Original column text                                                | Description                             | Type        | Coding / notes |
| ------------------- | ------------------------------------------------------------------- | --------------------------------------- | ----------- | -------------- |
| `rec1_flag`         | 1st Recurrence (1: yes, 0: no)                                      | Indicator of first recurrence           | binary      | 1/0            |
| `rec1_date`         | Date of first recurrence per RANO (date of MRI)                     | Date of radiologic recurrence           | date        |                |
| `rec1_resectable`   | Resectability per Neurosurgeon… (1: yes, 0: no)                     | Neurosurgeon’s opinion on resectability | binary      | 1/0            |
| `rec1_surg`         | Surgical Resection (1: yes, 0: no)                                  | Re-resection at first recurrence        | binary      | 1/0            |
| `srs_date`          | Date of SRS or last day of re-RT for recurrence                     | Date of SRS / completion of re-RT       | date        |                |
| `kps_srs`           | KPS before SRS or re-RT for Recurrence                              | Karnofsky score right before SRS        | numeric     | 0–100          |
| `srs_comp_code`     | SRS or re-RT complications - 1: RN, 2: seizures, 3: others, 0: none | Overall complication category           | categorical | 0–3            |
| `srs_rn`            | Radiation necrosis                                                  | Specific RN indicator                   | binary      | 1/0            |
| `srs_seizure`       | Seizures                                                            | Post-treatment seizures                 | binary      | 1/0            |
| `srs_new_deficit`   | New post-SRS or re-RT neurological deficit (1:yes, 0:no)            | New neurologic deficit                  | binary      | 1/0            |
| `srs_deficit_trans` | Neurological deficit transient (<3 months) (1:yes, 0: no)           | Deficit resolved < 3 months             | binary      | 1/0            |


# 1.4 SRS Dosimetry and Targeting
| Var name          | Original column text                                              | Description                                          | Type        | Coding / notes    |
| ----------------- | ----------------------------------------------------------------- | ---------------------------------------------------- | ----------- | ----------------- |
| `srs_dose`        | SRS Dose (Gy)                                                     | Prescribed SRS dose                                  | numeric     | Gy                |
| `srs_dose_med_lo` | SRS Dose by Median (including 16 in lower)                        | Indicator for dose ≤ median (incl 16)                | binary      | 1 = lower         |
| `srs_dose_med_hi` | SRS Dose by Median (including 16 in higher)                       | Indicator for dose ≥ median (incl 16)                | binary      | 1 = higher        |
| `srs_dose_q1`     | SRS Dose by 1st quartile (14)                                     | Indicator for dose grouping wrt 14 Gy                | binary      | as specified      |
| `srs_dose_q3`     | SRS Dose by 3rd quartile (19)                                     | Indicator grouping wrt 19 Gy                         | binary      |                   |
| `srs_dose_psm19`  | SRS Dose for PSM (19)                                             | Dose group for propensity score matching (19 Gy cut) | binary      |                   |
| `srs_dose_psm16`  | SRS Dose for PSM (16)                                             | Dose group for PSM (16 Gy cut)                       | binary      |                   |
| `srs_dose_pub`    | SRS Dose for analysis by prior publication                        | Dose categories per prior paper                      | binary/cat  | follow manuscript |
| `srs_target_type` | Target 1: enhancing tumor, 2: enhancement + Flair/T2, 3: Flair/T2 | What is targeted in SRS                              | categorical | 1–3               |
| `srs_fx`          | Fractions                                                         | Number of fractions                                  | numeric     |                   |
| `srs_isodose`     | Isodose Line (%)                                                  | Prescribed isodose line percentage                   | numeric     |                   |
| `srs_min`         | Min (Gy)                                                          | Minimum dose in target                               | numeric     |                   |
| `srs_max`         | Max (Gy)                                                          | Maximum dose in target                               | numeric     |                   |
| `srs_mean`        | Mean (Gy)                                                         | Mean target dose                                     | numeric     |                   |
| `srs_n_targets`   | Number of Targets                                                 | Number of targets treated                            | numeric     |                   |
| `srs_coverage`    | Coverage                                                          | Volume of target receiving prescription dose         | numeric     | (0–1 or %)        |
| `srs_selectivity` | Selectivity                                                       | How well dose conforms to target                     | numeric     |                   |
| `srs_gi`          | Gradient Index                                                    | Dose fall-off metric                                 | numeric     |                   |


# 1.5 Recurrence Localization & Pattern of Failure
| Var name              | Original column text                                                      | Description                               | Type        | Coding / notes |
| --------------------- | ------------------------------------------------------------------------- | ----------------------------------------- | ----------- | -------------- |
| `dom_hemi_rec`        | Dominant hemisphere (Yes/No) (recurrence block)                           | Recurrence in dominant hemisphere         | binary      | 1/0            |
| `rec_loc_type`        | Recurrence localization (1: cortical/subcortical, 2: deep, 3: multifocal) | Recurrence pattern by depth/multifocality | categorical | 1–3            |
| `deep_tumor_rec`      | Deep-seated tumor                                                         | Deep recurrence                           | binary      | 1/0            |
| `multifocal_rec`      | Multifocal (Yes/No)                                                       | Multifocal recurrence                     | binary      | 1/0            |
| `rec_loc_code`        | Anatomical localization of recurrence (1–6)                               | Lobe at recurrence                        | categorical | 1–6            |
| `rec_loc_frontal`     | Frontal                                                                   | Frontal recurrence                        | binary      | 1/0            |
| `rec_loc_parietal`    | Parietal                                                                  | Parietal recurrence                       | binary      | 1/0            |
| `rec_loc_occipital`   | Occipital                                                                 | Occipital recurrence                      | binary      | 1/0            |
| `rec_loc_temporal`    | Temporal                                                                  | Temporal recurrence                       | binary      | 1/0            |
| `rec_loc_cereb`       | Cerebellar                                                                | Cerebellar recurrence                     | binary      | 1/0            |
| `rec_loc_other`       | Others (deep midline structures)                                          | Deep/midline recurrence                   | binary      | 1/0            |
| `failure_infield`     | Pattern of failure 1: In-field, 0: out-of-field                           | If recurrence inside radiation field      | binary      | 1/0            |
| `fail_infield`        | Pattern of failure: In-field                                              | Explicit in-field flag                    | binary      | 1/0            |
| `fail_outfield`       | Pattern of failure: out-of-field                                          | Explicit out-of-field flag                | binary      | 1/0            |
| `fail_residual`       | Residual contrast-enhancing tumor left after first-line therapy           | Failure from residual tumor               | binary      | 1/0            |
| `fail_adj_cavity`     | Adjacent to resection cavity                                              | Recurrence adjacent to cavity             | binary      | 1/0            |
| `fail_flair_not_adj`  | Within initial T2/FLAIR abnormality but not adjacent to resection cavity  | Local, non-cavity recurrence              | binary      | 1/0            |
| `fail_distant_conn`   | Distant with continuous connection to initial T2/FLAIR abnormality        | Distant but connected                     | binary      | 1/0            |
| `fail_distant_unconn` | Distant without any connection to initial T2/FLAIR abnormality            | Truly distant recurrence                  | binary      | 1/0            |


# 1.6 Volume & Systemic Treatment at Recurrence
| Var name    | Original column text                              | Description                       | Type    | Coding / notes                    |
| ----------- | ------------------------------------------------- | --------------------------------- | ------- | --------------------------------- |
| `vol_srs`   | Pre-SRS/RT contrast-enhancing tumor volume in cm³ | Volume treated with SRS           | numeric | cm³                               |
| `vol_med3`  | Volume for analysis by Median (3 cm)              | Indicator for volume > or ≤ 3 cm³ | binary  | 1 = above cutoff (define clearly) |
| `vol_q1_08` | Volume by 1st quartile (0.8 cm)                   | Indicator by Q1 threshold         | binary  |                                   |
| `vol_q3_87` | Volume by 3rd quartile (8.7 cm)                   | Indicator by Q3 threshold         | binary  |                                   |
| `vol_pub5`  | Volume for analysis by prior publication (5 cm)   | Indicator per 5 cm³ cutpoint      | binary  |                                   |

Systemic treatment combinations are at 1st recurrence, 2nd recurrence, etc. For survival analysis, usually summarize them as “received X at recurrence (ever/never)” and possibly a regimen category.

# 1.7 Outcomes
| Var name            | Original column text             | Description                               | Type    | Coding / notes               |
| ------------------- | -------------------------------- | ----------------------------------------- | ------- | ---------------------------- |
| `death`             | Death (1: yes / 0: no)           | Vital status                              | binary  | 1 = dead, 0 = alive/censored |
| `last_fu_date`      | Date of death or last follow-up  | Date of final contact                     | date    |                              |
| `pfs_time`          | PFS                              | Progression-free survival time (if given) | numeric | Check units (months vs days) |
| `os_time`           | OS                               | Overall survival time (if given)          | numeric | Check units                  |
| `prs_time`          | PRS                              | Post-recurrence survival                  | numeric |                              |
| `srs_surv_time`     | Survival from SRS                | Time from SRS to death/last FU            | numeric |                              |
| `time_prog_to_srs`  | Time from progression to SRS     | Interval from recurrence to SRS           | numeric |                              |
| `time_srs_to_prog2` | Time from SRS to 2nd progression | Second progression survival               | numeric |                              |

If PFS/OS are not provided as numeric intervals, derive them from the dates
