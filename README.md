arcpyWhereAmI
=============

Find a layer in a map document that references the input featureclass or shapefile

#Purpose


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
