interp_IB_response_ICESat2_ATL11.py
===================================

- Calculates inverse-barometer (IB) responses for correcting ICESat-2 annual land ice height data
- Calculates IB responses for both along-track and across-track locations
- Can use mean sea level pressure outputs from [ERA-Interim](http://apps.ecmwf.int/datasets/data/interim-full-moda), [ERA5](http://apps.ecmwf.int/data-catalogues/era5/?class=ea) and [MERRA-2](https://gmao.gsfc.nasa.gov/reanalysis/MERRA-2/) reanalyses

#### Calling Sequence
```bash
python interp_IB_response_ICESat2_ATL11.py --directory <path_to_directory> --reanalysis <model> input_file
```
[Source code](https://github.com/tsutterley/read-ICESat-2/blob/main/scripts/interp_IB_response_ICESat2_ATL11.py)

#### Inputs
1. `input_file`: input ICESat-2 ATL11 file

#### Command Line Options
- `-D X`, `--directory X`: Working data directory
- `-R X`, `--reanalysis X`: Reanalysis model to run
    * `'ERA-Interim'`
    * `'ERA5'`
    * `'MERRA-2'`
- `-m X`, `--mean X`: Start and end year range for mean
- `-d X`, `--density X`: Density of seawater in kg/m<sup>3</sup>
- `-C`, `--crossovers`: Run ATL11 Crossovers
- `-V`, `--verbose`: Output information about each created file
- `-M X`, `--mode X`: Permission mode of output file