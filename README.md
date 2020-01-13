## Useful python macros in Klayout for drawing superconducting circuits

Here I keep python codes and macros for Klayout that I used in designing a photomask layout. The general design rule in creating a mask using Klayout is decribed in *chip_design_run.odt*. Below, I explain how to use macros.

### Install
1. Download *Klayout-JK.zip* and uncompress it. Or clone Klayout-JK repository.
2. In Klayout, Macro -> Macro Development -> Click on "Python" tab -> Inside "Python" tab, right click -> Add Location -> Select folder *Klayout-JK* -> If "Run Macro" pop-up windows appears, click "yes" to run macros. -> close

### How to create a PCell from "Jaseung_Lib" library

1. Load property file (Recommended)   
File -> Load Layer Properties -> Select *LayerPropertyFile* file 
  
2. PathToCPW  
This macro converts a path to CPW PCell. To use it,  
First, draw a path, and select it.     
Second, go to Edit -> Selection -> Convert To PCell.  
Third, select "PathToCPW".  

3. MakeMeanderCPW  
This macro creates a PCell for meander CPW alone. To use it,   
First, click "Instance" icon in the toolbar.  
Second, select "Jaseng_Lib" from 'library' pull-down list.  
Third, select "MakeMeanderCPW" cell from 'cell' pull-down list.  
Fourth, click on "PCell" tab to enter parameters.  

### How to create flux trap holes on a selected cell
1. CreateFluxTrap  
Flux trap holes are created in the selected cell instance.     
First, select a cell instance where you want to create flux trap holes.  
Second, run the CreateFluxTrap macro: Macros-> Create Flux Trap
