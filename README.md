Spitzer Gaussian Process Pipeline
---

In Development
---

Inspired by Evans et al 2015 (http://adsabs.harvard.edu/abs/2015MNRAS.451..680E) This Pipeline implements the use of Gaussian Processes (www.gaussianprocess.org) for decorrelating the Spitzer instrumental noise profiles.  

- The primary noise profile for Spitzer is known as the "Intrapixel Effect" or "InstraPixel Sensitivity Variations (IPSV)".   - This noise profile varies the flux read out by the detector as a function of the position on the detector.
- Secondary noise profiles vary the flux as a function of the PSF width -- via the "noise pixel" (http://adsabs.harvard.edu/abs/2013ApJ...766...95L).
- A subtler noise profile is related to periodic battary warming that introduces a short period saw pattern into the flux

By using a set of Gaussian Process kernels, we will be able to address each of these correlations in the data, in order to robustly fit a covariance model to the noise simulataneously with the astrophysical model to the astrophysical signal ("data").
