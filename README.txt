# Enter your text here
How to use PCell from 'Jaseung_Lib' library

0. File -> Load Layer Properties -> Select 'LayerPropertyFile_Jaseung' file (This file has pre-defined layers for my convience.

0.1 Mactor -> Macro Development -> Click on 'Python' tab -> Inside 'Python' tab, right click -> Add Location -> Select folder 'Klayout-JK' -> If 'Run Macro' pop-up windows appears, click 'yes' to run macros. -> close

1. PathToCPW:
- This macro converts a path to CPW. 
- First, draw a path, and select it.
- Second, go to Edit->Selection->Convert To Pcel.
- Third, select "PathToCPW".

- By defaul, four polygons are created and placed into three layers.
- Original path, rounded path ==> CPW path layer
  Keepout ==> Keepout layer
  Image ==> Image layer

2. MakeCPW_standalone:
- It creates a PCell for CPW alone. To use it, 
- First, click "Instance" icon in the toolbar.
- Second, select "Jaseng_Lib" from 'library' pull-down list.
- Third, select "MakeCPW" cell from 'cell' pull-down list.
- Fourth, click on "PCell" tab to enter parameters.

3. creatFluxTrap:
- Flux trap arrays are created in a selected cell. 
- Need a cell called 'fluxtrapsinglecell', which has only 4x4um^2 square in flux trap layer.
- Need to put x and y center positions of the cell in the CHIP coordinate in the code.
- A cell must not have child cells.
