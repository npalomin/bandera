| STEP| TOOL          | ACTION  |
| ----|---------------|---------|
| 1   | Export in Catalog |Right click on file (geojson) and export to gdb|
| 2   | Model Builder |Calculate mid point Feature Vertices to Points|
| 3   | Project | Convert to UTM if neccesary
| 4   | IDLE |Create Transect lines with python script (link data features to gdb)|
| 5   | Add Geometry Attributes| Create LINE_START_MID_END for Transect|
| 6   | Add Field & Field Calculator| slope Type Float VB Script (y1-y2) / (x1-x2)|
| 7   | Add Field & Field Calculator| radians Type Float Python radians = math.atan(!slope!)|
| 8   | Add Field & Field Calculator| degrees Type Float Python degrees = (180/math.pi)* !radians!|
| 9   | Add Field & Field Calculator| heading Type Float VB Script heading = 360 - [degrees]|
|10   | 
