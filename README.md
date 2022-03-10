# convert-shp-to-csv

This tool will take a shape file (.shp), and convert it to a gridded csv file with lat/long of the
center of the grid as columns.

Any shapes that overlap this point when the shape is overlaid on to the grid will be reflected in
additional columns

## Usage:

```
usage: convert-shp-to-csv [-h] [--output-file OUTPUT_FILE] [--cell-size CELL_SIZE] shape_file

Converts a shape file (.shp) to a gridded csv file.
    

positional arguments:
  shape_file            Shape file (.shp) to convert

optional arguments:
  -h, --help            show this help message and exit
  --output-file OUTPUT_FILE, -o OUTPUT_FILE
                        Name of csv file to output
  --cell-size CELL_SIZE
                        Cell size, in lat/long segments. Default: 0.1
```

## Example output:

```
latitude,longitude,EthGLG,EthHGComb
7.4488230199999546,34.35153731999999,Unconsolidated sedimentary - Miocene to Recent (minor consolidated Alwero Sandstone),U-LM
7.4488230199999546,34.35153731999999,Igneous Volcanic,I-M/H
7.4488230199999546,34.35153731999999,Precambrian Mobile/Orogenic Belt,B-L
7.548823019999955,34.35153731999999,Unconsolidated sedimentary - Miocene to Recent (minor consolidated Alwero Sandstone),U-LM
7.548823019999955,34.35153731999999,Igneous Volcanic,I-M/H
7.548823019999955,34.35153731999999,Unconsolidated sedimentary - Miocene to Recent (minor consolidated Alwero Sandstone),U-LM
```