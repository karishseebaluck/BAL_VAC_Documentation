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
| PROBA_RF | 25 | ?? |
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



**Note:**<br /> 
The relevant data model for these catalogs can be found in the links below.<br />
The data model for the redshift fitting part of the columns can be found [here](https://desidatamodel.readthedocs.io/en/latest/DESI_SPECTRO_REDUX/SPECPROD/tiles/GROUPTYPE/TILEID/GROUPID/qso_qn-SPECTROGRAPH-TILEID-GROUPID.html) and [here.](https://desidatamodel.readthedocs.io/en/latest/DESI_SPECTRO_REDUX/SPECPROD/tiles/GROUPTYPE/TILEID/GROUPID/qso_mgii-SPECTROGRAPH-TILEID-GROUPID.html)<br />
Table 1 from [Fillbert et. al 2023](https://www.overleaf.com/read/gnvypxkmsdzs) (in preperation) contains details on the BAL specific columns.


Contact Us
----------
Contact [Simon Fillbert](mailto:filbert.6@buckeyemail.osu.edu) or [Paul Martini](mailto:martini.10@osu.edu) for questions regarding these catalogs.

