# Database description

## 1. objects

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
| id             | integer          | not null |             |
| oid            | text             | not null |             |
| nobs           | integer          |          |             |
| mean_magap_g   | double precision |          |             |
| mean_magap_r   | double precision |          |             |
|median_magap_g  | double precision |          |             |
|median_magap_r  | double precision |          |             |
|max_magap_g     | double precision |          |             |
|max_magap_r     | double precision |          |             |
|min_magap_g     | double precision |          |             |
|min_magap_r     | double precision |          |             |
|sigma_magap_g   | double precision |          |             |
|sigma_magap_r   | double precision |          |             |
|last_magap_g    | double precision |          |             |
|last_magap_r    | double precision |          |             |
|first_magap_g   | double precision |          |             |
|first_magap_r   | double precision |          |             |
|mean_magpsf_g   | double precision |          |             |
|mean_magpsf_r   | double precision |          |             |
|median_magpsf_g | double precision |          |             |
|median_magpsf_r | double precision |          |             |
|max_magpsf_g    | double precision |          |             |
|max_magpsf_r    | double precision |          |             |
|min_magpsf_g    | double precision |          |             |
|min_magpsf_r    | double precision |          |             |
|sigma_magpsf_g  | double precision |          |             |
|sigma_magpsf_r  | double precision |          |             |
|last_magpsf_g   | double precision |          |             |
|last_magpsf_r   | double precision |          |             |
|first_magpsf_g  | double precision |          |             |
|first_magpsf_r  | double precision |          |             |
|meanra          | double precision |          |             |
|meandec         | double precision |          |             |
|sigmara         | double precision |          |             |
|sigmadec        | double precision |          |             |
|deltajd         | double precision |          |             |
|lastjd          | double precision |          |             |
|firstjd         | double precision |          |             |
|period          | double precision |          |             |
|catalogid       | integer          |          |             |
|classxmatch     | integer          |          |             |
|classrf         | integer          |          |             |
|pclassrf        | double precision |          |             |

## 2. detections

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
|object_id     | integer          |           |              |
|oid           | text             |           |              |
|candid        | bigint           |           |              |
|jd            | double precision |           |              |
|fid           | smallint         |           |              |
|diffmaglim    | double precision |           |              |
|magpsf        | double precision |           |              |
|magap         | double precision |           |              |
|sigmapsf      | double precision |           |              |
|sigmagap      | double precision |           |              |
|ra            | double precision |           |              |
|dec           | double precision |           |              |
|sigmara       | double precision |           |              |
|sigmadec      | double precision |           |              |
|isdiffpos     | smallint         |           |              |
|distpsnr1     | double precision |           |              |
|sgscore1      | double precision |           |              |
|field         | integer          |           |              |
|rcid          | integer          |           |              |
|magnr         | double precision |           |              |
|sigmagnr      | double precision |           |              |
|rb            | double precision |           |              |
|magpsf_corr   | double precision |           |              |
|magap_corr    | double precision |           |              |
|sigmapsf_corr | double precision |           |              |
|sigmagap_corr | double precision |           |              |

## 3. no_detections

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
|oid        | text             |           |              |
|jd         | double precision |           |              |
|diffmaglim | double precision |           |              |
|fid        | smallint         |           |              |
|object_id  | integer          |           |              |

## 4. features

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
|oid            | text             | not null  |              |
|n_samples_1    | integer          |           |              |
|amplitude_1                   | double precision |           |              |
|andersondarling_1             | double precision |           |              |
|autocor_length_1              | double precision |           |              |
|beyond1std_1                  | double precision |           |              |
|car_sigma_1                   | double precision |           |              |
|car_mean_1                    | double precision |           |              |
|car_tau_1                     | double precision |           |              |
|con_1                         | double precision |           |              |
|eta_e_1                       | double precision |           |              |
|gskew_1                       | double precision |           |              |
|maxslope_1                    | double precision |           |              |
|mean_1                        | double precision |           |              |
|meanvariance_1                | double precision |           |              |
|medianabsdev_1                | double precision |           |              |
|medianbrp_1                   | double precision |           |              |
|pairslopetrend_1              | double precision |           |              |
|percentamplitude_1            | double precision |           |              |
|q31_1                         | double precision |           |              |
|periodls_1                    | double precision |           |              |
|period_fit_1                  | double precision |           |              |
|psi_cs_1                      | double precision |           |              |
|psi_eta_1                     | double precision |           |              |
|rcs_1                         | double precision |           |              |
|skew_1                        | double precision |           |              |
|smallkurtosis_1               | double precision |           |              |
|std_1                         | double precision |           |              |
|stetsonk_1                    | double precision |           |              |
|freq1_harmonics_amplitude_0_1 | double precision |           |              |
|freq1_harmonics_rel_phase_0_1 | double precision |           |              |
|freq1_harmonics_amplitude_1_1 | double precision |           |              |
|freq1_harmonics_rel_phase_1_1 | double precision |           |              |
|freq1_harmonics_amplitude_2_1 | double precision |           |              |
|freq1_harmonics_rel_phase_2_1 | double precision |           |              |
|freq1_harmonics_amplitude_3_1 | double precision |           |              |
|freq1_harmonics_rel_phase_3_1 | double precision |           |              |
| req2_harmonics_amplitude_0_1  |  double precision  |             | |
|  freq2_harmonics_rel_phase_0_1  |  double precision  |             | |
|  freq2_harmonics_amplitude_1_1  |  double precision  |             | |
|  freq2_harmonics_rel_phase_1_1  |  double precision  |             | |
|  freq2_harmonics_amplitude_2_1  |  double precision  |             | |
|  freq2_harmonics_rel_phase_2_1  |  double precision  |             | |
|  freq2_harmonics_amplitude_3_1  |  double precision  |             | |
|  freq2_harmonics_rel_phase_3_1  |  double precision  |             | |
|  freq3_harmonics_amplitude_0_1  |  double precision  |             | |
|  freq3_harmonics_rel_phase_0_1  |  double precision  |             | |
|  freq3_harmonics_amplitude_1_1  |  double precision  |             | |
|  freq3_harmonics_rel_phase_1_1  |  double precision  |             | |
|  freq3_harmonics_amplitude_2_1  |  double precision  |             | |
|  freq3_harmonics_rel_phase_2_1  |  double precision  |             | |
|  freq3_harmonics_amplitude_3_1  |  double precision  |             | |
|  freq3_harmonics_rel_phase_3_1  |  double precision  |             | |
|  n_samples_2                    |  double precision  |             | |
|  amplitude_2                    |  double precision  |             | |
|  andersondarling_2              |  double precision  |             | |
|  autocor_length_2               |  double precision  |             | |
|  beyond1std_2                   |  double precision  |             | |
|  car_sigma_2                    |  double precision  |             | |
|  car_mean_2                     |  double precision  |             | |
|  car_tau_2                      |  double precision  |             | |
|  con_2                          |  double precision  |             | |
|  eta_e_2                        |  double precision  |             | |
|  gskew_2                        |  double precision  |             | |
|  maxslope_2                     |  double precision  |             | |
|  mean_2                         |  double precision  |             | |
| meanvariance_2                 |  double precision  |             | |
|  medianabsdev_2                 |  double precision  |             | |
|  medianbrp_2                    |  double precision  |             | |
|  pairslopetrend_2               |  double precision  |             | |
|  percentamplitude_2             |  double precision  |             | |
|  q31_2                          |  double precision  |             | |
|  periodls_2                     |  double precision  |             | |
|  period_fit_2                   |  double precision  |             | |
|  psi_cs_2                       |  double precision  |             | |
|  psi_eta_2                      |  double precision  |             | |
|  rcs_2                          |  double precision  |             | |
|  skew_2                         |  double precision  |             | |
|  smallkurtosis_2                |  double precision  |             | |
|  std_2                          |  double precision  |             | |
|  stetsonk_2                     |  double precision  |             | |
|  freq1_harmonics_amplitude_0_2  |  double precision  |             | |
|  freq1_harmonics_rel_phase_0_2  |  double precision  |             | |
|  freq1_harmonics_amplitude_1_2  |  double precision  |             | |
|  freq1_harmonics_rel_phase_1_2  |  double precision  |             | |
|  freq1_harmonics_amplitude_2_2  |  double precision  |             | |
|  freq1_harmonics_rel_phase_2_2  |  double precision  |             | |
|  freq1_harmonics_amplitude_3_2  |  double precision  |             | |
|  freq1_harmonics_rel_phase_3_2  |  double precision  |             | |
|  freq2_harmonics_amplitude_0_2  |  double precision  |             | |
|  freq2_harmonics_rel_phase_0_2  |  double precision  |             | |
|  freq2_harmonics_amplitude_1_2  |  double precision  |             | |
|  freq2_harmonics_rel_phase_1_2  |  double precision  |             | |
|  freq2_harmonics_amplitude_2_2  |  double precision  |             | |
|  freq2_harmonics_rel_phase_2_2  |  double precision  |             | |
|  freq2_harmonics_amplitude_3_2  |  double precision  |             | |
|  freq2_harmonics_rel_phase_3_2  |  double precision  |             | |
|  freq3_harmonics_amplitude_0_2  |  double precision  |             | |
| freq3_harmonics_amplitude_1_2  |  double precision  |             | |
|  freq3_harmonics_rel_phase_1_2  |  double precision  |             | |
|  freq3_harmonics_amplitude_2_2  |  double precision  |             | |
|  freq3_harmonics_rel_phase_2_2  |  double precision  |             | |
|  freq3_harmonics_amplitude_3_2  |  double precision  |             | |
|  freq3_harmonics_rel_phase_3_2  |  double precision  |             | |
|  gal_b                          |  double precision  |             | |
|  gal_l                          |  double precision  |             | |
|  object_id                      |  integer           |             | |


## 5. probabilities

// Insert description

| Column | Type | Modifier | Description |
| ------ | ---- | -------- | ----------- |
|  oid           |  text              |  not null   | |
|  classifierid  |  integer           |  not null   | |
|  ceph_prob     |  double precision  |             | |
|  dsct_prob     |  double precision  |             | |
|  eb_prob       |  double precision  |             | |
|  lpv_prob      |  double precision  |             | |
|  rrl_prob      |  double precision  |             | |
|  sne_prob      |  double precision  |             | |
|  other_prob    |  double precision  |             | |
|  object_id     |  integer           |             | |


## 6. xmatch

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
|  oid        |  character varying(12)  |             | |
|  catalogid  |  character varying(15)  |             | |
|  cid        |  character varying(40)  |             | |
|  object_id  |  integer                |             | |

## 7. class

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
|  id      |  integer                |             | |
|  name    |  character varying(15)  |             | |


## 8. crtsnorth

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
|  Catalina_Surveys_ID  |  text              |             | |
|  Numerical_ID         |  bigint            |             | |
|  V_(mag)              |  double precision  |             | |
|  Period_(days)        |  double precision  |             | |
|  Amplitude            |  double precision  |             | |
|  Number_Obs           |  integer           |             | |
|  Var_Type             |  integer           |             | |
|  ra                   |  double precision  |             | |
|  dec                  |  double precision  |             | |

## 9. crtssouth

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
|  SSS_ID        |  text              |             | |
|  Numerical_ID  |  bigint            |             | |
|  ra            |  double precision  |             | |
|  dec           |  double precision  |             | |
|  Period        |  double precision  |             | |
|  V_CSS         |  double precision  |             | |
|  Npts          |  integer           |             | |
|  V_amp         |  double precision  |             | |
|  Type          |  integer           |             | |

## 10. asassn

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
| ASAS-SN Name                |  text              |             | |
|  Other Names                 |  text              |             | |
|  LCID                        |  integer           |             | |
|  ra                          |  double precision  |             | |
|  dec                         |  double precision  |             | |
|  Mean VMag                   |  double precision  |             | |
|  Amplitude                   |  double precision  |             | |
|  Period                      |  double precision  |             | |
|  Type                        |  text              |             | |
|  Url                         |  text              |             | |
|  Reference                   |  text              |             | |
|  Dist                        |  double precision  |             | |
|  Parallax                    |  double precision  |             | |
|  Parallax Error              |  double precision  |             | |
|  Gmag                        |  double precision  |             | |
|  Bpmag                       |  double precision  |             | |
|  Rpmag                       |  double precision  |             | |
|  Jmag                        |  double precision  |             | |
|  Hmag                        |  double precision  |             | |
|  Kmag                        |  double precision  |             | |
|  W1mag                       |  double precision  |             | |
|  W2mag                       |  double precision  |             | |
|  W3mag                       |  double precision  |             | |
|  W4mag                       |  double precision  |             | |
|  BP-RR                       |  double precision  |             | |
|  J-K                         |  double precision  |             | |
|  W1-W2                       |  double precision  |             | |
|  W3-W4                       |  double precision  |             | |
|  Sllk Statistic              |  double precision  |             | |
|  RF Regression Score         |  double precision  |             | |
|  Classification Probability  |  double precision  |             | |
|  Epoch (HJD)                 |  double precision  |             | |

## 11. tns

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
|  Name                  |  text                         |             | |
|  RA_orig               |  text                         |             | |
|  DEC_orig              |  text                         |             | |
|  Obj. Type             |  text                         |             | |
|  Redshift              |  double precision             |             | |
|  Host Name             |  text                         |             | |
|  Host Redshift         |  double precision             |             | |
|  Discovering Group/s   |  text                         |             | |
|  Classifying Group/s   |  text                         |             | |
|  Associated Group/s    |  text                         |             | |
|  Disc. Internal Name   |  text                         |             | |
|  Disc. Instrument/s    |  text                         |             | |
|  Class. Instrument/s   |  text                         |             | |
|  TNS AT                |  integer                      |             | |
|  Public                |  integer                      |             | |
|  End Prop. Period      |  date                         |             | |
|  Discovery Mag         |  double precision             |             | |
|  Discovery Mag Filter  |  text                         |             | |
|  Discovery Date (UT)   |  timestamp without time zone  |             | |
|  Sender                |  text                         |             | |
|  Ext. catalog/s        |  text                         |             | |
|  ra                    |  double precision             |             | |
|  dec                   |  double precision             |             | |
|  aitoff_x              |  double precision             |             | |
|  aitoff_y              |  double precision             |             | |

## 12. linear

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
|  LINEARobjectID  |  bigint            |             | |
|  LCtype          |  integer           |             | |
|  P               |  double precision  |             | |
|  A               |  double precision  |             | |
|  mmed            |  double precision  |             | |
|  stdev           |  double precision  |             | |
|  rms             |  double precision  |             | |
|  Lchi2pdf        |  double precision  |             | |
|  nObs            |  integer           |             | |
|  skew            |  double precision  |             | |
|  kurt            |  double precision  |             | |
|  LR              |  double precision  |             | |
|  CUF             |  integer           |             | |
|  t2              |  integer           |             | |
|  t3              |  integer           |             | |
|  ra              |  double precision  |             | |
|  dec             |  double precision  |             | |
|  oType           |  integer           |             | |
|  nS              |  integer           |             | |
|  rExt            |  double precision  |             | |
|  u               |  double precision  |             | |
|  g               |  double precision  |             | |
|  r               |  double precision  |             | |
|  i               |  double precision  |             | |
|  z               |  double precision  |             | |
|  uErr            |  double precision  |             | |
|  gErr            |  double precision  |             | |
|  rErr            |  double precision  |             | |
|  iErr            |  double precision  |             | |
|  zErr            |  double precision  |             | |

## 13. magref

// Insert description

| Column         | Type             | Modifier | Description |
| -------------- | ---------------- | -------- | ----------- |
|  object_id  |  integer           |             | |
|  oid        |  text              |             | |
|  fid        |  integer           |             | |
|  rcid       |  integer           |             | |
|  field      |  integer           |             | |
|  magref     |  double precision  |             | |
|  sigmagref  |  double precision  |             | |
|  corrected  |  boolean           |             | |
