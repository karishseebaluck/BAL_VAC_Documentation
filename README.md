BAL Quasar Catalog for DESI Early Release Data
==============================================

#### Version: 1.0 

Description
-----------
This document describes the content of our BAL value added catalogs with updated redshifts for [DESI Fuji Early Data Release (EDR)](https://data.desi.lbl.gov/public/edr).
A more detailed explanation of the catalogs can be found in [Filbert et al. 2023](https://www.overleaf.com/read/gnvypxkmsdzs) (in preparation).

Files and Data Model
---------------------
The BAL catalogs with updated redshifts for Fuji (EDR) can be found at [https://data.desi.lbl.gov/public/edr/vac/bal-masked-redshift/fuji/v1.0](https://data.desi.lbl.gov/public/edr/vac/bal-masked-redshift/fuji/v1.0)

DESI Collaborators can access these files at /global/cfs/cdirs/desi/public/edr/vac/bal-masked-redshift/fuji/v1.0

The VAC files contain catalogs of BALs that have had their absorption features masked. The BALs were then run through Paul Martini's [baltools](https://github.com/paulmartini/baltools) to create the catalogs.

Our VAC file contains two catalogs which are described in more detail in the table below.

| File Name | File Size |  Number of QSOs  |
|:---------:|:---------:|------------------|
| QSO_cat_fuji_sv1_dark_bal_mask_v1.0.fits | 42.7 MB | 37,903 |
| QSO_cat_fuji_sv3_dark_bal_mask_v1.0.fits | 57.4 MB | 50,993 |

The table below contains descriptions of some of the columns in our catalogs.
| Column Name | # |  Description  |
|:-----------:|:-:|---------------|
| TARGETID | 0 | [Link](https://desidatamodel.readthedocs.io/en/latest/DESI_SPECTRO_REDUX/SPECPROD/tiles/GROUPTYPE/TILEID/GROUPID/qso_qn-SPECTROGRAPH-TILEID-GROUPID.html) |
| Z | 1 | Best fit redshift after masking |
| ZERR | 2 | Best fit redshift error post masking |
| ZWARN | 3 | Warning flags; 0 is good |
| SPECTYPE | 4 | Spectype from redrock file |
| COADD_FIBERSTATUS | 5 | bitwise-AND of input FIBERSTATUS |
| TARGET_RA | 6 | Target right ascension [degrees] |
| TARGET_DEC | 7 | Target declination [degrees] |
| MORPHTYPE | 8 | [Link](https://desidatamodel.readthedocs.io/en/latest/DESI_TARGET/TARG_DIR/DR/VERSION/targets/PHASE/RESOLVE/OBSCON/PHASEtargets-OBSCON-RESOLVE-hp-HP.html#hdu1) |
| EBV | 9 | [Link](https://desidatamodel.readthedocs.io/en/latest/DESI_TARGET/TARG_DIR/DR/VERSION/targets/PHASE/RESOLVE/OBSCON/PHASEtargets-OBSCON-RESOLVE-hp-HP.html#hdu1) |
| PROBA_RF | 25 | Probability of Random Forest selection |
| MASKBITS | 26 | [Link](https://desidatamodel.readthedocs.io/en/latest/DESI_TARGET/TARG_DIR/DR/VERSION/targets/PHASE/RESOLVE/OBSCON/PHASEtargets-OBSCON-RESOLVE-hp-HP.html#hdu1) |
| SV3_DESI_TARGET | 27 | DESI (dark time program) target selection bitmask for SV3 |
| SV3_SCND_TARGET | 28 | Secondary target selection bitmask for SV3 |
| DESI_TARGET | 29 | [Link](https://desidatamodel.readthedocs.io/en/latest/DESI_TARGET/TARG_DIR/DR/VERSION/targets/PHASE/RESOLVE/OBSCON/PHASEtargets-OBSCON-RESOLVE-hp-HP.html#hdu1) |
| COADD_NUMEXP | 30 | Number of exposures in coadd |
| COADD_EXPTIME | 31 | Summed exposure time for coadd [seconds] |
| COADD_EXPTIME | 32 | Target selection bitmask for commissioning |
| SV1_DESI_TARGET | 33 | DESI (dark time program) target selection bitmask for SV1 |
| SV2_DESI_TARGET | 34 | DESI (dark time program) target selection bitmask for SV2 |
| SV1_SCND_TARGET | 35 | Secondary target selection bitmask for SV1 |
| SV2_SCND_TARGET | 36 | Secondary target selection bitmask for SV2 |
| SCND_TARGET | 37 | [Link](https://desidatamodel.readthedocs.io/en/latest/DESI_TARGET/TARG_DIR/DR/VERSION/targets/PHASE/RESOLVE/OBSCON/PHASEtargets-OBSCON-RESOLVE-hp-HP.html#hdu1) |
| TSNR2_LYA | 38 | LYA template (S/N)^2 summed over B,R,Z |
| TSNR2_QSO | 39 | QSO template (S/N)^2 summed over B,R,Z |
| QSO_MASKBITS | 61 | QSO selection bitmask |
| HPXPIXEL | 62 | [Link](https://desidatamodel.readthedocs.io/en/latest/DESI_TARGET/TARG_DIR/DR/VERSION/targets/PHASE/RESOLVE/OBSCON/PHASEtargets-OBSCON-RESOLVE-hp-HP.html#hdu1) |
| SURVEY | 63 | SV3 Survey |
| PROGRAM | 64 | Program name(dark) |

The descriptions for columns 10 through 24 can be found [here](https://desidatamodel.readthedocs.io/en/latest/DESI_TARGET/TARG_DIR/DR/VERSION/targets/PHASE/RESOLVE/OBSCON/PHASEtargets-OBSCON-RESOLVE-hp-HP.html#hdu1).

The descriptions for columns 40 through 46 can be found [here](https://desidatamodel.readthedocs.io/en/latest/DESI_SPECTRO_REDUX/SPECPROD/tiles/GROUPTYPE/TILEID/GROUPID/qso_mgii-SPECTROGRAPH-TILEID-GROUPID.html).

The descriptions for columns 47 through 60 can be found [here](https://desidatamodel.readthedocs.io/en/latest/DESI_SPECTRO_REDUX/SPECPROD/tiles/GROUPTYPE/TILEID/GROUPID/qso_qn-SPECTROGRAPH-TILEID-GROUPID.html).

Columns 65 through 96 as well as column 103 are "BAL specific columns", unique to the BAL VAC. Information about these targets is shown below and can  also be found in Table 1. of [Filbert et al. 2023](https://www.overleaf.com/read/gnvypxkmsdzs) (in preparation).

| Column # | Column name | Data type | Units | Description |
|:--------:|:-----------:|:---------:|:-----:|---------------|
| 65 | PCA_COEFFS | float32[5] | | Coefficients on PCA eigenbasis for spectrum fit. |
| 66 | PCA_CHI2  | float32 | | Goodness of fit from PCA components. |
| 67 | BAL_PROB | float32 | | Likelihood of BAL (not populated in DESI EDR BAL catalog) | 
| 68 | BI_CIV | float32 | km/s | Equivalent width of CIV absorption by Balnicity index definition. |
| 69 | ERR_BI_CIV | float32 | km/s | Uncertainty in BI from CIV absorption. | 
| 70 | NCIV_2000 | int32 | | Number of absorption troughs from CIV extending > 2000 km/s. | 
| 71 | VMIN_CIV_2000 | float32[5] | km/s | Minimum velocity of BI absorption troughs blueward of CIV. | 
| 72 | VMAX_CIV_2000 | float32[5]  | km/s | Maximum velocity of BI absorption troughs blueward of CIV. | 
| 73 | POSMIN_CIV_2000 | float32[5] | km/s | Velocity displacement from CIV of normalized flux minimum for each AI absorption trough. |
| 74 | FMIN_CIV_2000 | float32[5]  | | Value of normalized flux minimum for each BI absorption trough from CIV. |
| 75 | AI_CIV | float32 | km/s | Equivalent width of CIV absorption by absorption index definition. | 
| 76 | ERR_AI_CIV | float32 | km/s | Uncertainty in AI from CIV absorption. |
| 77 | NCIV_450 | int32 | | Number of absorption troughs from CIV extending > 450 km/s. | 
| 78 | VMIN_CIV_450 | float32[17] | km/s | Minimum velocity of AI absorption troughs blueward of CIV. | 
| 79 | VMAX_CIV_450 | float32[17] | km/s | Maximum velocity of AI absorption troughs blueward of CIV. | 
| 80 | POSMIN_CIV_450 | float32[17] | km/s | Velocity displacement from CIV of normalized flux minimum for each AI absorption trough. | 
| 81 | FMIN_CIV_450 | float32[17] | km/s | Value of normalized flux minimum for each AI absorption trough from CIV. | 
| 82 | BI_SIIV | float32 | km\s | Equivalent width of  SiIV absorption by Balnicity index definition. | 
| 83 | ERR_BI_SIIV | float32 | km/s | Uncertainty in BI from SiIV absorption. |
| 84 | NSIIV_2000 | int32 | | Number of absorption troughs from SiIV extending > 2000 km/s. | 
| 85 | VMIN_SIIV_2000 | float32[5] | km/s | Minimum velocity of BI absorption troughs blueward of SiIV. |
| 86 | VMAX_SIIV_2000 | float32[5]  | km/s | Maximum velocity of BI absorption troughs blueward of SiIV. | 
| 87 | POSMIN_SIIV_2000 | float32[5]  | km/s | Velocity displacement from SiIV of normalized flux minimum for each BI absorption trough. |
| 88 | FMIN_SIIV_2000 | float32[5] | km/s | Value of normalized flux minimum for each BI absorption trough from SiIV. | 
| 89 | AI_SIIV | float32 | km/s | Equivalent width of SiIV absorption by absorption index definition. |
| 90 | ERR_AI_SIIV | float32 | km/s | Uncertainty in AI from SiIV absorption. | 
| 91 | NSIIV_450 | int32 | | Number of absorption  troughs from SiIV extending > 450 km/s. | 
| 92 | VMIN_SIIV_450 | float32[17] | km/s | Minimum velocity of AI absorption troughs blueward of SiIV. | 
| 93 | VMAX_SIIV_450 | float32[17] | km/s | Maximum velocity of AI absorption troughs blueward of SiIV. | 
| 94 | POSMIN_SIIV_450 | float32[17] | km/s | Velocity displacement from SiIV of normalized flux minimum for each AI absorption trough. | 
| 95 | FMIN_SIIV_450 |  float32[17] | km/s | Value of normalized flux minimum for each AI absorption trough from SiIV. |
| 96 | BALMASK | byte  | | Bitmask specifying whether BAL information was evaluated and why. | 
| 103 | SNR_CIV | float64 | | SNR in region near CIV emission feature. |

**Note:**<br /> 
Columns 97 through 102 are redundant columns.


Contact Us
----------
Contact [Simon Fillbert](mailto:filbert.6@buckeyemail.osu.edu) or [Paul Martini](mailto:martini.10@osu.edu) for questions regarding these catalogs.

