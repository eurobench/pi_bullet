## Purposes

PI extraction codes within the BULLET testbed.
Two agorithms have been implemented: pi_bullet_walking and pi_bullet_walkingComplete.

The former extracts following PIs:
- Peak_load_left
- Peak_load_right
- RMS_load_left
- RMS_load_right
- Stance_time_left
- Stance_time_right

using following files
- subject_N_run_R_wrench_CrutchLeft.csv
- subject_N_run_R_wrench_CrutchRight.csv
- subject_N_run_R_gaitEvents.yaml.

The latter extracs Peak_load_left, Peak_load_right, RMS_load_left, RMS_load_right, Stance_time_left, Stance_time_right, Peak_load_shoulders_left, Peak_load_shoulders_right, RMS_load_shoulders_left, RMS_load_shoulders_right from subject_N_run_R_wrench_CrutchLeft.csv, subject_N_run_R_wrench_CrutchRight.csv, subject_N_run_R_gaitEvents, subject_N_run_R_wrench_ShoulderLeft.csv, subject_N_run_R_wrench_ShoulderRight.csv.

## Installation

To enable the code under octave, additional packages are needed.

```console
sudo apt-get install liboctave-dev
```

Follow [these recommendations](https://octave.org/doc/v4.2.1/Installing-and-Removing-Packages.html) to make the installation of the additional packages needed:

- [control](https://octave.sourceforge.io/control/index.html)
- [signal](https://octave.sourceforge.io/signal/index.html)
- [io](https://octave.sourceforge.io/io/index.html)
- [statistics](https://octave.sourceforge.io/statistics/index.html)

Once octave is configured:

```console
pkg load control
pkg load signal
pkg load io
pkg load statistics
```

## Usage

pi_bullet_walking:
```console
./run_pi_BulletWalking subject_N_run_R_wrench_CrutchLeft.csv subject_N_run_R_wrench_CrutchRight.csv subject_N_run_R_gaitEvents.yaml outputDir
```

pi_bullet_walkingComplete:
```console
./run_pi_BulletWalkingComplete subject_N_run_R_wrench_CrutchLeft.csv subject_N_run_R_wrench_CrutchRight.csv subject_N_run_R_gaitEvents.yaml subject_N_run_R_wrench_ShoulderLeft.csv subject_N_run_R_wrench_ShoulderRight.csv outputDir
```

## Build docker image

To be completed

## Launch the docker image

to be completed

## Acknowledgements

<a href="http://eurobench2020.eu">
  <img src="http://eurobench2020.eu/wp-content/uploads/2018/06/cropped-logoweb.png"
       alt="rosin_logo" height="60" >
</a>

Supported by Eurobench - the European robotic platform for bipedal locomotion benchmarking.
More information: [Eurobench website][eurobench_website]

<img src="http://eurobench2020.eu/wp-content/uploads/2018/02/euflag.png"
     alt="eu_flag" width="100" align="left" >

This project has received funding from the European Union’s Horizon 2020
research and innovation programme under grant agreement no. 779963.

The opinions and arguments expressed reflect only the author‘s view and
reflect in no way the European Commission‘s opinions.
The European Commission is not responsible for any use that may be made
of the information it contains.

[eurobench_logo]: http://eurobench2020.eu/wp-content/uploads/2018/06/cropped-logoweb.png
[eurobench_website]: http://eurobench2020.eu "Go to website"
