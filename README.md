BAL Quasar Catalog for DESI Early Release Data
==============================================

#### Version: 1.0 

Description
-----------
This document describes the content of our BAL value added catalogs with updated redshifts for [DESI Fuji Early Data Release (EDR)](https://data.desi.lbl.gov/public/edr).
A more detailed explanation of the catalogs can be found in [Filbert et al. 2023](https://www.overleaf.com/project/62c73817097b4c652b1b1f1b) (in preparation).

Files and Data Model
---------------------
The BAL catalogs with updated redshifts for Fuji (EDR) can be found at [https://data.desi.lbl.gov/public/edr/vac/lsdr9-photometry/fuji/v2.0](https://data.desi.lbl.gov/public/edr/vac/bal-masked-redshift/fuji-v1.0)

DESI Collaborators can access these files at /global/cfs/cdirs/desi/public/edr/vac/bal-masked-redshift/fuji-v1.0

The VAC files contain catalogs of BALs that have had their absorption features masked. The BALs were then run through Paul Martini's [baltools](https://github.com/paulmartini/baltools) to create the catalogs.

Our VAC file contains two catalogs which are described in more detail in the table below.

| File Name | File Size |  Number of QSOs  |
|-----------|:---------:|------------------|
| QSO_cat_fuji_sv1_dark-bal-mask-priors-SNR-v1.0.fits | 42.7 MB | 37,903 |
| QSO_cat_fuji_sv3_dark-bal-mask-priors-SNR-v1.0.fits | 57.4 MB | 50,993 |

**Note:** 

The relevant data model for these catalogs can be found in the links below.<br />
The data model for the redshift fitting part of the columns can be found [here](https://desidatamodel.readthedocs.io/en/latest/DESI_SPECTRO_REDUX/SPECPROD/tiles/GROUPTYPE/TILEID/GROUPID/qso_qn-SPECTROGRAPH-TILEID-GROUPID.html) and [here.](https://desidatamodel.readthedocs.io/en/latest/DESI_SPECTRO_REDUX/SPECPROD/tiles/GROUPTYPE/TILEID/GROUPID/qso_mgii-SPECTROGRAPH-TILEID-GROUPID.html)<br />
Table 1 from [Fillbert et. al 2023](https://www.overleaf.com/read/gnvypxkmsdzs) (in preperation) contains details on the BAL specific columns.


Contact Us
----------
Contact [Simon Fillbert](mailto:filbert.6@buckeyemail.osu.edu) or [Paul Martini](mailto:martini.10@osu.edu) for questions regarding these catalogs.

