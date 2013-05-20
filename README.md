arcpyWhereAmI
=============

Find a layer in a map document that references the input featureclass or shapefile

#Purpose

 This tool helps solve the problem associated with deleting a featureclass or shapefile.
 Sometimes when you delete a dataset you don't know if that broke a layer a MXD.
 This tool will indicate if a dataset is a layer source.
 
# Technical Details

 The script uses the os.walk function to gather the sub-folders from the the starting location.
 A for loop is used to iterate through all the sub-folders that have been gathered.
 The workspace environment setting is reset for every folder and the arcpy.ListFiles() gathers all the MXD's.
 Arcpy mapping is used to open the mapdocument and loop through all the layers.
 When a layer is found to have the same source, it is added to a python dictionary to track the result.
 When it's done the dictionary is looped on to write out the results.
 

#How to run

###Inputs

+ Featureclass to find

  * C:\DemoData\PYTH_10_1\Running_scripts\Wilson.gdb\Wilson_Schools

  > This is the dataset that you are interested in finding out where it exists in file structure and which
  > Map document it is in. 

+ Path to a file to track results

  * C:\DemoData\Data\Where\findResults.txt

  > this file will be created to store where all the map documents are located.
  > Each result represents a map document that has a layer thats source is the same as the input
