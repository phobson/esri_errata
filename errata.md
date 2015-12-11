# Esri's documentation errors

## Rasters
[Version 10.2 rasters](http://goo.gl/67NwDj) says `Raster.path` is the "full path and filename". 

#### What it should say
It's just the path to the folder.

#### Fix
You need to do `os.path.join(raster.path, raster.name)` to get actually get the full path & filename.

An even more direct alternative would be to use `raster.catalogPath`.

## Toolboxes
[Version Pro and earlier toolboxes] (https://pro.arcgis.com/en/pro-app/arcpy/classes/parameter.htm)
claimed that you set the parameter dependendencies with a list of integers.

#### What it should say
This is incorrect. You need to use either a list of integers *as strings* or the parameter names.

#### Fix
```python
param2.parameterDependencies = ["1"] # sets the dep. of param2 to the parameter at index 1
## OR
param2.parameterDependencies = [param1.name]
```
#### See also:
http://gis.stackexchange.com/questions/168353/how-to-set-parameter-dependencies-in-arcgis-python-toolboxes

## Flow Accumulation
[In ArcGIS Pro and earlier,](http://pro.arcgis.com/en/pro-app/tool-reference/spatial-analyst/flow-accumulation.htm#I_ESRI_TOOLILLUSTRATION_C94AF40DB7D149AAAF21F96B6E6CD97A) the results for the flow accumulation example are wrong.

#### Correction
http://gis.stackexchange.com/questions/63160/arcmap-10-restrict-flow-accumulation/63338#63338

#### See also:
http://gis.stackexchange.com/questions/144086/does-this-arcgis-flow-accumulation-example-have-an-error
