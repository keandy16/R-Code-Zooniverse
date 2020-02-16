# R-Code-Zooniverse
Zooniverse Data Processing 

This repository will contain the R Code I used to upload the photos to Zooniverse as well as analyse the data 
after photos have been classified.

To Use Before Uploading to Zooniverse:
1. Use "Extract_Image_Metadata_KA.Rmd" to process assign events to the photos. The photos should have already been run through the command line to have uniform name, size, and a csv file to be uploaded to R.
2. Run the DF output from Step 1 through "Make_Manifest_KA.Rmd" to get a table showing photo order within the events.
3. The file "Extract_Images_Metadata_Date_Issues.Rmd" assigns events to photos that have the incorrect dates/camera date malfunctions.

After Photo Data has been Extracted from Zooniverse:
1. "cleaning_dataKA.Rmd" has post-processing code that organizes the data generated from Zooniverse into a working format in R.
2. "Zooniverse_Modifications.Rmd" is attempting to format the data frame so that it is similar to the format from Chapter 5 and the WildID people. This still needs some editing (particularly the part on Jaccard Index).
3. "DiversityIndices_KA.Rmd" calculates the Shannon and Simpson Diversity indices and works just fine. 
4. "Naïve_Occupancy_Final.Rmd" attempts naïve occupancy but needs some work. 
5. "RAI_calculations.Rmd" attempts RAI calculation but needs some work. 
6. "Species_Accumulation_Curve.Rmd" works but I'm not sure it is the correct calculation.
