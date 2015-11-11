# Esri's documentation errors

## Rasters
[Version 10.2 rasters](http://goo.gl/67NwDj) says `Raster.path` is the "full path and filename". 
It's just the path.
You need to do `os.path.join(raster.path, raster.name)` to get actually get the full path.

## Toolboxes
[Version Pro and earlier toolboxes] (https://pro.arcgis.com/en/pro-app/arcpy/classes/parameter.htm)
claimed that you set the parameter dependendencies with a list of integers.
This is incorrect. You need to use either a list of integers *as strings* or the parameter names.

### See also:
http://gis.stackexchange.com/questions/168353/how-to-set-parameter-dependencies-in-arcgis-python-toolboxes

## Flow Accumulation
The example dataset for the flow accumulation function is wrong.

### See also:
http://gis.stackexchange.com/questions/144086/does-this-arcgis-flow-accumulation-example-have-an-error
