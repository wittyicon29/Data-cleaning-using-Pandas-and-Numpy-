# Data-cleaning-using-Pandas-and-Numpy-
A Cepheid variable is a type of star that, due to some inherent instability, pulsates radially, varying in both diameter and temperature and producing changes in brightness with a well-defined stable period and amplitude. As it turns out, the period of pulsation and the Luminosity (i.e the absolute magnitude) of the Cephied are related.

We'll use data of cepheids from the Small Magallenic Cloud (SMC) obtained by a survey called Optical Gravitational Lensing Experiment (OGLE). The Small Magellanic Cloud is a dwarf galaxy satellite of the Milky Way, and distances to any star in it can be assumed to be almost constant. So the magnitudes translated directly into absolute magnitudes with some offset dependent on the distance to the SMC!

Data Cleaning

The data file given consists of 'ID', the identifier for the star, 'RA', the right ascension in HMS format; 'Decl', the declination in DMS format; 'I', the band magnitude; 'V. the V band magnitude; 'P_1', the period.

Some entries in the V and I band magnitude have a value of -99.990, so we do not want to use these stars for further analysis. Remove such entries. Further, convert the RA and Dec values to degrees from HMS and DMS respectively. You might find Pandas convenient for the above purposes.

In [15]:

#Code here

Plot the RA, Dec coordinates in a sky grid using Matplotlib. (Hint: Look up Mollweide projections in Matplotlib)

In [16]:

#Code here

P-L Diagrams

Plot the Magnitude vs log(Period) for V and bands. Observe that a linear fit can be done to obtain the period magnitude relation for each band separately. Use scipy's curve fit module to obtain the relation for both V and I band. The P-L relation is of the form

m = a log(P) + I

where m is the apparent magnitude, a is the slope, P is period and I is the intercept
