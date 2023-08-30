BAL Quasar Catalog for DESI Early Release Data
==============================================

#### Version: 1.0 

Description
-----------
This document describes the content of our BAL value added catalogs with updated redshifts for [DESI Fuji Early Data Release (EDR)](https://data.desi.lbl.gov/public/edr).
A more detailed explanation of the catalogs can be found in [Filbert et al. 2023](https://www.overleaf.com/read/gnvypxkmsdzs) (in preparation).

Files and Data Model
---------------------
The BAL catalogs with updated redshifts for Fuji (EDR) can be found at [https://data.desi.lbl.gov/public/edr/vac/edr/bal/fuji/v1.0/](https://data.desi.lbl.gov/public/edr/vac/edr/bal/fuji/v1.0/)

DESI Collaborators can access these files at /global/cfs/cdirs/desi/public/edr/vac/bal-masked-redshift/fuji/v1.0

The VAC files contain catalogs of BALs that have had their absorption features masked. The BALs were then run through Paul Martini's [baltools](https://github.com/paulmartini/baltools) to create the catalogs.

Our VAC file contains two catalogs which are described in more detail in the table below.

| File Name | File Size |  Number of QSOs  |
|:---------:|:---------:|------------------|
| QSO_cat_fuji_sv1_dark_bal_mask_v1.0.fits | 42.7 MB | 37,903 |
| QSO_cat_fuji_sv3_dark_bal_mask_v1.0.fits | 57.4 MB | 50,993 |



All of the above columns below are not specific to the BAL VAC. As such, more detailed documentation of these columns is provided below.

More detailed descriptions for columns 10 through 24 can be found [here](https://desidatamodel.readthedocs.io/en/latest/DESI_TARGET/TARG_DIR/DR/VERSION/targets/PHASE/RESOLVE/OBSCON/PHASEtargets-OBSCON-RESOLVE-hp-HP.html#hdu1).

More detailed descriptions for columns 40 through 46 can be found [here](https://desidatamodel.readthedocs.io/en/latest/DESI_SPECTRO_REDUX/SPECPROD/tiles/GROUPTYPE/TILEID/GROUPID/qso_mgii-SPECTROGRAPH-TILEID-GROUPID.html).

More detailed descriptions for columns 47 through 60 can be found [here](https://desidatamodel.readthedocs.io/en/latest/DESI_SPECTRO_REDUX/SPECPROD/tiles/GROUPTYPE/TILEID/GROUPID/qso_qn-SPECTROGRAPH-TILEID-GROUPID.html).



| Column # | Column name | Data type | Units | Description |
|:--------:|:-----------:|:---------:|:-----:|---------------|
| 0 | TARGETID | int64 | | Unique DESI target ID. |
| 1 | Z | float64 | | Redshift of target from redrock. [Link](https://github.com/desihub/redrock) |
| 2 | ZERR | float64 | | Redshift error from redrock. | 
| 3 | ZWARN | int64 | | Redshift warning flags; 0 means no error. [Mask definitions](https://github.com/desihub/redrock/blob/main/py/redrock/zwarning.py). |
| 4 | SPECTYPE | char[6] | | Type of object being observed. |
| 5 | COADD_FIBERSTATUS | int32 | | bitwise-AND of input FIBERSTATUS. |
| 6 | TARGET_RA | float64 | deg | Target right ascension. |
| 7 | TARGET_DEC | float64 | deg | Target declination. |
| 8 | MORPHTYPE | char[4] | | [Morphological model](https://www.legacysurvey.org/dr9/catalogs/) type. |
| 9 | EBV | float32 | mag | Galactic extinction E(B-V) reddening from [SFD98](https://ui.adsabs.harvard.edu/abs/1998ApJ...500..525S/abstract). |
| 10 | FLUX_G | float32 | nanomaggy | [LS](https://www.legacysurvey.org/dr9/catalogs/) flux from tractor input (g). |
| 11 | FLUX_R | float32 | nanomaggy | [LS](https://www.legacysurvey.org/dr9/catalogs/) flux from tractor input (r). |
| 12 | FLUX_Z | float32 | nanomaggy | [LS](https://www.legacysurvey.org/dr9/catalogs/) flux from tractor input (z). |
| 13 | FLUX_W1 | float32 | nanomaggy | WISE flux in W1 (AB system) |
| 14 | FLUX_W1 | float32 | nanomaggy | WISE flux in W2 (AB system) |
| 15 | FLUX_IVAR_G | float32 | nanomaggy^-2 | Inverse variance of FLUX_G. |
| 16 | FLUX_IVAR_R | float32 | nanomaggy^-2 | Inverse variance of FLUX_R. |
| 17 | FLUX_IVAR_Z | float32 | nanomaggy^-2 | Inverse variance of FLUX_Z. |
| 18 | FLUX_IVAR_W1 | float32 | nanomaggy^-2 | Inverse variance of FLUX_W1 (AB system). |
| 19 | FLUX_IVAR_GW2 | float32 | nanomaggy^-2 | Inverse variance of FLUX_W2 (AB system). |
| 20 | MW_TRANSMISSION_G | float64 | | Milky Way dust transmission in [LS](https://www.legacysurvey.org/dr9/catalogs/) g. |
| 21 | MW_TRANSMISSION_R | float64 | | Milky Way dust transmission in [LS](https://www.legacysurvey.org/dr9/catalogs/) r. |
| 22 | MW_TRANSMISSION_Z | float64 | | Milky Way dust transmission in [LS](https://www.legacysurvey.org/dr9/catalogs/) r. |
| 23 | MW_TRANSMISSION_W1 | float64 | | Milky Way dust transmission in WISE W1. |
| 24 | MW_TRANSMISSION_W2 | float64 | | Milky Way dust transmission in WISE W2. |
| 25 | PROBA_RF | float64 | | Probability of Random Forest selection. |
| 26 | MASKBITS | int16 | | bitmask for maskbits maps, as on the [LS DR9 bitmasks page](https://www.legacysurvey.org/dr9/bitmasks/). |
| 27 | SV3_DESI_TARGET | int64 | | DESI (dark time program) target selection bitmask for SV3. |
| 28 | SV3_SCND_TARGET | int64 | | Secondary target selection bitmask for SV3. |
| 29 | DESI_TARGET | int64 | | DESI (dark time program) target selection [bitmask](https://desidatamodel.readthedocs.io/en/latest/DESI_TARGET/TARG_DIR/DR/VERSION/targets/PHASE/RESOLVE/OBSCON/PHASEtargets-OBSCON-RESOLVE-hp-HP.html#id1). |
| 30 | COADD_NUMEXP | int16 | | Number of exposures in coadd. |
| 31 | COADD_EXPTIME | float32 | sec | Summed exposure time for coadd. |
| 32 | CMX_TARGET | int64 | | Target selection bitmask for commissioning |
| 37 | SCND_TARGET | int64 | | SCND (secondary program) target selection bitmask. |
| 38 | TSNR2_LYA | float32 | | LYA template (S/N)^2 summed over B,R,Z. | 
| 39 | TSNR2_QSO | float32 | | QSO template (S/N)^2 summed over B,R,Z. | 
| 40 | DELTA_CHI2_MGII | float32 | | Difference of chi2 between redrock fit and [MgII fitter](https://github.com/desihub/desispec/blob/720153babcf85dd93530252b0c1f631d48edfc0d/py/desispec/mgii_afterburner.py#L5) over the lambda interval considered during the fit. |
| 41 | A_MGII | float32 | | Fit parameter for MgII afterburner. | 
| 42 | SIGMA_MGII | float32 | | Fit parameter for MgII afterburner. |
| 43 | B_MGII | float32 | | Fit parameter for MgII afterburner. |
| 44 | VAR_A_MGII | float32 | | Error on A_MGII. |
| 45 | VAR_SIGMA_MGII | float32 | | Error on SIGMA_MGII. |
| 46 | VAR_B_MGII | float32 | | Error on B_MGII. |
| 47 | Z_RR | float32 | | Redshift collected from redrock file. |
| 48 | Z_QN | float32 | | Redshift measured by QuasarNET using line with highest confidence. | 
| 49 | C_LYA | float32 | | Confidence for LyA line, i.e. ~probability to be a QSO. |
| 50 | C_CIV | float32 | | Confidence for CIV line. | 
| 51 | C_CIII | float32 | | Confidence for CIII line. |
| 52 | C_MGII | float32 | | Confidence for MGII line. |
| 53 | C_Hbeta | float32 | | Confidence for Hbeta line. |
| 54 | C_Halpha | float32 | | Confidence for Halpha line. |
| 55 | Z_LYA | float32 | | Redshift estimated by QuasarNET with LyA line. |
| 56 | Z_CIV | float32 | | Redshift estimated by QuasarNET with CIV line. |
| 57 | Z_CIII | float32 | | Redshift estimated by QuasarNET with CIII line. |
| 58 | Z_MGII | float32 | | Redshift estimated by QuasarNET with MgII line. |
| 59 | Z_Hbeta | float32 | | Redshift estimated by QuasarNET with Hbeta line. |
| 60 | Z_Halpha | float32 | | Redshift estimated by QuasarNET with Halpha line. |
| 61 | QSO_MASKBITS | int32 | | Bitmask encoding path object took through redshift afterburner. |
| 62 | HPXPIXEL | int64 | | HEALPixel containing target at HPXNSIDE. |
| 63 | SURVEY | char[3] | | Abbreviation of survey that target was observed under. |
| 64 | PROGRAM | char[4] | | Abbreviation of program that target was observed under. |

**Note:**<br /> 
Columns 33 through 36 are not detailed here as they are specific to each catalog. In any case, they are target selection bitmasks and likely not relevant for most users. 



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
| 82 | BI_SIIV | float32 | km/s | Equivalent width of  SiIV absorption by Balnicity index definition. | 
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
| 96 | BALMASK | unsigned byte | | Bitmask specifying whether BAL information was evaluated and why. | 
| 97 | Z_MASK | float64 | | Redshift evaluated by redrock after BAL masking procedure. |
| 98 | ZERR_MASK | float64 | | Redshift error on Z_MASK from redrock. |
| 99 | ZWARN_MASK | int64 | | Redshift warning flags from redrock after masking BALs; 0 means no error. [Mask definitions](https://github.com/desihub/redrock/blob/main/py/redrock/zwarning.py). |
| 100 | CHI2_MASK | float64 | | Goodness of fit of best fitting template to spectra with BALs masked. |
| 101 | DELTACHI2_MASK | float64 | | Difference in goodness of fit between two best fitting templates of spectra with BALs masked\[1]. |
| 102 | SPECTYPE_MASK | chat[6] | | Spectype of target after BALs are masked. Should be 'QSO' since only QSO templates used. |
| 103 | SNR_CIV | float64 | | SNR in region near CIV emission feature. |


\[1]: Note that, since this catalog features targets from the [quasar afterburner](https://ui.adsabs.harvard.edu/abs/2023ApJ...944..107C/abstract), we are relatively sure that these objects are true quasars. Because of this, we only use quasar templates when rerunning redrock after masking BALs. This results in DELTACHI2_MASK values which may be lower than one might expect from typical DESI data. 




Contact Us
----------
Contact [Simon Fillbert](mailto:filbert.6@buckeyemail.osu.edu) or [Paul Martini](mailto:martini.10@osu.edu) for questions regarding these catalogs.

