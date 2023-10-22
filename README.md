
# Soundless Sensors
This repository contains an algorithm that employs linear regression to analyze all auxiliary channels potentially containing information about noise sources in LIGO. The aim is to identify a small, useful subset for reconstructing variations in LIGO’s astrophysical range

# What is LIGO?

The Laser Interferometer Gravitational-Wave Observatory (LIGO) revolutionized the realm of gravitational-wave astronomy in 2015 when it observed the fusion of binary black holes in the GW150914 system. Subsequently, LIGO and Virgo have witnessed numerous black hole mergers. In 2017, LIGO and Virgo introduced gravitational-wave multi-messenger astronomy with the revelation of the binary neutron star collision GW170817, promptly disseminating its celestial origin, facilitating follow-up observations by the astronomical community. These groundbreaking achievements, involving the precise measurement of minuscule spacetime alterations induced by astrophysical gravitational waves, resulted from years of painstaking research and development that culminated in observatories possessing unrivaled sensitivity.

LIGO Hanford (H1) and LIGO Livingston (L1) are intricate interferometric detectors spanning kilometers in scale. Their capacity to detect gravitational waves is restricted by sources of interference originating within the instruments and their surroundings. An established yardstick for this sensitivity is the "binary-neutron-star (BNS) range," denoting the distance at which a single detector could perceive the convergence of a pair of neutron stars, each with a mass of 1.4 solar masses, while maintaining a signal-to-noise ratio of 8. During LIGO's initial two observation campaigns, O1 and O2, the reach of each detector exhibited substantial fluctuations on both short-term and hourly intervals, often fluctuating by substantial margins.

Uncovering and mitigating the causes behind these variations, to maximize the detection range, would lead to superior signal-to-noise observations and a substantial upsurge in the volume of celestial events observed, since the accessible spatial volume is proportionate to the cube of the range. The operation of LIGO detectors at the requisite sensitivity for gravitational-wave detection necessitates the implementation of numerous control loops and an array of sensors for meticulous oversight and management of the instrumentation and surrounding conditions. The myriad channels continuously recording data from these sensors enable investigations into irregular shifts in detector sensitivity. However, owing to the intricate nature of the system, the count of auxiliary sensor channels stands at approximately 500,000. Scrutinizing such an extensive dataset to ascertain which sensors are most closely linked to fluctuations in the detection range presents a formidable yet indispensable challenge.

# Algorithm




