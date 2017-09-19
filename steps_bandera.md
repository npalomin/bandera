| STEP| TOOL          | ACTION  |
| ----|---------------|---------|
| 1   | Export in Catalog | Right click on file (geojson) and export to gdb|
| 2   | Model Builder | Calculate mid point Feature Vertices to Points|
| 3   | Project | Convert to UTM if neccesary
| 4   | IDLE |Create Transect lines with python script (link data features to gdb)|
| 5   | Add Geometry Attributes| Create LINE_START_MID_END for Transect|
| 6   | Add Field & Field Calculator| slope Type Float VB Script (y1-y2) / (x1-x2)|
| 7   | Add Field & Field Calculator| radians Type Float Python radians = math.atan(!slope!)|
| 8   | Add Field & Field Calculator| degrees Type Float Python degrees = (180/math.pi)* !radians!|
| 9   | Add Field & Field Calculator| heading Type Float VB Script heading = 360 - [degrees]|
|10   | Feature To Polygon| Convert lines (manzanas) to polygon|
|11   | Intersect |Intersect polygon with Transect (Output type LINE) *with the same projection*|
|12   | Intersect |Intersect line(kerb) with Transect (Output type POINT) *with the same projection*|
|13   | Add XY Coordinatesa | calculate x, y for intersection points|
|14   | Table To Excel |Save Attribute Table to excel|



|12   | Table To Excel |Save Attribute Table to excel|
|13   | Export as CSV |Save excel to csv file|
|14   | Pyton Pandas Jupyter |import pandas as pd / %matplotlib inline|
|15   | Pyton Pandas Jupyter |canyon = pd.read_csv('N:\\bandera\GIS\Man_int_tran_merge_UTM.csv')|
|16   | Pyton Pandas Jupyter |canyonsum = df.groupby('FID_Export_CS_transects').sum()|
