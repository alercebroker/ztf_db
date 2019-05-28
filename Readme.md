# Database description

## 1. objects

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
| **id** |  integer           |  not null  | Internal ALeRCE ID |
| **oid** |  text              |  not null  | ZTF object ID |
| **nobs** |  integer           |            | Number of observations |
| **mean_magap_g** |  double precision  |            | Mean aperture corrected magnitude in g |
| **mean_magap_r** |  double precision  |            | Mean aperture corrected magnitude in r band |
| **median_magap_g** |  double precision  |            | Median aperture corrected magnitude in g |
| **median_magap_r** |  double precision  |            | Median aperture corrected magnitude in r |
| **max_magap_g** |  double precision  |            | Max aperture corrected magnitude in g |
| **max_magap_r** |  double precision  |            | Max aperture corrected magnitude in r |
| **min_magap_g** |  double precision  |            | Min aperture corrected magnitude in g |
| **min_magap_r** |  double precision  |            | Min aperture corrected magnitude in r |
| **sigma_magap_g** |  double precision  |            | Standard deviation of the aperture corrected magnitude in g |
| **sigma_magap_r** |  double precision  |            | Standard deviation of the aperture corrected magnitude in r |
| **last_magap_g** |  double precision  |            | Last value of the aperture corrected magnitude in g |
| **last_magap_r** |  double precision  |            | Last value of the aperture corrected magnitude in r |
| **first_magap_g** |  double precision  |            | First value of the aperture corrected magnitude in g |
| **first_magap_r** |  double precision  |            | First value of the aperture corrected magnitude in r |
| **mean_magpsf_g** |  double precision  |            | Mean value of the psf corrected magnitude in g |
| **mean_magpsf_r** |  double precision  |            | Mean value of the psf corrected magnitude in r |
| **median_magpsf_g** |  double precision  |            | Median value of the psf corrected magnitude in g |
| **median_magpsf_r** |  double precision  |            | Mean value of the psf corrected magnitude in r |
| **max_magpsf_g** |  double precision  |            | Max value of the psf corrected magnitude in g |
| **max_magpsf_r** |  double precision  |            | Max value of the psf corrected magnitude in r |
| **min_magpsf_g** |  double precision  |            | Min value of the psf corrected magnitude in g |
| **min_magpsf_r** |  double precision  |            | Min value of the psf corrected magnitude in r |
| **sigma_magpsf_g** |  double precision  |            | Standard deviation of the psf corrected magnitude in g |
| **sigma_magpsf_r** |  double precision  |            | Standard deviation of the psf corrected magnitude in r |
| **last_magpsf_g** |  double precision  |            | Last value of the psf corrected magnitude in g |
| **last_magpsf_r** |  double precision  |            | Last value of the psf corrected magnitude in r |
| **first_magpsf_g** |  double precision  |            | First value of the psf corrected magnitude in g |
| **first_magpsf_r** |  double precision  |            | First value of the psf corrected magnitude in r |
| **meanra** |  double precision  |            | Mean right ascension [deg] |
| **meandec** |  double precision  |            | Mean declination [deg] |
| **sigmara** |  double precision  |            | Standard deviation of the right ascension [deg] |
| **sigmadec** |  double precision  |            | Standard deviation of the declination [deg] |
| **deltajd** |  double precision  |            | Difference between the last and first detections |
| **lastmjd** |  double precision  |            | Last detected modified julian date |
| **firstmjd** |  double precision  |            | First detected modified julian date |
| **period** |  double precision  |            | Reported Period if any [days] |
| **catalogid** |  integer           |            | Preferred Catalog where a cross match exists if any |
| **classxmatch** |  integer           |            | ID in the previous cross match catalog if any |
| **classrf** |  integer           |            | predicted class according to the random forest classifier |
| **pclassrf** |  double precision  |            | probability of the most likely class according to the random forest classfier|

## 2. detections

Attributes retrieved from the ZTF alert.

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
| **object_id** |  integer           |             | unique identifier for this object (number format) |
| **oid** |  text              |             | unique identifier for this object (ZTF format) |
| **candid** |  bigint            |             | Candidate ID from operations DB                              |
| **mjd** |  double precision  |             | Observation Julian date at start of exposure [days] |
| **fid** |  smallint          |             | Filter ID (1=g; 2=r; 3=i) |
| **diffmaglim** |  double precision  |             | 5-sigma mag limit in difference image based on PSF-fit photometry [mag] |
| **magpsf** |  double precision  |             | magnitude from PSF-fit photometry [mag] |
| **magap** |  double precision  |             | Aperture mag using 8 pixel diameter aperture [mag] |
| **sigmapsf** |  double precision  |             | 1-sigma uncertainty in magpsf [mag] |
| **sigmagap** |  double precision  |             | 1-sigma uncertainty in magap [mag] |
| **ra** |  double precision  |             | Right Ascension of candidate; J2000 [deg] |
| **dec** |  double precision  |             | Declination of candidate; J2000 [deg] |
| **sigmara** |  double precision  |             |                |
| **sigmadec** |  double precision  |             |                |
| **isdiffpos** |  smallint          |             | t or 1 => candidate is from positive (sci minus ref) subtraction; f or 0 => candidate is from negative (ref minus sci) subtraction |
| **distpsnr1** |  double precision  |             | Distance of closest source from PS1 catalog; if exists within 30 arcsec [arcsec] |
| **sgscore1** |  double precision  |             | Star/Galaxy score of closest source from PS1 catalog 0 <= sgscore <= 1 where closer to 1 implies higher likelihood of being a star |
| **field** |  integer           |             | ZTF field ID |
| **rcid** |  integer           |             | Readout channel ID [00 .. 63] |
| **magnr** |  double precision  |             | magnitude of nearest source in reference image PSF-catalog within 30 arcsec [mag] |
| **sigmagnr** |  double precision  |             | 1-sigma uncertainty in magnr within 30 arcsec [mag] |
| **rb** |  double precision  |             | RealBogus quality score; range is 0 to 1 where closer to 1 is more reliable |
| **magpsf_corr** |  double precision  |             |                |
| **magap_corr** |  double precision  |             |                |
| **sigmapsf_corr** |  double precision  |             |                |
| **sigmagap_corr** |  double precision  |             |                |

## 3. non_detections

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
| **oid** |  text              |             | ZTF object id |
| **mjd** |  double precision  |             | Modified Julian Date |
| **diffmaglim** |  double precision  |             | Limiting difference magnitude |
| **fid** |  smallint          |             | FIlter ID (1=g; 2=r; 3=i)|
| **object_id** |  integer           |             | unique identifier for this object (number format) |

## 4. features

Description of FATS features is in http://isadoranun.github.io/tsfeat/FeaturesDocumentation.html#The-features

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
| **oid** |  text              |  not null   |  ZTF object id |
| **n_samples_1** |  double precision  |             |                |
| **amplitude_1** |  double precision  |             |                |
| **andersondarling_1** |  double precision  |             |                |
| **autocor_length_1** |  double precision  |             |                |
| **beyond1std_1** |  double precision  |             |                |
| **car_sigma_1** |  double precision  |             |                |
| **car_mean_1** |  double precision  |             |                |
| **car_tau_1** |  double precision  |             |                |
| **con_1** |  double precision  |             |                |
| **eta_e_1** |  double precision  |             |                |
| **gskew_1** |  double precision  |             |                |
| **maxslope_1** |  double precision  |             |                |
| **mean_1** |  double precision  |             |                |
| **meanvariance_1** |  double precision  |             |                |
| **medianabsdev_1** |  double precision  |             |                |
| **medianbrp_1** |  double precision  |             |                |
| **pairslopetrend_1** |  double precision  |             |                |
| **percentamplitude_1** |  double precision  |             |                |
| **q31_1** |  double precision  |             |                |
| **periodls_1** |  double precision  |             |                |
| **period_fit_1** |  double precision  |             |                |
| **psi_cs_1** |  double precision  |             |                |
| **psi_eta_1** |  double precision  |             |                |
| **rcs_1** |  double precision  |             |                |
| **skew_1** |  double precision  |             |                |
| **smallkurtosis_1** |  double precision  |             |                |
| **std_1** |  double precision  |             |                |
| **stetsonk_1** |  double precision  |             |                |
| **freq1_harmonics_amplitude_0_1** |  double precision  |             |                |
| **freq1_harmonics_rel_phase_0_1** |  double precision  |             |                |
| **freq1_harmonics_amplitude_1_1** |  double precision  |             |                |
| **freq1_harmonics_rel_phase_1_1** |  double precision  |             |                |
| **freq1_harmonics_amplitude_2_1** |  double precision  |             |                |
| **freq1_harmonics_rel_phase_2_1** |  double precision  |             |                |
| **freq1_harmonics_amplitude_3_1** |  double precision  |             |                |
| **freq1_harmonics_rel_phase_3_1** |  double precision  |             |                |
| **req2_harmonics_amplitude_0_1** |   double precision   |               |   |
| **freq2_harmonics_rel_phase_0_1** |   double precision   |               |   |
| **freq2_harmonics_amplitude_1_1** |   double precision   |               |   |
| **freq2_harmonics_rel_phase_1_1** |   double precision   |               |   |
| **freq2_harmonics_amplitude_2_1** |   double precision   |               |   |
| **freq2_harmonics_rel_phase_2_1** |   double precision   |               |   |
| **freq2_harmonics_amplitude_3_1** |   double precision   |               |   |
| **freq2_harmonics_rel_phase_3_1** |   double precision   |               |   |
| **freq3_harmonics_amplitude_0_1** |   double precision   |               |   |
| **freq3_harmonics_rel_phase_0_1** |   double precision   |               |   |
| **freq3_harmonics_amplitude_1_1** |   double precision   |               |   |
| **freq3_harmonics_rel_phase_1_1** |   double precision   |               |   |
| **freq3_harmonics_amplitude_2_1** |   double precision   |               |   |
| **freq3_harmonics_rel_phase_2_1** |   double precision   |               |   |
| **freq3_harmonics_amplitude_3_1** |   double precision   |               |   |
| **freq3_harmonics_rel_phase_3_1** |   double precision   |               |   |
| **n_samples_2** |   double precision   |               |   |
| **amplitude_2** |   double precision   |               |   |
| **andersondarling_2** |   double precision   |               |   |
| **autocor_length_2** |   double precision   |               |   |
| **beyond1std_2** |   double precision   |               |   |
| **car_sigma_2** |   double precision   |               |   |
| **car_mean_2** |   double precision   |               |   |
| **car_tau_2** |   double precision   |               |   |
| **con_2** |   double precision   |               |   |
| **eta_e_2** |   double precision   |               |   |
| **gskew_2** |   double precision   |               |   |
| **maxslope_2** |   double precision   |               |   |
| **mean_2** |   double precision   |               |   |
| **meanvariance_2** |   double precision   |               |   |
| **medianabsdev_2** |   double precision   |               |   |
| **medianbrp_2** |   double precision   |               |   |
| **pairslopetrend_2** |   double precision   |               |   |
| **percentamplitude_2** |   double precision   |               |   |
| **q31_2** |   double precision   |               |   |
| **periodls_2** |   double precision   |               |   |
| **period_fit_2** |   double precision   |               |   |
| **psi_cs_2** |   double precision   |               |   |
| **psi_eta_2** |   double precision   |               |   |
| **rcs_2** |   double precision   |               |   |
| **skew_2** |   double precision   |               |   |
| **smallkurtosis_2** |   double precision   |               |   |
| **std_2** |   double precision   |               |   |
| **stetsonk_2** |   double precision   |               |   |
| **freq1_harmonics_amplitude_0_2** |   double precision   |               |   |
| **freq1_harmonics_rel_phase_0_2** |   double precision   |               |   |
| **freq1_harmonics_amplitude_1_2** |   double precision   |               |   |
| **freq1_harmonics_rel_phase_1_2** |   double precision   |               |   |
| **freq1_harmonics_amplitude_2_2** |   double precision   |               |   |
| **freq1_harmonics_rel_phase_2_2** |   double precision   |               |   |
| **freq1_harmonics_amplitude_3_2** |   double precision   |               |   |
| **freq1_harmonics_rel_phase_3_2** |   double precision   |               |   |
| **freq2_harmonics_amplitude_0_2** |   double precision   |               |   |
| **freq2_harmonics_rel_phase_0_2** |   double precision   |               |   |
| **freq2_harmonics_amplitude_1_2** |   double precision   |               |   |
| **freq2_harmonics_rel_phase_1_2** |   double precision   |               |   |
| **freq2_harmonics_amplitude_2_2** |   double precision   |               |   |
| **freq2_harmonics_rel_phase_2_2** |   double precision   |               |   |
| **freq2_harmonics_amplitude_3_2** |   double precision   |               |   |
| **freq2_harmonics_rel_phase_3_2** |   double precision   |               |   |
| **freq3_harmonics_amplitude_0_2** |   double precision   |               |   |
| **freq3_harmonics_amplitude_1_2** |   double precision   |               |   |
| **freq3_harmonics_rel_phase_1_2** |   double precision   |               |   |
| **freq3_harmonics_amplitude_2_2** |   double precision   |               |   |
| **freq3_harmonics_rel_phase_2_2** |   double precision   |               |   |
| **freq3_harmonics_amplitude_3_2** |   double precision   |               |   |
| **freq3_harmonics_rel_phase_3_2** |   double precision   |               |   |
| **gal_b** |   double precision   |               |  galactic latitude  |
| **gal_l** |   double precision   |               |  galactic longitude  |
| **object_id** |   integer            |               |   |


## 5. probabilities

Random Forest probabilities https://github.com/alercebroker/baseline_classifier/wiki/Random-Forest-v1

| Column | Type | Modifier | Description |
| ------ | ---- | -------- | ----------- |
| **oid** |   text               |   not null    |   |
| **classifierid** |   integer            |   not null    |   |
| **ceph_prob** |   double precision   |               |  Cepheid probability  |
| **dsct_prob** |   double precision   |               |  Delta scuti probability  |
| **eb_prob** |   double precision   |               |  Eclipsing binary probability  |
| **lpv_prob** |   double precision   |               |  Long-period variable probability  |
| **rrl_prob** |   double precision   |               |  RR Lyrae probability  |
| **sne_prob** |   double precision   |               |  Supernovae probability  |
| **other_prob** |   double precision   |               |  "Other" probability (Tidal disruption event, active galactic nuclei, other pulsating objects, cataclismic variables, novae, other periodic objects)  |
| **object_id** |   integer            |               |   |


## 6. xmatch

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
| **oid** |   character varying(12)   |               |   |
| **catalogid** |   character varying(15)   |               |   |
| **cid** |   character varying(40)   |               |   |
| **object_id** |   integer                 |               |   |

## 7. class

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
| **id** |   integer                 |               |   |
| **name** |   character varying(15)   |               |   |


## 8. crtsnorth

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
| **Catalina_Surveys_ID** |   text               |               |   |
| **Numerical_ID** |   bigint             |               |   |
| **V_(mag)** |   double precision   |               |   |
| **Period_(days)** |   double precision   |               |   |
| **Amplitude** |   double precision   |               |   |
| **Number_Obs** |   integer            |               |   |
| **Var_Type** |   integer            |               |   |
| **ra** |   double precision   |               |   |
| **dec** |   double precision   |               |   |

## 9. crtssouth

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
| **SSS_ID** |   text               |               |   |
| **Numerical_ID** |   bigint             |               |   |
| **ra** |   double precision   |               |   |
| **dec** |   double precision   |               |   |
| **Period** |   double precision   |               |   |
| **V_CSS** |   double precision   |               |   |
| **Npts** |   integer            |               |   |
| **V_amp** |   double precision   |               |   |
| **Type** |   integer            |               |   |

## 10. asassn

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
| **ASAS-SN Name** |   text               |               |   |
| **Other Names** |   text               |               |   |
| **LCID** |   integer            |               |   |
| **ra** |   double precision   |               |   |
| **dec** |   double precision   |               |   |
| **Mean VMag** |   double precision   |               |   |
| **Amplitude** |   double precision   |               |   |
| **Period** |   double precision   |               |   |
| **Type** |   text               |               |   |
| **Url** |   text               |               |   |
| **Reference** |   text               |               |   |
| **Dist** |   double precision   |               |   |
| **Parallax** |   double precision   |               |   |
| **Parallax Error** |   double precision   |               |   |
| **Gmag** |   double precision   |               |   |
| **Bpmag** |   double precision   |               |   |
| **Rpmag** |   double precision   |               |   |
| **Jmag** |   double precision   |               |   |
| **Hmag** |   double precision   |               |   |
| **Kmag** |   double precision   |               |   |
| **W1mag** |   double precision   |               |   |
| **W2mag** |   double precision   |               |   |
| **W3mag** |   double precision   |               |   |
| **W4mag** |   double precision   |               |   |
| **BP-RR** |   double precision   |               |   |
| **J-K** |   double precision   |               |   |
| **W1-W2** |   double precision   |               |   |
| **W3-W4** |   double precision   |               |   |
| **Sllk Statistic** |   double precision   |               |   |
| **RF Regression Score** |   double precision   |               |   |
| **Classification Probability** |   double precision   |               |   |
| **Epoch (HJD)** |   double precision   |               |   |

## 11. tns

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
| **Name** |   text                          |               |   |
| **RA_orig** |   text                          |               |   |
| **DEC_orig** |   text                          |               |   |
| **Obj. Type** |   text                          |               |   |
| **Redshift** |   double precision              |               |   |
| **Host Name** |   text                          |               |   |
| **Host Redshift** |   double precision              |               |   |
| **Discovering Group/s** |   text                          |               |   |
| **Classifying Group/s** |   text                          |               |   |
| **Associated Group/s** |   text                          |               |   |
| **Disc. Internal Name** |   text                          |               |   |
| **Disc. Instrument/s** |   text                          |               |   |
| **Class. Instrument/s** |   text                          |               |   |
| **TNS AT** |   integer                       |               |   |
| **Public** |   integer                       |               |   |
| **End Prop. Period** |   date                          |               |   |
| **Discovery Mag** |   double precision              |               |   |
| **Discovery Mag Filter** |   text                          |               |   |
| **Discovery Date (UT)** |   timestamp without time zone   |               |   |
| **Sender** |   text                          |               |   |
| **Ext. catalog/s** |   text                          |               |   |
| **ra** |   double precision              |               |   |
| **dec** |   double precision              |               |   |
| **aitoff_x** |   double precision              |               |   |
| **aitoff_y** |   double precision              |               |   |

## 12. linear

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
| **LINEARobjectID** |   bigint             |               |   |
| **LCtype** |   integer            |               |   |
| **P** |   double precision   |               |   |
| **A** |   double precision   |               |   |
| **mmed** |   double precision   |               |   |
| **stdev** |   double precision   |               |   |
| **rms** |   double precision   |               |   |
| **Lchi2pdf** |   double precision   |               |   |
| **nObs** |   integer            |               |   |
| **skew** |   double precision   |               |   |
| **kurt** |   double precision   |               |   |
| **LR** |   double precision   |               |   |
| **CUF** |   integer            |               |   |
| **t2** |   integer            |               |   |
| **t3** |   integer            |               |   |
| **ra** |   double precision   |               |   |
| **dec** |   double precision   |               |   |
| **oType** |   integer            |               |   |
| **nS** |   integer            |               |   |
| **rExt** |   double precision   |               |   |
| **u** |   double precision   |               |   |
| **g** |   double precision   |               |   |
| **r** |   double precision   |               |   |
| **i** |   double precision   |               |   |
| **z** |   double precision   |               |   |
| **uErr** |   double precision   |               |   |
| **gErr** |   double precision   |               |   |
| **rErr** |   double precision   |               |   |
| **iErr** |   double precision   |               |   |
| **zErr** |   double precision   |               |   |

## 13. magref

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
| **object_id** |   integer            |               |   |
| **oid** |   text               |               |   |
| **fid** |   integer            |               |   |
| **rcid** |   integer            |               |   |
| **field** |   integer            |               |   |
| **magref** |   double precision   |               |   |
| **sigmagref** |   double precision   |               |   |
| **corrected** |   boolean            |               |   |
