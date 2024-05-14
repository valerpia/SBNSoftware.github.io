---
layout: page
title: SBN Production Available Samples wiki
subtitle: Wiki for SBN Production available samples
description: Wiki for the SBN Production Team samples bookkeeping 
hero_height: is-medium
# menubar: sbnprod_menu
toc: true
toc_title: SBN Production Available Samples
---



SBN Production Available Samples Page
==========================================

A list of samples that were requested and produced since Oct 2020 and the status of open requests can be checked at the [SBN Production Requests Database](https://docs.google.com/spreadsheets/d/17mFPGsP7gw4GRLSCwIL15QrtUnLVri_2k2Wjzhd6Ork/edit?usp=sharing). More information on how to make requests can be found at the [SBN Production Wiki](https://sbnsoftware.github.io/sbn/sbnprod_wiki/Wiki).

The spreadsheet contain the configuration files used, the code version, the statistics produced and the SAM dataset for access. Currently the production passes are organized in spreadsheet tabs. If necessary information can't be found, please email the production group at [sbn-mc-prod@fnal.gov](sbn-mc-prod@fnal.gov)

More information about the workflow can be found at the [SBN Analysis Infrastructure Workflow Management page](../../AnalysisInfrastructure/WorkflowManagement/workflow.md).

How to access the samples
--------------------------

MC sample datasets are declared to the SBN SAM instance which is acessible to both SBND and ICARUS collaborators. All samweb commands should specify the SBN instance with `samweb -e sbn`, following are some useful commands:

### Definition commands
- checking definition files: `samweb -e sbn list-definition-files {definition}`
- checking number of files and events (for samples with full metadata): `samweb -e sbn list-definition-files {definition} --summary`

### File commands
- checking metadata: `samweb -e sbn get-metadata {filename}`
- file location: `samweb -e sbn locate-file {filename}`

### Accessing files at CNAF
some of ICARUS samples are available at CNAF, those files are declared to samweb and can be accessed from grid jobs from FNAL.

Recommended workflow:
- Identify files  
`samweb -e icarus get-file-access-url --schema https “file-name.root”`
- Copy a few files locally for development/testing  
`ifdh cp -D <url from above command> /path/to/user/data/area/`
- Submit grid jobs over full sample  

More info about CNAF: https://wiki.infn.it/progetti/icarus/home


Monte Carlo official SBN Production Samples
--------------------------

SBND MC
--------------------------

| Sample Description | production push | release version | # Events | Sample type | Samweb definition |    
| --- | --- | --- | --- | --- | --- |  
| BNB + Cosmics GiBUU | MC2023B | v09_75_03_02 | 102189 | reco1 | official_MCP2023B_prodoverlay_corsika_cosmics_proton_gibuu_dirtpropagation_sbnd_gibuu_g4_wcsim_detsim_reco1_sbnd | 
| --- | --- | --- | --- | reco2 | official_MCP2023B_prodoverlay_corsika_cosmics_proton_gibuu_dirtpropagation_sbnd_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2023B_prodoverlay_corsika_cosmics_proton_gibuu_dirtpropagation_sbnd_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2023B_prodoverlay_corsika_cosmics_proton_gibuu_dirtpropagation_sbnd_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2023B_prodoverlay_corsika_cosmics_proton_gibuu_dirtpropagation_sbnd_caf_flat_caf_sbnd |
| BNB + Cosmics GENIE Recomb (-3,-3) | MC2023B | v09_75_03_02 | 102189 | reco1 | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb-3-3_scrub_g4_wcsim_detsim_reco1_sbnd | 
| --- | --- | --- | --- | reco2 | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb-3-3_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb-3-3_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb-3-3_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb-3-3_flat_caf_sbnd |
| BNB + Cosmics GENIE Recomb (3,3) | MC2023B | v09_75_03_02 | 102189 | reco1 | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb33_scrub_g4_wcsim_detsim_reco1_sbnd | 
| --- | --- | --- | --- | reco2 | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb33_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb33_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb33_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb33_flat_caf_sbnd |
| BNB + Cosmics GENIE Diff (1,0) | MC2023B | v09_75_03_03 | 102189 | reco1 | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_diff-10_scrub_g4_wcsim_detsim_reco1_sbnd | 
| --- | --- | --- | --- | reco2 | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_diff-10_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_diff-10_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_diff-10_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_diff-10_caf_flat_caf_sbnd |
| BNB + Cosmics GENIE Diff (1,0) | MC2023B | v09_75_03_03 | 102189 | reco1 | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_diff10_scrub_g4_wcsim_detsim_reco1_sbnd | 
| --- | --- | --- | --- | reco2 | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_diff10_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_diff10_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_diff10_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_diff10_caf_flat_caf_sbnd |
| BNB + Cosmics GENIE Recomb (0,1) | MC2023B | v09_75_03_02 | 102189 | reco1 | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb01_scrub_g4_wcsim_detsim_reco1_sbnd | 
| --- | --- | --- | --- | reco2 | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb01_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb01_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb01_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb01_caf_flat_caf_sbnd |
| BNB + Cosmics GENIE Recomb (1,0) | MC2023B | v09_75_03_02 | 102189 | reco1 | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb10_scrub_g4_wcsim_detsim_reco1_sbnd | 
| --- | --- | --- | --- | reco2 | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb10_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb10_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb10_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_recomb10_caf_flat_caf_sbnd |
| BNB + Cosmics GENIE CV | MC2023B | v09_75_03_02 | 102189 | reco1 | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_gen_g4_wcsim_detsim_reco1_sbnd | 
| --- | --- | --- | --- | reco2 | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2023B_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_caf_flat_caf_sbnd |
| FullOsc + Cosmics | MC2023A | v09_75_01 | 99250 | reco1 | official_MCP2023A_prodoverlay_corsika_cosmics_proton_genie_fullosc_spill_gsimple-configh-v1_tpc_gen_g4_detsim_reco1_sbnd | 
| --- | --- | --- | 63750 | reco2 | official_MCP2023A_prodoverlay_corsika_cosmics_proton_genie_fullosc_spill_gsimple-configh-v1_tpc_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2023A_prodoverlay_corsika_cosmics_proton_genie_fullosc_spill_gsimple-configh-v1_tpc_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2023A_prodoverlay_corsika_cosmics_proton_genie_fullosc_spill_gsimple-configh-v1_tpc_reco2_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2023A_prodoverlay_corsika_cosmics_proton_genie_fullosc_spill_gsimple-configh-v1_tpc_reco2_flat_caf_sbnd |
| Intrinsic NuE + Cosmics | MC2023A | v09_75_01 | 100050 | reco1 | official_MCP2023A_prodoverlay_corsika_cosmics_proton_genie_intrnue_spill_tpc_sbnd_gen_g4_detsim_reco1_sbn | 
| --- | --- | --- | 99600 | reco2 | official_MCP2023A_prodoverlay_corsika_cosmics_proton_genie_intrnue_spill_tpc_sbnd_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2023A_prodoverlay_corsika_cosmics_proton_genie_intrnue_spill_tpc_sbnd_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2023A_prodoverlay_corsika_cosmics_proton_genie_intrnue_spill_tpc_sbnd_reco2_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2023A_prodoverlay_corsika_cosmics_proton_genie_intrnue_spill_tpc_sbnd_reco2_flat_caf_sbnd |
| Intime Cosmics | MC2023A | v09_75_01 | 112493 | reco1 | official_MCP2023A_prodcorsika_proton_intime_filter_sce_gen_g4_detsim_reco1_sbnd | 
| --- | --- | --- | 112554 | reco2 | official_MCP2023A_prodcorsika_proton_intime_filter_sce_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2023A_prodcorsika_proton_intime_filter_sce_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2023A_prodcorsika_proton_intime_filter_sce_reco2_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2023A_prodcorsika_proton_intime_filter_sce_reco2_flat_caf_sbnd |
| BNB + Cosmics | MC2023Av | v09_75_02 | 199184 | reco1 | official_MCP2023Av2_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_gen_g4_detsim_reco1_sbnd | 
| --- | --- | --- | 189149 | reco2 | official_MCP2023Av2_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2023Av2_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2023Av2_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_reco2_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2023Av2_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_reco2_flat_caf_sbnd |
| BNB Nue + cosmics | MC2022A | v09_37_02_04 | 175000 | reco1 | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_intrnue_spill_gsimple-configh-v1_tpc_gen_g4_detsim_reco1_sbnd | 
| --- | --- | --- | --- | reco2 | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_intrnue_spill_gsimple-configh-v1_tpc_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_intrnue_spill_gsimple-configh-v1_tpc_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_intrnue_spill_gsimple-configh-v1_tpc_reco2_concat_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_intrnue_spill_gsimple-configh-v1_tpc_reco2_concat_flat_caf_sbnd |
| BNB Full Osc + cosmics | MC2022A | v09_37_02_04 | 175000 | reco1 | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_fullosc_spill_gsimple-configh-v1_tpc_gen_g4_detsim_reco1_sbnd | 
| --- | --- | --- | --- | reco2 | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_fullosc_spill_gsimple-configh-v1_tpc_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_fullosc_spill_gsimple-configh-v1_tpc_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_fullosc_spill_gsimple-configh-v1_tpc_reco2_concat_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_fullosc_spill_gsimple-configh-v1_tpc_reco2_concat_flat_caf_sbnd |
| In time cosmics | MC2022A | v09_37_02_04 | 380000 | reco1 | official_MCP2022A_prodcorsika_proton_intime_filter_sce_gen_g4_detsim_reco1_sbnd | 
| --- | --- | --- | --- | reco2 | official_MCP2022A_prodcorsika_proton_intime_filter_sce_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2022A_prodcorsika_proton_intime_filter_sce_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2022A_prodcorsika_proton_intime_filter_sce_reco2_concat_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2022A_prodcorsika_proton_intime_filter_sce_reco2_concat_flat_caf_sbnd |
| BNB nu+cosmics | MC2022A | v09_37_02_04 | 3500000 | reco1 | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_gen_g4_detsim_reco1_sbnd | 
| --- | --- | --- | --- | reco2 | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_reco2_concat_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_rockbox_sce_reco2_concat_flat_caf_sbnd |
| BNB nue+cosmics, raw | MC2022A | v09_37_02_04 | 10000 | reco1 | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_intrnue_spill_tpc_sbnd_gen_g4_detsim_reco1_sbnd | 
| --- | --- | --- | --- | reco2 | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_intrnue_spill_tpc_sbnd_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_intrnue_spill_tpc_sbnd_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_intrnue_spill_tpc_sbnd_reco2_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_intrnue_spill_tpc_sbnd_reco2_flat_caf_sbnd |
| BNB+cosmics, raw | MC2022A | v09_37_02_04 | 10000 | reco1 | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_nu_spill_tpc_sbnd_gen_g4_detsim_reco1_sbnd | 
| --- | --- | --- | --- | reco2 | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_nu_spill_tpc_sbnd_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_nu_spill_tpc_sbnd_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_nu_spill_tpc_sbnd_reco2_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2022A_prodoverlay_corsika_cosmics_proton_genie_nu_spill_tpc_sbnd_reco2_flat_caf_sbnd |
| NS-CRT crossing muon triggers, raw | MC2022A | v09_37_02_04 | 10000 | reco1 | official_MCP2022A_prodcorsika_cosmics_proton_frontbackcrt_mu_filter_gen_g4_detsim_reco1_sbnd | 
| --- | --- | --- | --- | reco2 | official_MCP2022A_prodcorsika_cosmics_proton_frontbackcrt_mu_filter_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2022A_prodcorsika_cosmics_proton_frontbackcrt_mu_filter_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2022A_prodcorsika_cosmics_proton_frontbackcrt_mu_filter_reco2_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2022A_prodcorsika_cosmics_proton_frontbackcrt_mu_filter_reco2_flat_caf_sbnd |
| EW-CRT crossing muon triggers, raw | MC2022A | v09_37_02_04 | 10000 | reco1 | official_MCP2022A_prodcorsika_cosmics_proton_eastwestcrt_mu_filter_gen_g4_detsim_reco1_sbnd | 
| --- | --- | --- | --- | reco2 | official_MCP2022A_prodcorsika_cosmics_proton_eastwestcrt_mu_filter_reco2_sbnd |
| --- | --- | --- | --- | calib tuple | hist_official_MCP2022A_prodcorsika_cosmics_proton_eastwestcrt_mu_filter_reco2_sbnd |
| --- | --- | --- | --- | caf | official_MCP2022A_prodcorsika_cosmics_proton_eastwestcrt_mu_filter_reco2_caf_sbnd |
| --- | --- | --- | --- | flatcaf | official_MCP2022A_prodcorsika_cosmics_proton_eastwestcrt_mu_filter_reco2_flat_caf_sbnd |
| BNB nue + cosmic | MC2021Bv1 | v09_28_01_02 | 15000 | reco2 | official_MC2021Bv1_prodoverlay_corsika_cosmics_proton_genie_nu_spill_gsimple-configh-v1_tpc_reco2_sbnd | 
| --- | --- | --- | 14800 | flat caf | official_MC2021Bv1_prodoverlay_corsika_cosmics_proton_genie_nu_spill_gsimple-configh-v1_tpc_reco2_flat_caf_sbnd |
| BNB nue + cosmic | MC2021Bv1 | v09_28_01_02 | 15000 | reco1 | official_MC2021Bv1_prodoverlay_corsika_cosmics_proton_genie_intrnue_spill_gsimple-configh-v1_tpc_gen_g4_detsim_reco1_sbnd | 
| --- | --- | --- | 15000 | reco2 | official_MC2021Bv1_prodoverlay_corsika_cosmics_proton_genie_nu_spill_gsimple-configh-v1_tpc_reco2_sbnd | 
| --- | --- | --- |  15000 | caf | official_MC2021Bv1_prodoverlay_corsika_cosmics_proton_genie_nu_spill_gsimple-configh-v1_tpc_reco2_caf_sbnd | 
| BNB full osc + cosmics | MC2021Bv1 | v09_28_01_02 | --- | reco1 | test15_official_test15_MC2021Bv1_prodoverlay_corsika_cosmics_proton_genie_fullosc_spill_gsimple-configh-v1_tpc_reco1_sbnd | 
| --- | --- | --- | --- | reco2 | test_official_test_MC2021Bv1_prodoverlay_corsika_cosmics_proton_genie_fullosc_spill_gsimple-configh-v1_tpc_reco2_sbnd |
| --- | --- | --- | --- | caf | test_official_test_MC2021Bv1_prodoverlay_corsika_cosmics_proton_genie_fullosc_spill_gsimple-configh-v1_tpc_reco2_caf_sbnd |
| BNB nu + cosmic | MC2021Bv1 | v09_28_01_02 | --- | reco1 | official_MC2021Bv1_prodoverlay_corsika_cosmics_proton_genie_nu_spill_gsimple-configh-v1_tpc_reco1_sbnd | 
| --- | --- | --- | --- | reco2 | test100_official_test100_MC2021Bv1_prodoverlay_corsika_cosmics_proton_genie_nu_spill_gsimple-configh-v1_tpc_reco2_sbnd | 
| --- | --- | --- | --- | caf | test100_official_test100_MC2021Bv1_prodoverlay_corsika_cosmics_proton_genie_nu_spill_gsimple-configh-v1_tpc_reco2_caf_sbnd | 
| in time cosmics, with SCE | MCP2021A | v09_26_00 | --- | reco2 | official_MCP2021A_prodoverlay_corsika_cosmics_proton_genie_nu_spill_tpc_sbnd_reco2_sbnd | 
| --- | --- | v09_28_00 | 1144 | concat caf | official_MCP2021A_CAF_prodcorsika_proton_intime_filter_sc_concat_caf_sbnd |
| BNB neutrinos + cosmics, with SCE | MCP2021A | v09_26_00 | --- | reco2 | official_MCP2021A_prodgenie_nu_singleinteraction_tpc_sbnd_reco2_sbnd | 
| --- | --- | v09_28_00 | 185300 | flat caf | official_MCP2021A_CAF_prodoverlay_corsika_cosmics_proton_genie_nu_spill_tpc_sbnd_flat_caf_sbnd | 
| BNB nu only, with SCE | MCP2021A | v09_26_00 | --- | reco2 | official_MCP2021A_prodcorsika_proton_intime_filter_sce_reco2_sbnd | 
| --- | --- | v09_28_00 | 150000 | concat caf | official_MCP2021A_CAF_prodgenie_nu_singleinteraction_tpc_sbnd_concat_caf_sbnd	| 
| Intime Cosmics | SBNWorkshop0421 | v09_19_00_02 | 150627 | flat cafs | 	workshop_SBNWorkshop0421_prodcorsika_proton_intime_filter_flat_caf_sbnd	|
| NuE Overlay | SBNWorkshop0421 | v09_19_00_01 | 45700 | flat cafs | 	workshop_SBNWorkshop0421_prodoverlay_corsika_cosmics_proton_genie_intrnue_spill_gsimple-configf-v1_tpc_flat_caf_sbnd |
| BNB Overlay | SBNWorkshop0421 | v09_19_00_01 | 286850 | flat cafs | workshop_SBNWorkshop0421_prodoverlay_corsika_cosmics_proton_genie_nu_spill_gsimple-configf-v1_tpc_flat_caf_sbnd | 
| Intime cosmics | MCP2020A | v09_09_00 | 151407 | reco2 | official_MCP2020A_prodcorsika_proton_intime_filter_reco2_sbnd	|
| BNBnue | MCP2020A | v09_09_00 | 72300 | reco2 | official_MCP2020A_prodgenie_intrnue_singleinteraction_tpc_gsimple-configf-v1_reco2_sbnd	|
| BNBnue + cosmics | MCP2020A | v09_09_00 | 45950 | reco2 | official_MCP2020A_prodoverlay_corsika_cosmics_proton_genie_intrnue_spill_gsimple-configf-v1_tpc-configf-v1_tpc_reco2_sbnd | 
| BNB nu + cosmics | MCP2020A | v09_09_00 | 287350 | reco2 | official_MCP2020A_prodoverlay_corsika_cosmics_proton_genie_nu_spill_gsimple-configf-v1_tpc-configf-v1_tpc_reco2_sbnd	|
| Cathode crossing muons | MCP2020A | v09_08_00 | 9700 | detsim | official_MCP2020A_prodsingle_mu_10GeV_cathodecrossing_detsim_sbnd |
| low energy electrons | MCP2020A | v09_08_00 | 19000 | detsim | official_MCP2020A_prodsingle_electron_1-50MeV_detsim_sbnd |
| Stopping muons from top | MCP2020A | v09_08_00 | 9500 | detsim | official_MCP2020A_prodsingle_muplus_stopping_fromtop_detsim_sbnd |
| BNB nu (single interaction) | MCP2020A | v09_09_00 | 198400 | reco2 | official_MCP2020A_prodgenie_nu_singleinteraction_tpc_gsimple-configf-v1_reco2_sbnd |


ICARUS MC
--------------------------

| Sample Description | production push | release version | # Events | Sample type | Samweb definition |   
| --- | --- | --- | --- | --- | --- |
| BNB + Intime Cosmics (1d convolution) | MC2024A | v09_87_00 | --- | calibtuple |  prodcorsika_proton_intime_icarus_bnb_sce_1d_drift_on_MC-v09_87_00-042024-cnaf
| --- | --- | --- | --- | caf |  prodcorsika_proton_intime_icarus_bnb_sce_1d_drift_on_MC-v09_87_00-042024-cnaf
| --- | --- | --- | --- | flatcaf |  prodcorsika_proton_intime_icarus_bnb_sce_1d_drift_on_MC-v09_87_00-042024-cnaf
| BNB + Cosmics (1d convolution) | MC2024A | v09_84_00_01 | --- | calibtuple |  mc-v09_84_00_01-202403-cnaf-corrsce
| --- | --- | --- | --- | caf |  mc-v09_84_00_01-202403-cnaf-corrsce
| --- | --- | --- | --- | flatcaf |  mc-v09_84_00_01-202403-cnaf-corrsce
| BNB + Intime Cosmics (2d deconvolution validation) | MC2024A | v09_83_01 | 24851 | calibtuple |  icaruspro_production_v09_83_01_2024A_ICARUS_BNB_Intime_Cosmics_MC_2024_BNB_MC_calibtuple |
| --- | --- | --- | --- | caf | icaruspro_production_v09_83_01_2024A_ICARUS_BNB_Intime_Cosmics_MC_2024_BNB_MC_caf |
| --- | --- | --- | --- | flatcaf | icaruspro_production_v09_83_01_2024A_ICARUS_BNB_Intime_Cosmics_MC_2024_BNB_MC_flatcaf |
| NuMI Dirt + Cosmic | MC2023A | v09_72_00_03 | 211500 | reco2 |  icaruspro_v09_72_00_03_2023A_ICARUS_NuMI_MC_dirt_plus_cosmics_pretuned_signal_shape_stage1 |
| --- | --- | --- | --- | calibtuple |  icaruspro_production_v09_72_00_03_2023A_ICARUS_NuMI_MC_dirt_plus_cosmics_pretuned_signal_shape_calibtuple |
| --- | --- | --- | --- | caf | icaruspro_production_v09_72_00_03_2023A_ICARUS_NuMI_MC_dirt_plus_cosmics_pretuned_signal_shape_caf |
| --- | --- | --- | --- | flatcaf | icaruspro_production_v09_72_00_03_2023A_ICARUS_NuMI_MC_dirt_plus_cosmics_pretuned_signal_shape_flatcaf |
| NuMI Intime Cosmic | MC2023A | v09_72_00_03 | 200375 | reco2 | icaruspro_v09_72_00_03_2023A_ICARUS_NuMI_MC_intime_cosmics_pretuned_signal_shape_stage1 |
| --- | --- | --- | --- | calibtuple |  icaruspro_production_v09_72_00_03_2023A_ICARUS_NuMI_MC_intime_cosmics_pretuned_signal_shape_calibtuple |
| --- | --- | --- | --- | caf | icaruspro_production_v09_72_00_03_2023A_ICARUS_NuMI_MC_intime_cosmics_pretuned_signal_shape_caf |
| --- | --- | --- | --- | flatcaf | icaruspro_production_v09_72_00_03_2023A_ICARUS_NuMI_MC_intime_cosmics_pretuned_signal_shape_flatcaf |
| NuMI Neutrino MC Phase 1 | MC2023A | v09_72_00_03 | 586890 | reco2 | icaruspro_v09_72_00_03_2023A_ICARUS_NuMI_MC_Nu_Phase1_sample_pretuned_signal_shape_stage1 |
| --- | --- | --- | --- | calibtuple |  icaruspro_production_v09_72_00_03_2023A_ICARUS_NuMI_MC_Nu_Phase1_sample_pretuned_signal_shape_calibtuple |
| --- | --- | --- | --- | caf | icaruspro_production_v09_72_00_03_2023A_ICARUS_NuMI_MC_Nu_Phase1_sample_pretuned_signal_shape_caf |
| --- | --- | --- | --- | flatcaf | icaruspro_production_v09_72_00_03_2023A_ICARUS_NuMI_MC_Nu_Phase1_sample_pretuned_signal_shape_flatcaf |
| ICARUS BNB Mini Production intime cosmics | MC2023A | v09_72_00_01 | 90093 | reco2 |  icaruspro_2023A_ICARUS_BNB_cosmics_reco2 |
| --- | --- | --- | --- | calibtuple | icaruspro_hists_2023A_ICARUS_BNB_cosmics_reco2 |
| --- | --- | --- | --- | caf | icaruspro_2023A_ICARUS_BNB_cosmics_caf |
| --- | --- | --- | --- | flatcaf | icaruspro_2023A_ICARUS_BNB_cosmics_flatcaf | 
| ICARUS BNB Mini Production | MC2023A | v09_69_01 | 94980 | reco2 |  icaruspro_2023A_ICARUS_BNB_cosmics_reco2 |
| --- | --- | --- | --- | calibtuple | icaruspro_hists_2023A_ICARUS_BNB_cosmics_reco2 |
| --- | --- | --- | --- | caf | icaruspro_2023A_ICARUS_NuMI_MC_flatcaf_2023Mar10 |
| --- | --- | --- | --- | flatcaf | icaruspro_2023A_ICARUS_NuMI_MC_flatcaf_2023Mar10 |
| NuMI Neutrino Mini Production | MC2023A | v09_68_00_01 | 74600 | reco2 | icaruspro_2023A_ICARUS_NuMI_MC_stage1_2023Mar10 |
| --- | --- | --- | --- | calibtuples | icaruspro_2023A_ICARUS_NuMI_MC_caf_2023Mar10 |
| --- | --- | --- | --- | caf | icaruspro_2023A_ICARUS_NuMI_MC_caf_2023Mar10 |
| --- | --- | --- | --- | flatcaf | icaruspro_2023A_ICARUS_NuMI_MC_flatcaf_2023Mar10 |
| NuMI in-time cosmics w/Overburden | MC2022A | v09_37_02_04 | 809054 | reco2 | IcarusProd_2022A_NUMI_in-time_Cosmics_withOverburden_v09_37_02_04_reco2 |
| --- | --- | --- | --- | calibtuples |  IcarusProd_2022A_NUMI_in-time_Cosmics_withOverburden_v09_37_02_04_calibtuples |
| --- | --- | --- | --- | caf | IcarusProd_2022A_NUMI_in-time_Cosmics_withOverburden_v09_37_02_07_caf |
| --- | --- | --- | --- | flatcaf | IcarusProd_2022A_NUMI_in-time_Cosmics_withOverburden_v09_37_02_07_flatcaf |
| ICARUS_numi_higgs_M200_th2e-4_KDIF | MC2022A | v09_37_02_05 | 77950 | reco2 | IcarusProd_2022A_ICARUS_numi_higgs_M200_th2e-4_KDIF_reco2 |
| --- | --- | --- | 77950 | caf | IcarusProd_2022A_ICARUS_numi_higgs_M200_th2e-4_KDIF_caf |
| --- | --- | --- | 77950 | flatcaf | IcarusProd_2022A_ICARUS_numi_higgs_M200_th2e-4_KDIF_flatcaf |
| ICARUS_numi_higgs_M150_th2e-4_KDIF | MC2022A | v09_37_02_05 | 56300 | reco2 | IcarusProd_2022A_ICARUS_numi_higgs_M150_th2e-4_KDIF_reco2 |
| --- | --- | --- | 56300 | caf | IcarusProd_2022A_ICARUS_numi_higgs_M150_th2e-4_KDIF_caf |
| --- | --- | --- | 56300 | flatcaf | IcarusProd_2022A_ICARUS_numi_higgs_M150_th2e-4_KDIF_flatcaf |
| ICARUS_numi_higgs_M100_th2e-4_KDIF | MC2022A | v09_37_02_05 | 111100 | reco2 | IcarusProd_2022A_ICARUS_numi_higgs_M100_th2e-4_KDIF_reco2 |
| --- | --- | --- | 110900 | caf | IcarusProd_2022A_ICARUS_numi_higgs_M100_th2e-4_KDIF_caf |
| --- | --- | --- | 110900 | flatcaf | IcarusProd_2022A_ICARUS_numi_higgs_M100_th2e-4_KDIF_flatcaf |
| ICARUS_numi_higgs_M050_th2e-4_KDIF | MC2022A | v09_37_02_05 | 59850 | reco2 | IcarusProd_2022A_ICARUS_numi_higgs_M050_th2e-4_KDIF_reco2 |
| --- | --- | --- | 59750 | caf | IcarusProd_2022A_ICARUS_numi_higgs_M050_th2e-4_KDIF_caf |
| --- | --- | --- | 59750 | flatcaf | IcarusProd_2022A_ICARUS_numi_higgs_M050_th2e-4_KDIF_flatcaf |
| ICARUS intime cosmics 1D drift simulation waveform files | MC2022A | v09_51_00 | 217,332 | reco2 | IcarusProd_2022A_Intime_Cosmic_WF_v09_51_00_reco2 | 
| --- | --- | --- | 204,630 | calib tuple | IcarusProd_2022A_Intime_Cosmic_WF_v09_51_00_calibtuples |
| NUMI in-time cosmics with Overburden | MC2022A | v09_37_02_04 | 809,054 | reco2 | IcarusProd_2022A_NUMI_in-time_Cosmics_withOverburden_v09_37_02_04_reco2 | 
| --- | --- | --- | --- | calib tuple | IcarusProd_2022A_NUMI_in-time_Cosmics_withOverburden_v09_37_02_04_calibtuples |
| --- | --- | v09_37_02_07 | 809,054 | caf | IcarusProd_2022A_NUMI_in-time_Cosmics_withOverburden_v09_37_02_07_caf |
| --- | --- | --- | --- | flatcaf | IcarusProd_2022A_NUMI_in-time_Cosmics_withOverburden_v09_37_02_07_flatcaf |
| NUMI in-time cosmics without Overburden | MC2022A | v09_37_02_04 | 1,441,943 | reco2 | IcarusProd_2022A_NUMI_in-time_Cosmics_v09_37_02_04_reco2 | 
| --- | --- | --- | --- | calib tuple | IcarusProd_2022A_NUMI_in-time_Cosmics_v09_37_02_04_calibtuples |
| --- | --- | v09_37_02_07 | 1,443,061 | caf | IcarusProd_2022A_NUMI_in-time_Cosmics_v09_37_02_07_caf |
| --- | --- | --- | --- | flatcaf | IcarusProd_2022A_NUMI_in-time_Cosmics_v09_37_02_07_flatcaf |
| BNB in-time cosmics with Overburden | MC2022A | v09_37_02_04 | 1,909,017 | reco2 | IcarusProd_2022A_BNB_in-time_Cosmics_v09_37_02_04_reco2 | 
| --- | --- | --- | --- | calib tuple | IcarusProd_2022A_BNB_in-time_Cosmics_v09_37_02_04_calibtuples |
| --- | --- | v09_37_02_07 | 1,909,017 | caf | IcarusProd_2022A_BNB_in-time_Cosmics_v09_37_02_07_caf |
| --- | --- | --- | --- | flatcaf | IcarusProd_2022A_BNB_in-time_Cosmics_v09_37_02_07_flatcaf |
| nu+cosmics w/Overburden | MC2022A | v09_37_02_04 | 437044 | reco1 | IcarusProd2022A_icarus_BNB_Nu_Cosmics_v09_37_02_04_reco1 |
| --- | --- | --- | --- | reco2 | IcarusProd2022A_icarus_BNB_Nu_Cosmics_v09_37_02_04_reco2 |
| --- | --- | --- | --- | calib tuples | hist_IcarusProd2022A_icarus_BNB_Nu_Cosmics_v09_37_02_04_reco2 |
| --- | --- | --- | 346060 | caf | IcarusProd2022A_icarus_BNB_Nu_Cosmics_v09_37_02_04_caf |
| --- | --- | --- | --- | flatcaf | IcarusProd2022A_icarus_BNB_Nu_Cosmics_v09_37_02_04_flatcaf |
| NuMI nu+cosmics w/o Overburden | MC2022A | v09_37_02_04 | --- | reco1 | IcarusProd2022A_icarus_numi_nu_cosmics_v09_37_02_04_reco1 |
| --- | --- | --- | --- | reco2 | IcarusProd2022A_icarus_numi_nu_cosmics_v09_37_02_04_reco2 |
| --- | --- | --- | 628249 | caf | IcarusProd2022A_icarus_numi_nu_cosmics_v09_37_02_04_caf |
| BNB fullosc+cosmics w/Overburden | MC2022A | v09_37_02_04 | --- | reco1 | IcarusProd_2022A_BNB_FullOsc_Cosmics_v09_37_02_04_reco1 |
| --- | --- | --- | --- | reco2 | IcarusProd_2022A_BNB_FullOsc_Cosmics_v09_37_02_04_reco2 |
| --- | --- | --- | 194 | caf | IcarusProd_2022A_BNB_FullOsc_Cosmics_v09_37_02_04_caf |
| BNB nue+cosmics w/Overburden | MC2022A | v09_37_02_04 | --- | reco1 | IcarusProd_2022A_BNB_Nue_Cosmics_v09_37_02_04_reco1 |
| --- | --- | --- | --- | reco2 | IcarusProd_2022A_BNB_Nue_Cosmics_v09_37_02_04_reco2 |
| --- | --- | --- | 200 | caf | IcarusProd_2022A_BNB_Nue_Cosmics_v09_37_02_04_caf |
| NuMI full-osc+cosmics w/o Overburden | MC2022A | v09_37_02_04 | --- | reco1 | IcarusProd_2022A_NuMI_FullOsc_Cosmics_v09_37_02_04_reco1 |
| --- | --- | --- | --- | reco2 | IcarusProd_2022A_NuMI_FullOsc_Cosmics_v09_37_02_04_reco2 |
| --- | --- | --- | 3724 | caf | IcarusProd_2022A_NuMI_FullOsc_Cosmics_v09_37_02_04_caf |
| NuMI nue+cosmics w/o Overburden | MC2022A | v09_37_02_04 | --- | reco1 | IcarusProd_2022A_NuMI_Nue_Cosmics_v09_37_02_04_reco1 |
| --- | --- | --- | --- | reco2 | IcarusProd_2022A_NuMI_Nue_Cosmics_v09_37_02_04_reco2 |
| --- | --- | --- | 3554 | caf | IcarusProd_2022A_NuMI_Nue_Cosmics_v09_37_02_04_caf |
| Cosmics, Lifetime 3.5 ms, No SCE  | MCP2021C | v09_37_01_03p01 | 24400 | reco2 | IcarusProd_PuritySample_eLifetime3.5ms_NoSCE_v09_37_01_03p01_reco2 |
| --- | --- | --- | --- | calib ntuples | IcarusProd_PuritySample_eLifetime3.5ms_NoSCE_v09_37_01_03p01_calibtuples |
| Cosmics, Lifetime 6 ms, No SCE  | MCP2021C | v09_37_01_03p01 | 24400 | reco2 | IcarusProd_PuritySample_eLifetime6ms_NoSCE_v09_37_01_03p01_reco2 |
| --- | --- | --- | --- | calib ntuples | IcarusProd_PuritySample_eLifetime6ms_NoSCE_v09_37_01_03p01_calibtuples |
| Cosmics, Lifetime 3.5 ms, No Diffusion  | MCP2021C | v09_37_01_03p01 | 20925 | reco2 | IcarusProd_PuritySample_eLifetime3.5ms_NoDiffusion_v09_37_01_03p01_reco2 |
| --- | --- | --- | --- | calib ntuples | IcarusProd_PuritySample_eLifetime3.5ms_NoDiffusion_v09_37_01_03p01_calibtuples |
| Cosmics, Lifetime 6 ms, No Diffusion  | MCP2021C | v09_37_01_03p01 | 20750 | reco2 | IcarusProd_PuritySample_eLifetime6ms_NoDiffusion_v09_37_01_03p01_reco2 |
| --- | --- | --- | --- | calib ntuples | IcarusProd_PuritySample_eLifetime6ms_NoDiffusion_v09_37_01_03p01_calibtuples |
| Cosmics, Lifetime 3.5 ms, No SCE No Diffusion | MCP2021C | v09_37_01_03p01 | 21125 | reco2 | IcarusProd_PuritySample_eLifetime3.5ms_NoSCE_NoDiffusion_v09_37_01_03p01_reco2 |
| --- | --- | --- | --- | calib ntuples | IcarusProd_PuritySample_eLifetime3.5ms_NoSCE_NoDiffusion_v09_37_01_03p01_calibtuples |
| Cosmics, Lifetime 6 ms, No SCE No Diffusion | MCP2021C | v09_37_01_03p01 | 20600 | reco2 | IcarusProd_PuritySample_eLifetime6ms_NoSCE_NoDiffusion_v09_37_01_03p01_reco2 |
| --- | --- | --- | --- | calib ntuples | IcarusProd_PuritySample_eLifetime6ms_NoSCE_NoDiffusion_v09_37_01_03p01_calibtuples |
| Cosmics, Lifetime 1 ms  | MCP2021C | v09_37_01_03p01 | 20200 | reco2 | IcarusProd_PuritySample_eLifetime1ms_v09_37_01_03p01_reco2_commonruns |
| --- | --- | --- | --- | calib ntuples | IcarusProd_PuritySample_eLifetime1ms_v09_37_01_03p01_calibtuples_commonruns |
| Cosmics, Lifetime 3.5 ms  | MCP2021C | v09_37_01_03p01 | 20200 | reco2 | IcarusProd_PuritySample_eLifetime3.5ms_v09_37_01_03p01_reco2_commonruns |
| --- | --- | --- | --- | calib ntuples | IcarusProd_PuritySample_eLifetime3.5ms_v09_37_01_03p01_calibtuples_commonruns |
| Cosmics, Lifetime 6 ms  | MCP2021C | v09_37_01_03p01 | 20200 | reco2 | IcarusProd_PuritySample_eLifetime6ms_v09_37_01_03p01_reco2_commonruns |
| --- | --- | --- | --- | calib ntuples | IcarusProd_PuritySample_eLifetime6ms_v09_37_01_03p01_calibtuples_commonruns |
| Cosmics, Lifetime 10 ms  | MCP2021C | v09_37_01_03p01 | 20200 | reco2 | IcarusProd_PuritySample_eLifetime10ms_v09_37_01_03p01_reco2_commonruns |
| --- | --- | --- | --- | calib ntuples | IcarusProd_PuritySample_eLifetime10ms_v09_37_01_03p01_calibtuples_commonruns |
| NuMI nue + cosmics | MCP2021C | v09_37_01_02p01 | 13326 | reco1 | Official_IcarusProd2021C_NUMI_Nue_Cosmics_v09_37_01_02p01_reco1 |
| --- | --- | --- | 13326 | reco2 | Official_IcarusProd2021C_NUMI_Nue_Cosmics_v09_37_01_02p01_reco2 |
| --- | --- | --- | --- | calib ntuples | Official_IcarusProd2021C_NUMI_Nue_Cosmics_v09_37_01_02p01_CalibTuples |
| --- | --- | v09_37_01_03p01 | 13326 | caf |Official_IcarusProd2021C_NUMI_Nue_Cosmics_v09_37_01_03p01_caf |
| NuMI nu + cosmic | MCP2021C | v09_37_01_02p01 | 48487 | reco1 | Official_IcarusProd2021C_NUMI_Nu_Cosmics_v09_37_01_02p01_reco1 |
| --- | --- | --- | 48459 | reco2 | Official_IcarusProd2021C_NUMI_Nu_Cosmics_v09_37_01_02p01_reco2 |
| --- | --- | --- | --- | calib ntuples | Official_IcarusProd2021C_NUMI_Nu_Cosmics_v09_37_01_02p01_CalibTuples |
| --- | --- | v09_37_01_03p01 | 48459 | caf | Official_IcarusProd2021C_NUMI_Nu_Cosmics_v09_37_01_03p01_caf |
| NUMI full osc | MCP2021C | v09_37_01_02p01 | 16565 | reco1 | Official_IcarusProd2021C_NUMI_FullOsc_Cosmics_v09_37_01_02p01_reco1 |
| --- | --- | --- | 16564 | reco2 | Official_IcarusProd2021C_NUMI_FullOsc_Cosmics_v09_37_01_02p01_reco2 |
| --- | --- | --- | --- | calib ntuples | Official_IcarusProd2021C_NUMI_FullOsc_Cosmics_v09_37_01_02p01_CalibTuples |
| --- | --- | v09_37_01_03p01 | 16564 | caf | Official_IcarusProd2021C_NUMI_FullOsc_Cosmics_v09_37_01_03p01_caf |
| NUMI Intime Cosmics | MCP2021C | v09_37_01_02p01 | 350794 | reco1 | Official_IcarusProd2021C_NUMI_in-time_Cosmics_v09_37_01_02p01_reco1 |
| --- | --- | --- | 350554 | reco2 | Official_IcarusProd2021C_NUMI_in-time_Cosmics_v09_37_01_02p01_reco2 |
| --- | --- | --- | --- | calib ntuples | Official_IcarusProd2021C_NUMI_in-time_Cosmics_v09_37_01_02p01_CalibTuples |
| --- | --- | v09_37_01_03p01 | 350554 | caf | Official_IcarusProd2021C_NUMI_in-time_Cosmics_v09_37_01_03p01_caf |
| BNB nue + cosmic | MCP2021C | v09_37_01_02p01 | 2549 | reco1 | Official_IcarusProd2021C_BNB_Nue_Cosmics_v09_37_01_02p01_reco1 |
| --- | --- | --- | 2549 | reco2 | Official_IcarusProd2021C_BNB_Nue_Cosmics_v09_37_01_02p01_reco2 |
| --- | --- | --- | --- | calib ntuples | Official_IcarusProd2021C_BNB_Nue_Cosmics_v09_37_01_02p01_CalibTuples |
| --- | --- | v09_37_01_03p01 | 2549 | caf | Official_IcarusProd2021C_BNB_Nue_Cosmics_v09_37_01_03p01_caf |
| BNB nu + cosmics |MCP2021C | v09_37_01_02p01 | 34800 | reco1 | Official_IcarusProd2021C_BNB_Nu_Cosmics_v09_37_01_02p01_reco1 |
| --- | --- | --- | 34770 | reco2 | Official_IcarusProd2021C_BNB_Nu_Cosmics_v09_37_01_02p01_reco2 |
| --- | --- | --- | --- | calib ntuples | Official_IcarusProd2021C_BNB_Nu_Cosmics_v09_37_01_02p01_CalibTuples |
| --- | --- | v09_37_01_03p01 | 34770 | caf | Official_IcarusProd2021C_BNB_Nu_Cosmics_v09_37_01_03p01_caf |
| BNB full osc | MCP2021C | v09_37_01_02p01 | 2146 | reco1 | Official_IcarusProd2021C_BNB_FullOsc_Cosmics_v09_37_01_02p01_reco1 |
| --- | --- | --- | 2129 | reco2 | Official_IcarusProd2021C_BNB_FullOsc_Cosmics_v09_37_01_02p01_reco2 |
| --- | --- | --- | --- | calib ntuples | Official_IcarusProd2021C_BNB_FullOsc_Cosmics_v09_37_01_02p01_CalibTuples |
| --- | --- | v09_37_01_03p01 | 2129 | caf | Official_IcarusProd2021C_BNB_FullOsc_Cosmics_v09_37_01_03p01_caf |
| BNB Intime Cosmics | MCP2021C | v09_37_01_02p01 | 339541 | reco1 | Official_IcarusProd2021C_BNB_in-time_Cosmics_v09_37_01_02p01_reco1 |
| --- | --- | --- | 339305 | reco2 | Official_IcarusProd2021C_BNB_in-time_Cosmics_v09_37_01_02p01_reco2 |
| --- | --- | --- | --- | calib ntuples | Official_IcarusProd2021C_BNB_in-time_Cosmics_v09_37_01_02p01_CalibTuples |
| --- | --- | v09_37_01_03p01 | 339257 | caf | Official_IcarusProd2021C_BNB_in-time_Cosmics_v09_37_01_03p01_caf |
| NuMI nue + cosmics | MCP2021B | v09_28_01_01_01 | 10020 | reco2 | IcarusProd2021B_NuMI_Nue_Cosmics_v09_28_01_01_01_reco2 |
| --- | --- | --- | --- | calib ntuples | IcarusProd2021B_NuMI_Nue_Cosmics_v09_28_01_01_01_CalibTuples |
| --- | --- | --- | 10020 | caf |IcarusProd2021B_NuMI_Nue_Cosmics_v09_28_01_01_01_caf |
| NuMI + cosmic | MCP2021B | v09_28_01_01_01 | 60278 | reco1 | IcarusProd2021B_NuMI_Nu_Cosmics_v09_28_01_01_01_reco1 |
| --- | --- | --- | 59625 | reco2 | IcarusProd2021B_NuMI_Nu_Cosmics_v09_28_01_01_01_reco2 |
| --- | --- | --- | --- | calib ntuples | IcarusProd2021B_NuMI_Nu_Cosmics_v09_28_01_01_01_CalibTuples |
| --- | --- | --- | 59625 | caf | IcarusProd2021B_NuMI_Nu_Cosmics_v09_28_01_01_01_caf |
| BNB nue + cosmic | MCP2021B | v09_28_01_01_01 | 16598 | reco1 | IcarusProd2021B_BNB_Nue_Cosmics_v09_28_01_01_01_reco1 |
| --- | --- | --- | 15471 | reco2 | IcarusProd2021B_BNB_Nue_Cosmics_v09_28_01_01_01_reco2 |
| --- | --- | --- | --- | calib ntuples | IcarusProd2021B_BNB_Nue_Cosmics_v09_28_01_01_01_CalibTuples |
| --- | --- | --- | 15471 | caf | IcarusProd2021B_BNB_Nue_Cosmics_v09_28_01_01_01_caf |
| BNB full osc | MCP2021B | v09_28_01_01_01 | 16091 | reco1 | IcarusProd2021B_BNB_FullOsc_Cosmics_v09_28_01_01_01_reco1 |
| --- | --- | --- | 15960 | reco2 | IcarusProd2021B_BNB_FullOsc_Cosmics_v09_28_01_01_01_reco2 |
| --- | --- | --- | --- | calib ntuples | IcarusProd2021B_BNB_FullOsc_Cosmics_v09_28_01_01_01_CalibTuples |
| --- | --- | --- | 9048 | caf | IcarusProd2021B_BNB_FullOsc_Cosmics_v09_28_01_01_01_caf |
| Intime Cosmics | MCP2021B | v09_28_01_01_01 | 50479 | reco1 | IcarusProd2021B_Intime_Cosmic_v09_28_01_01_01_reco1 |
| --- | --- | --- | 50452 | reco2 | IcarusProd2021B_Intime_Cosmic_v09_28_01_01_01_reco2 |
| --- | --- | --- | --- | calib ntuples | IcarusProd2021B_Intime_Cosmic_v09_28_01_01_01_CalibTuples |
| --- | --- | --- | 50452 | caf | IcarusProd2021B_Intime_Cosmic_v09_28_01_01_01_caf |
| BNB nu + cosmics | MCP2021B | v09_28_01_01_01 | 51827 | reco1 | IcarusProd2021B_BNB_Nu_Cosmics_v09_28_01_01_01_reco1 |
| --- | --- | --- | 50478 | reco2 | IcarusProd2021B_BNB_Nu_Cosmics_v09_28_01_01_01_reco2 |
| --- | --- | --- | --- | calib ntuples | IcarusProd2021B_BNB_Nu_Cosmics_v09_28_01_01_01_CalibTuples |
| --- | --- | --- | 49872 | caf | IcarusProd2021B_BNB_Nu_Cosmics_v09_28_01_01_01_caf |
| Intime cosmics with overburden | MCP2021A | v09_27_00_02 | 32525 | reco2 | ICARUS_prod_2021A_00_nu_outoftime_ovb_v09_27_00_02 |
| Nu + Cosmics Overburden | MCP2021A | v09_27_00_02 | 31489 | reco2 | ICARUS_prod_2021A_00_intime_outoftime_ovb_v09_27_00_02	|
| intime cosmics | MCP2020A | v09_17_00 | 14939 | detsim | ICARUS_event_selection_intime_cosmics_v09_17_00_detsim	|
| BNB Nu + intime cosmics | MCP2020A | v09_17_00 | 11175 | detsim | ICARUS_event_selection_BNB_NuPlus_intime_cosmics_v09_17_00_detsim	|
| Intime Cosmics | SBNWorkshop0421 | v09_19_00_02 | 112223 | caf | workshop_SBNWorkshop0421_prod_corsika_intime_cosmics-config_caf_icarus	|
| BNB Nue | SBNWorkshop0421 | v09_19_00_02 | 53250 | caf | workshop_SBNWorkshop0421_prodoverlay_corsika_cosmics_cosmics_proton_genie_intrnue_spill_gsimple-config_caf_icarus |
| BNB Nu | SBNWorkshop0421 | v09_19_00_02 | 162896 | caf | workshop_SBNWorkshop0421_prodoverlay_corsika_cosmics_cosmics_proton_genie_nu_spill_gsimple-config_caf_icarus	|
| BNB Nue + cosmics | MCP2020A | v09_17_01 | 9190 | reco2 | poms_icarus_bnb_nue_cosmic_v09_17_01_reco2	|
| --- | --- | --- | 8790 | caf | poms_icarus_bnb_nue_cosmic_v09_17_01_caf | 
| Numi off axis + cosmic | MCP2020A | v09_17_01 | 47425 | reco2 | icarus_numi_offaxis_cosmic_v09_17_01	|
| BNB nu-only | MCP2020A | v09_09_02_01 | 113302 | reco2 | poms_icarus_prod_2020A_00_BNB_nu_v09_09_02_01_reco2		|
| NuMI off axis for ICARUS | MCP2020A | v09_07_00_prof | 70790 | reco2 | ICARUS_prod_2020A_00_numioffaxis_v09_10_01_reco2	|
| COSMICs_ML | --- | v09_07_00_prof | 543700 | detsim | ICARUS_poms_prod_cosmics_ML_v09_07_00_detsim	|
| Intime cosmics | MCP2020A | v09_09_00 | 189534 | reco2 | ICARUS_prod_2020A_00_intime_cosmic_v09_09_00_reco2_halfstats	| 
| --- | --- | --- | 159538 | reco2SCEfix | ICARUS_prod_intime_cosmic_v09_09_02_01_reco2SCEfix | 
| BNB Nue + cosmics | MCP2020A | v09_09_00 | 58339 | reco2 | ICARUS_prod_2020A_00_BNB_nue_cosmic_v09_09_00_reco2	| 
| --- | --- | --- | 56514 | reco2SCEfix | ICARUS_prod_BNB_nue_cosmic_v09_09_02_01_reco2SCEfix | 
| BNB Nu + cosmics | MCP2020A | v09_09_00 | 189775 | reco2 | ICARUS_prod_2020A_00_BNB_nu_cosmic_v09_09_00_reco2_halfstats	|
| --- | --- | --- | 165816 | reco2SCEfix | ICARUS_prod_BNB_nu_cosmic_v09_09_02_01_reco2SCEfix | 
| BNB nue | MCP2020A | v09_09_00 | 50976 | reco2 | ICARUS_prod_2020A_00_BNB_nue_v09_09_00_reco2	| 
| --- | --- | --- | 51092 | reco2SCEfix | ICARUS_prod_BNB_nue_v09_09_02_01_reco2SCEfix | 
		

### Notes on samples ###
* MC2020A
  * SBND Intime Cosmic sample in MCP2020A (and possibly older productions)
    * bug in LArSoft can lead to issues where the best matching particle is non existent
    * more information: [DocDB:20894](https://sbn-docdb.fnal.gov/cgi-bin/private/ShowDocument?docid=20894) 

Data SBN Production Samples
--------------------------

ICARUS DATA
--------------------------

ICARUS Reconstructed DATA
--------------------------

### Notes on samples ###
* Run 1 reprocessing is the reprocessing of selected runs based on the good run list created by Gray and Minerba. Please refer to this docdb for the list of runs: https://sbn-docdb.fnal.gov/cgi-bin/sso/RetrieveFile?docid=25407&filename=ICARUS%20Data%20Re-Processing.pdf&version=1
* Run 1 batch 2 is the processing of run_number > 7621 and run_number < 8460 (before the update to the new DAQ configuration)
* Run 1 batch 3 is the processing of run_number >= 8460 and run_number < 8598 (after the update to the new DAQ configuration resulting in 8 new data stream: (offbeam) BNB/NuMI Majority/MinBias)

| Sample Description | production push | release version | # Events | Sample type | Samweb definition |    
| --- | --- | --- | --- | --- | --- | 
| Offbeam NuMI MinBias stream | Run 1 batch3 | v09_37_02_09 | 374836 | stage0 | IcarusProd_Run1_batch3_OffBeamNuMIMinBiasstream_stage0      |  
| --- | --- | --- | 374836 | stage1 | IcarusProd_Run1_batch3_OffBeamNuMIMinBiasstream_stage1 |
| Offbeam BNB MinBias stream | Run 1 batch3 | v09_37_02_09 | 741147 | stage0 | IcarusProd_Run1_batch3_OffBeamBNBMinBiasstream_stage0        | 
| --- | --- | --- | 741147 | stage1 | IcarusProd_Run1_batch3_OffBeamBNBMinBiasstream_stage1 |
| NuMI MinBias stream | Run 1 batch3 | v09_37_02_09 | 19566 | stage0 | IcarusProd_Run1_batch3_NuMIMinBiasstream_stage0     |  
| --- | --- | --- | 19566 | stage1 | IcarusProd_Run1_batch3_NuMIMinBiasstream_stage1 |
| BNB MinBias stream | Run 1 batch3 | v09_37_02_09 | 42680 | stage0 | IcarusProd_Run1_batch3_BNBMinBiasstream_stage0       | 
| --- | --- | --- | 42680 | stage1 | IcarusProd_Run1_batch3_BNBMinBiasstream_stage1 |            
| Offbeam NuMI Majority stream | Run 1 batch3 | v09_37_02_09 | 109510 | stage0 | IcarusProd_Run1_batch3_OffBeamNuMIMajoritystream_stage0      |       
| --- | --- | --- | 109510 | stage1 | IcarusProd_Run1_batch3_OffBeamNuMIMajoritystream_stage1 |
| Offbeam BNB Majority stream | Run 1 batch3 | v09_37_02_09 | 231169 | stage0 | IcarusProd_Run1_batch3_OffBeamBNBMajoritystream_stage0        | 
| --- | --- | --- | 231169 | stage1 | IcarusProd_Run1_batch3_OffBeamBNBMajoritystream_stage1 |
| NuMI Majority stream | Run 1 batch3 | v09_37_02_09 | 284336 | stage0 | IcarusProd_Run1_batch3_NuMIMajoritystream_stage0     |       
| --- | --- | --- | 284336 | stage1 | IcarusProd_Run1_batch3_NuMIMajoritystream_stage1 |
| BNB Majority stream | Run 1 batch3 | v09_37_02_09 | 368711 | stage0 | IcarusProd_Run1_batch3_BNBMajoritystream_stage0       | 
| --- | --- | --- | 368711 | stage1 | IcarusProd_Run1_batch3_BNBMajoritystream_stage1 |
| Offbeam NuMI stream | Run 1 batch2 | v09_37_02_03 | 102488 | stage0 | IcarusProd_Run1_batch2_OffBeamNuMIstream_stage0      |       
| --- | --- | --- | 102488 | stage1 | IcarusProd_Run1_batch2_OffBeamNuMIstream_stage1 |
| Offbeam BNB stream | Run 1 batch2 | v09_37_02_03 | 327855 | stage0 | IcarusProd_Run1_batch2_OffBeamBNBstream_stage0        | 
| --- | --- | --- | 327855 | stage1 | IcarusProd_Run1_batch2_OffBeamBNBstream_stage1 |
| NuMI stream | Run 1 batch2 | v09_37_02_03 | 200220 | stage0 | IcarusProd_Run1_batch2_NuMIstream_stage0     |       
| --- | --- | --- | 200220 | stage1 | IcarusProd_Run1_batch2_NuMIstream_stage1 |
| BNB stream | Run 1 batch2 | v09_37_02_03 | 935069 | stage0 | IcarusProd_Run1_batch2_BNBstream_stage0       | 
| --- | --- | --- | 935069 | stage1 | IcarusProd_Run1_batch2_BNBstream_stage1 |
| Offbeam NuMI stream | Run 1 reprocessing | v09_37_02_01 | 212809 | stage0 | IcarusProd_Run1_reprocess_OffBeamNuMIstream_stage0	| 
| --- | --- | --- | 212809 | stage1 | IcarusProd_Run1_reprocess_OffBeamNuMIstream_stage1 |
| Offbeam BNB stream | Run 1 reprocessing | v09_37_02_01 | 127768 | stage0 | IcarusProd_Run1_reprocess_OffBeamBNBstream_stage0	| 
| --- | --- | --- | 127768 | stage1 | IcarusProd_Run1_reprocess_OffBeamBNBstream_stage1 |
| NuMI stream | Run 1 reprocessing | v09_37_02_01 | 333097 | stage0 | IcarusProd_Run1_reprocess_NuMIstream_stage0	| 
| --- | --- | --- | 333097 | stage1 | IcarusProd_Run1_reprocess_NuMIstream_stage1 |
| BNB stream | Run 1 reprocessing | v09_37_02_01 | 627484 | stage0 | IcarusProd_Run1_reprocess_BNBstream_stage0	| 
| --- | --- | --- | 627484 | stage1 | IcarusProd_Run1_reprocess_BNBstream_stage1 |
| NuMI/BNB off/stream | Run 1 batch 3 | v09_72_00_05p03 | --- | stage1 | run1-v09_72_00_05p03-202311-cnaf
| ---| --- | --- | --- | caf | run1-v09_72_00_05p03-202311-cnaf
| BNB stream | Run 2 | v09_72_00_06 | --- | stage1 | run2-v09_72_00_06-202312-cnaf
| ---| --- | --- | --- | caf | run2-v09_72_00_06-202312-cnaf
| BNB stream | Run 9435 | v09_84_00_01 | --- | stage1 | run9435-v09_84_00_01-202403-cnaf
| ---| --- | --- | --- | stage0 | run9435-v09_84_00_01-202403-cnaf
| ---| --- | --- | --- | caf | run9435-v09_84_00_01-202403-cnaf
| BNB stream | Run 2 | v09_84_00_01 | --- | stage1 | run2-v09_84_00_01-202403-cnaf
| ---| --- | --- | --- | caf | run2-v09_84_00_01-202403-cnaf
