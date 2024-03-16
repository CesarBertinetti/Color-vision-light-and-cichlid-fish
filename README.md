# Color-vision-light-and-cichlids

Interactive Notebook for Repeated Divergence in Opsin Gene Expression Mirrors Photic Habitat Changes in Rapidly Evolving Crater Lake Cichlid Fishes


The datasets associated with this code can be found in https://datadryad.org/stash/share/gzH2CvhEtYRoc_bNWt-R4eJ3UnGCPdPYH19vI3hCNoQ

The code provided here is required to perform the analysis associated with the manuscript "Repeated Phenotypic Divergence in Visual Sensitivity Mirrors Photic Habitat Changes in Rapidly Evolving Crater Lake Cichlid Fishes"


The R Markdown interactive notebook includes a step-by-step description of the different analyses.

This Color-vision-light-and-cichlids_readme.txt file was created by Cesar Bertinetti on 2022-Oct-15 


GENERAL INFORMATION

1. Title of Dataset: Repeated Phenotypic Divergence in Visual Sensitivity Mirrors Photic Habitat Changes in Rapidly Evolving Crater Lake Cichlid Fishes


2. Author Information
	A. First Author
		Name: Cesar Bertinetti
		Institution: University of Notre Dame, Dpt. Biology
		Address: 299 Galvin Life Science Center, Notre Dame, IN, 46556, US
		Email: cbertinetti@hotmail.com

	B. Correspond Author 
		Name: Julián Torres-Dowdall
		Institution: University of Notre Dame, Dpt. Biology
		Address: 216 Galvin Life Science Center, Notre Dame, IN, 46556, US
		Email: torresdowdall@nd.edu

	C. Alternate Contact Information
		Name: Axel Meyer
		Institution: University of Konstanz, Dpt. Biology
		Address: Universitätstrasse 10, 78464, Germany
		Email: axel.meyer@uni-konstanz.de

3. Date of data collection: January-February 2018 

4. Geographic location of data collection: 

Central America, Nicaragua, 10 locations: Lake Nicaragua (Isletas), Lake Managua, Lake Apoyo, Lake Xiloá, Lake Asososca Managua, Asososca León, Lake Masaya, Lake Tiscapa and Río San Juan (El Castillo)


5. Information about funding sources that supported the collection of the data: This work was mainly supported by an European Research Council Advanced Grant (ERC, grant number 293700-GenAdapt) to A.M., the Deutsche Forschungsgemeinschaft (DFG, grant number TO 914/2-1) to J.T.D and the Young Scholar Fund of the University of Konstanz (grant number FP 794/15) to J.T.D.


SHARING/ACCESS INFORMATION

1. Licenses/restrictions placed on the data: Attribution 4.0 International (CC BY 4.0)
2. Recommended citation for this dataset:  DRYAD DOI


DATA & FILE OVERVIEW

1. File List: 

- RawIrradiance.zip; contains all measurements for each location. The name of the single txt files consists of "lightorientation_depth_AbsoluteIrradiance_date.txt". Only two columns, wavelength (nm) and irradiance (mW/cm²/nm).

- OpsinExpression.zip; contains raw opsin gene expression data obtained via qPCR for all specimens ("GeneExpression-CtValues.csv"). Csv files contain first column "Location", "ID", "Probe", "Species", Ct-Values for six opsin genes (sws1,sws2b,sws2a,rh2b,rh2a,lws) and two housekeeping genes (imp2, gapdh). Samples marked as "JTD2017" are based on Torres-Dowdall et al. (2017). *Rapid and Parallel Adaptive Evolution of the Visual System of Neotropical Midas Cichlid Fishes.* Mol Biol Evol, 34 (10), s. 2469–2485. doi:10.1093/molbev/msx143. 
The proportional opsin gene expression ("P_opsin") and the predicted sensitivity indices (PSI_chromophore) are reported for wild-caught and lab specimens in "Proportional Expression-wild.csv" and "ProportionalExpression-lab.csv" respectively.

- PhoticParameters.csv; contains output photic parameters extracted from processing raw irradiance data. Following columns are found: "P50": LambdaP50, photon distribution(nm); "Band":Spectral Bandwidth, spectral interval where 25-75% of the photons are found (nm), wavelengths between "P75" and "P25": LambdaP50,; "d":Depth, consists of one letter (d=downwelling, s=sidewelling, u=upwelling) followed by number representing the meter below water surface; "lux": percentage of total amount of photons compared to 0 m (15cm below water surface; "loc":location site where the data was collected.  

- SpectralSensitivity.zip; contains files with median ("med") and mean sensitivity of each population ("Sens_Pop.csv") and individual spectral sensitivities within those ("SensitivityCurves-Individuals.csv"). "Sens_Pop.csv" consists of first column "wl": Wavelength (nm) followed by media("_med") and mean("_mean") sensitivity for each location. The columns in "SensitivityCurves-Individuals.csv" consisting of the location name followed by the fish id consisting of one letter and one number. Abbreviation used "asman" (As.Managua), "sj" (River San Juan), "asleon" (As. Leon), "lknic" (Lake Nicaragua) and "lkman" (Lake Managua). The file name provides information about chromophore usage, either A2, A1 or 50% A1:A2 ("Amix), used to generate the curves. "ChangeSensitivity.csv" contains the pairwise comparisons between derived individual sensitivities and median source sensitivity.

- CorrelationDatasets.zip; contains the changes in photic conditions and visual sensitivity among source-derived populations pairs as well as the parameters used in the linear regression model with predicted sensitivity index as response variable of photic and rearing conditions. The files "ChangeDownIrradiance~ChangeSensitivity.csv", "ChangeSideIrradiance~ChangeSensitivity.csv", "ChangeTransmission~ChangeSensitivity.csv" contain the shift in spectral irradiance (either downwelling, sidewelling or spectral attenuation coefficient, respectively), identified with "_SS" column names, and spectral sensitivity ("_SI") in each location for different chromophore usage.  "CorrelationCoeficients.zip" contains the Pearson's correlation coefficients and the adjusted p-values for each individual in each location for downwelling ("Down"), sidewelling ("Side") and spectral attenuation coefficient ("Kd"). Finally, "Linear Mixed-Effect Model Dataset.csv" contains the predicted sensitivity index (PSI) for each individual, the respective values on the composite axis of photic conditions calculated via PCA and the origin of the sample either from "wild" or "lab" rearing conditions.

2. Relationship between files, if important: 

RawIrradiance.zip is used to generate PhoticParameters.zip

OpsinExpression.zip is to generate SpectralSensitivty.zip

RawIrradiance.zip, PhoticParameters.zip and SpectralSensitivity.zip are combined to generate CorrelationDatasets.zip

For the methods and tools used to generate the data please refer to "ManuscriptCode.html" which contains the code and instructions to replicate the analysis in R Software. 

