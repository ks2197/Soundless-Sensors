
# Soundless Sensors
This repository contains an algorithm that employs linear regression to analyze all auxiliary channels potentially containing information about noise sources in LIGO. The aim is to identify a small, useful subset for reconstructing variations in LIGO’s astrophysical range

# What is LIGO?

The Laser Interferometer Gravitational-Wave Observatory (LIGO) revolutionized the realm of gravitational-wave astronomy in 2015 when it observed the fusion of binary black holes in the GW150914 system. Subsequently, LIGO and Virgo have witnessed numerous black hole mergers. In 2017, LIGO and Virgo introduced gravitational-wave multi-messenger astronomy with the revelation of the binary neutron star collision GW170817, promptly disseminating its celestial origin, facilitating follow-up observations by the astronomical community. These groundbreaking achievements, involving the precise measurement of minuscule spacetime alterations induced by astrophysical gravitational waves, resulted from years of painstaking research and development that culminated in observatories possessing unrivaled sensitivity.

LIGO Hanford (H1) and LIGO Livingston (L1) are intricate interferometric detectors spanning kilometers in scale. Their capacity to detect gravitational waves is restricted by sources of interference originating within the instruments and their surroundings. An established yardstick for this sensitivity is the "binary-neutron-star (BNS) range," denoting the distance at which a single detector could perceive the convergence of a pair of neutron stars, each with a mass of 1.4 solar masses, while maintaining a signal-to-noise ratio of 8. During LIGO's initial two observation campaigns, O1 and O2, the reach of each detector exhibited substantial fluctuations on both short-term and hourly intervals, often fluctuating by substantial margins.

Uncovering and mitigating the causes behind these variations, to maximize the detection range, would lead to superior signal-to-noise observations and a substantial upsurge in the volume of celestial events observed, since the accessible spatial volume is proportionate to the cube of the range. The operation of LIGO detectors at the requisite sensitivity for gravitational-wave detection necessitates the implementation of numerous control loops and an array of sensors for meticulous oversight and management of the instrumentation and surrounding conditions. The myriad channels continuously recording data from these sensors enable investigations into irregular shifts in detector sensitivity. However, owing to the intricate nature of the system, the count of auxiliary sensor channels stands at approximately 500,000. Scrutinizing such an extensive dataset to ascertain which sensors are most closely linked to fluctuations in the detection range presents a formidable yet indispensable challenge.

# Algorithm
Here are the steps for the algorithm used to identify correlations between the range of each LIGO detector and LIGO's auxiliary channels, along with the introduction of lasso regression for improved results:

Step 1: Data Preparation
Collect the binary neutron star range of LIGO, sampled once per minute.
Gather minute trends of all or a selected subset of LIGO's auxiliary channels.

Step 2: Calculate Correlation Coefficients
For each auxiliary channel, compute both the Spearman and Pearson correlation coefficients with the binary neutron star range.
Calculate these coefficients to measure the strength and direction of the correlation between the channel's data and the range data.

Step 3: Rank Channels
Produce a webpage that ranks the auxiliary channels based on their highest overall correlation coefficients.
The webpage should include time series overlays and correlation scatter plots for each channel to aid in visualization.

Step 4: Assess Simple Algorithm
Acknowledge the limitations of the simple algorithm: It may highlight groups of channels related to sensitivity fluctuations but can be less interpretable due to the high number of auxiliary channels.

Step 5: Introduce Lasso Regression
Opt for lasso regression to build a model for the range using a smaller, ranked list of auxiliary channels rather than the exhaustive list.
Lasso regression is chosen because it can identify channels linked to noise sources driving range variations.

Step 6: Model Building
Describe the process of using lasso regression to create a model for the range based on the selected auxiliary channels.
The model aims to capture the main drivers of range fluctuations.

Step 7: Channel Clustering
Use the Pearson correlation coefficient to compare the small set of channels chosen by lasso with all other channels.
Identify "clusters" of channels that are highly correlated with the channels used in the model.
These clusters may represent groups of channels linked to specific phenomena influencing the range.
By implementing these steps, the algorithm can provide a more efficient and interpretable means of identifying correlations in LIGO data and isolating key factors contributing to range fluctuations.



