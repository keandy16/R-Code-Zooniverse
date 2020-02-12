# R-Code-Zooniverse
Zooniverse Data Processing 

This repository will contain the R Code I used to upload the photos to Zooniverse as well as analyse the data 
after photos have been classified.

To Use Before Uploading to Zooniverse:
1. Use "Extract_Image_Metadata_KA.Rmd" to process assign events to the photos. The photos should have already been run through the command line to have uniform name, size, and a csv file to be uploaded to R.
2. Run the DF output from Step 1 through "Make_Manifest_KA.Rmd" to get a table showing photo order within the events.
3. The file "Extract_Images_Metadata_Date_Issues.Rmd" assigns events to photos that have the incorrect dates/camera date malfunctions.

