# Arrival time data for Southern California

How to obtain data

## SCEDC

Phase data is available directly forom the Southern California Earthquake Data Center
([SCEDC](https://scedc.caltech.edu/index.html)).


## ComCat

All the data from Southern California networks is also availabel in the 
ANSS comprehensive earthquake catalog ([ComCat](https://earthquake.usgs.gov/data/comcat/)).


ComCat provides a [command-line interface](https://github.com/usgs/libcomcat/blob/master/docs/cli.md)
to access event data in the catalog.

In particular the script [`getphases`](https://github.com/usgs/libcomcat/blob/master/docs/cli.md#getphases)
extracts events and associated phase arrival time data.

```console
$ com2mnf_v2.py -b -124.5 -118.2 35.7 42.3 -s 1980-01-24T00:00:00 -e 1981-01-01T00:00:00 \
  -m 3.0 8.0 -o 10 -d 0 60 -dir $destdir -contrib nc -reqnet nc -regnam "NCAL"
```
