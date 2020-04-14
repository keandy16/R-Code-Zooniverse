# R-Code-Zooniverse
Zooniverse Data Processing 

This repository will contain the R Code I used to upload the photos to Zooniverse as well as analyse the data 
after photos have been classified.

To Use Before Uploading to Zooniverse:
1. Use "Extract_Image_Metadata_KA.Rmd" to process assign events to the photos. The photos should have already been run through the command line to have uniform name, size, and a csv file to be uploaded to R.
2. Run the DF output from Step 1 through "Make_Manifest_KA.Rmd" to get a table showing photo order within the events.
3. The file "Extract_Images_Metadata_Date_Issues.Rmd" assigns events to photos that have the incorrect dates/camera date malfunctions.

After Photo Data has been Extracted from Zooniverse:
1. "Flatten_data_final.Rmd" flattens JSON data from the csv file pulled directly from Zooniverse exports and transforms it into a workable format in R. For this code to work, source the associated functions in "our_functions.R"
2. "Testing_multiple_classifications.Rmd" should aggregate votes for different classifications and will return a data frame with the top n species for each subject.
3. "CheckTheseList.Rmd" separates subjects where classifiers did not have a clear concensus with voting. We considered a clear classification to have a propclass (proportion of classifiers) of 0.80 of higher. The output of this is a 'checkthese' csv for researchers to reclassify manually as well as a csv file with the subjects whose classifications were deemed certain.
4. "cleaning_data.Rmd" has post-processing code that organizes the data generated from the previous R markdowns. This script joins forest data and deployment dates to the classification data in order to calculate species accumulation curve, species richness, diversity, and other ecological measurements. 
5. "Species_Accumulation_Curve.Rmd" works but I'm not sure it is the correct calculation.
6. "Zooniverse_Modifications.Rmd" is attempting to format the data frame so that it is similar to the format from Chapter 5 and the WildID people. This still needs some editing (particularly the part on Jaccard Index).
7. "DiversityIndices_KA.Rmd" calculates the Shannon and Simpson Diversity indices and works just fine. 
8. "Naïve_Occupancy_Final.Rmd" attempts naïve occupancy but needs some work. 
9. "RAI_calculations.Rmd" attempts RAI calculation but needs some work. 
