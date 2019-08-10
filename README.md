# Useful python codes and macros in Klayout for drawing superconducting circuits

Here I keep python codes and macros for Klayout that I used in designing a photomask layout. The general design rule in creating a mask using Klayout is decribed in *chip_design_run.odt*. Below, I explain how to use PCells and macros.

### Installing
1. Download *Klayout-JK.zip* and uncompress it.
2. In Klayout, Macro -> Macro Development -> Click on "Python" tab -> Inside "Python" tab, right click -> Add Location -> Select folder *Klayout-JK* -> If "Run Macro" pop-up windows appears, click "yes" to run macros. -> close

### How to use PCell from "Jaseung_Lib" library
0. (Recommended) File -> Load Layer Properties -> Select *LayerPropertyFile* file (This file has pre-defined layers with names.)

1. PathToCPW  
   This macro converts a path to CPW, not a stand-alone PCell. To use it,  
   First, draw a path, and select it.     
   Second, go to Edit -> Selection -> Convert To Pcel.  
   Third, select "PathToCPW".  

   By defaul, four polygons are created and placed into three layers.
   
   Original path ==> OUTLINE layer
   KEEPOUT ==> KEEPOUT layer  
   IMAGE ==> IMAGE layer  

2. MakeMeanderCPW_standalone  
   This macro creates a PCell for CPW alone. To use it,   
   First, click "Instance" icon in the toolbar.  
   Second, select "Jaseng_Lib" from 'library' pull-down list.  
   Third, select "MakeMeanderCPW" cell from 'cell' pull-down list.  
   Fourth, click on "PCell" tab to enter parameters.  

3. creatFluxTrap  
   Flux trap arrays are created in a selected cell.     
   Need a cell called "fluxtrapsinglecell", which has only 4x4um^2 square in flux trap layer.  
   Need to put x and y center positions of the cell in the CHIP coordinate in the code.  
   A cell must not have child cells.  
