### 01.11.19 ###

Authors: 
	- Julian E. Vevik-------j.e.vevik@fys.uio.no
	- Sindre H. Kaald-------sindre.h.kaald@gmail.com
	- Tellef Storebakken----tellef.storebakken@fys.uio.no

All data are obtained with The OpenMC Monte Carlo code, v0.11.0. URL: https://docs.openmc.org/en/stable/	

A report on obtaining these plots and results are planned to be made in January 2020.

The plots in this directory are made to simulate a spherical scintillator with a diameter of 1m with a penetrating cylindrical chamber with a diameter of 10cm. All plots should have a description showing what is plotted in the plot title and/or in the filename.

Simulations were done with a simple geometry, only containing NE343 liquid scintillator and steel shielding (see the "geometry_plots" directory).

Material compositions:

	NE343 Scintillator (In this case containing 600L of NE343, doped with 0.5% Gd)
		- Density:----------1.016 g/cm3
		- C (Carbon):-------85.2534 wo
		- H (Hydrogen):-----5.8926 wo
		- N (Nitrogen):-----3.9 wo
		- O (Oxygen):-------4.454 wo
		- Gd (Gadolinium):--0.05 wo

	Stainless Steel shielding:
		- Density:----------8.03 g/cm3
		- Si (Silicon):-----0.0060 wo
		- Cr (Chromium):----0.19 wo
		- Mn (Manganese):---0.020 wo
		- Fe (Iron):--------0.684 wo
		- Ni (Nickel):------0.10 w0 


- Simulations were done with one neutron as a source in the middle of the cylindrical chamber with an isotropic angular distribution. Initial neutron energy should be shown in plots.

- All values were obtained with simulations 10 or 100 batches simulating 1000 particles. Values are normalized to number of initial particles.

- The gamma flux and neutron flux were scored with 1000 energy bins on the range (0,1e7), i.e. the flux-plots has a maximum energy uncertainty of +/- 10 keV. The flux is scored on a spheric shell on the outside of the shielding material.

- The plots trying to identify threshold values are based on classical calculations, where the neutron can transfer a maximum of 100% of its initial energy to a hydrogen when scattering elastically, and maximum of 28.6% of its energy can be transferred in a elastic scattering with carbon. According to G. F. Knoll "Radiation Detection and Measurement" page 555, an assumption can be made that on average the neutron will then transfer 50% and 14.3% of its energy when colliding with hydrogen and carbon respectively. The two plots trying to determine thresholds only then count neutrons colliding with hydrogen with an energy of 1 MeV so that it transfers 500 keV to the hydrogen, and ca 3.5 MeV and above neutrons are counted in the carbon plot so that the carbon would have received 500 keV. The resulting plots are, at least for us, hard to understand and interpret any useful information from (there might be something wrong?), so please consider this if they are going to be used.

- The leakage plots gives information about how many of the neutron escaped the detector, i.e. was not captured, but it does not give any information about how many scattering events the neutron may have gone through on the way out of the detector. A peculiar shape in high energies when using many energy measurement points was also seen, and is shown zoomed in in one of the plots.

- In the plot "Detector total (n,gamma) efficiency _ where (n,gamma) is the first reaction.png" the units says "per source particle", but it is supposed to say "% per source particle". EDIT 22.01.2020: This has been fixed
