
# Soundless Sensors
This repository contains an algorithm that employs linear regression to analyze all auxiliary channels potentially containing information about noise sources in LIGO. The aim is to identify a small, useful subset for reconstructing variations in LIGO’s astrophysical range

# What is LIGO?

The Laser Interferometer Gravitational-Wave Observatory (LIGO) dramatically opened the field of gravitational-wave astronomy in 2015 by observing the merging
binary black hole system GW150914.LIGO and Virgo have since observed several more black hole mergers. In 2017, LIGO and Virgo debuted gravitational-wave multi messenger astronomy with the discovery of the binary neutron star merger GW170817 and rapidly reported its source’s location, leading to electromagnetic observation by the astronomical community. These breakthroughs, measurements of the incredibly minute changes in spacetime caused by astrophysical gravitational waves, were the direct result of decades of research and development leading to observatories with unprecedented sensitivity.

LIGO Hanford (H1) and LIGO Livingston (L1) are highly complex kilometer-scale laser interferometric detectors. Their sensitivity to gravitational waves is limited
by sources of noise in the instruments and their environments. A common benchmark of this sensitivity is the “binary-neutron-star (BNS) range”, which is defined as the distance at which a single detector could observe the coalescence of a pair of 1.4 solar mass neutron stars with a signal-to-noise ratio of 8. During LIGO’s first two observing runs, O1 and O2, the range of each detector varied significantly on minute and hourly timescales, often by tens of percent. 

Identifying and removing the causes of this variation to maximize the range would lead to higher signal-to-noise observations and would dramatically increase the number of observations because the volume of space accessible is proportional to the cube of the range. Operating the LIGO detectors at the sensitivity needed for gravitational-wave detection requires a large number of control loops and sensors to precisely control and monitor the instrumentation and environment. The channels that continually record information from these sensors enable investigations into problematic variations in the sensitivity of the detector. However, due to the complexity of the system, the number of auxiliary sensor channels is roughly 500,000. Searching through such a large amount of data to determine which sensors are most highly correlated with variations in the range is a formidable yet important challenge.



