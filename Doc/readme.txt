
ArcB: a GIS tool for modelling annual difusse infiltration on a plot scale

Salvador España, Francisco J. Alcalá, Ángela Vallejos, Antonio Pulido-Bosch.

Contact:
España, S. 
salvaes@ual.es
Universidad de Almería
04012 Almería, Spain


 
ArcB is a GIS tool for modelling annual diffuse infiltration (RP) from precipitation (P) on a plot scale that uses ArcObjects as 
the programming language to incorporate equations and boundary conditions for the water balance consistency. Because detailed
weather, soil, and vegetation data are often missing, ArcB uses well-known non-global models such as Hargreaves for daily potential 
evapotranspiration and Budyko for annual actual evapotranspiration (EA), as well as the SCS Curve Number (CN) procedure for 24-h plot runoff (RO). 
Annual RP is quantified as the difference in annual P, EA, and RO.

Usage Tips:

Operation of ArcB includes 6 steps and 4 hydrological boundary conditions programmed to respect the numerical and conceptual consistency of the soil water budget (see Fig. 2 in ArcB_doc).

(1) Daily EP calculation using Hargreaves’ model (1994), by using input data for Td, Id, and Ad and other parameters 
(2) Annual EA calculation using Budyko’s model (1974), by using annual EP data ? as the sum of the above daily EP ? and the input data for annual P 
(3) Correction of the above annual EA by using the experimental CEA value
(4) Daily RO calculation for each rainy day by means of the CN procedure using the input data for 24-h P and CNII values
(5) Annual RO as the sum of daily RO
(6) Annual RP as the difference in annual P, EA, and RO. 


Using ArcB

1.	Open ArcCatalog and copy the ArcB folder in you hard drive.
2.	Add ArcB Toolbox to ArcToolbox list. 
3.	Create 2 input tables P and P_d. 
4.	Open ArcB in ArcCatalog and insert input tables (P and P_d), parameters (CNII and CEA) and geodatabases (ArcB_curr and ArcB_scra). Choose X (X_UTM) and Y (Y_UTM) fields and select the spatial reference.
5.	Run the model.
6.	ArcB creates 2 output files, 1 table and 1 .shp: 
			•	RO_RP: Annual values of  EP, EA, RO, and RP
			•	ER_RT_XY: Shapefile (point) with the meteorological station and annual values of  EP, EA, RO, and RP.
