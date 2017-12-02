# ExampleErcs
List of suitable example ercs. Please specify which output type it creates (map/timeseries) and what are possible parameters that can be changed (type of value, allowed ranges, default value, etc.).

## ERC Summaries:

`*` = Suitable

### Aquestiondrivenprocess

* File: ./Aquestiondrivenprocess/server.R, ./Aquestiondrivenprocess/ui.R
* Type of Output: Timeseries
* Parameter #1: Hedging Slope
* Parameter #1 Type: Floating point
* Parameter #1 Range: (1,3)
* Parameter #1 Step size: 0.1
* Parameter #1 Default Value: 2.0
* Parameter #2: Streamflow Sequnce
* Parameter #2 Type: Categorical
* Comments:
  1. (-) Parameter #2 implemented as a dropdown! (this can be omitted)
  2. (+/-) Produces 6 timeseries plots
  3. (+) Shiny app works out of the box!
  4. (+/-) Deals with reservoir operations

### Aspacetimemodel

* File: ./Aspacetimemodel/figure1_interactive.Rmd
* Type of Output: Map
* Parameter #1: Intensity
* Parameter #1 Type: Integer
* Parameter #1 Range: (1,50)
* Parameter #1 Step size: 1
* Parameter #1 Default Value: 30
* Comments:
  1. (-) The plotted map doesn't look interesting/suitable for this project.
  2. (+) Shiny Markdown works out of the box!
  3. (+) Deals with hurricane tracks

### BadgesToAcknowledgeOpenPractices

* File: ./BadgesToAcknowledgeOpenPractices/BadgesToAcknowledgeOpenPractices.Rmd
* Type of Output: Timeseries
* Parameter #1: Journal(?)
* Parameter #1 Type: NA
* Parameter #1 Range: NA
* Parameter #1 Step size: NA
* Parameter #1 Default Value: NA
* Comments:
  1. (-) The plots (Fig. 2 & Fig. 3) are not a good timeseries for our project (only 7 observations)
  2. (+/-) 5 data series in each plot
  3. (-) It seems some functions are from packages which are not loaded in the Markdown.

### Dates and Times Made Easy with lubridate

* File: ./Dates and Times Made Easy with lubridate/Dates and Times Made Easy with lubridate.Rmd
* Type of Output: Timeseries
* Parameter #1: (?)
* Parameter #1 Type: NA
* Parameter #1 Range: NA
* Parameter #1 Step size: NA
* Parameter #1 Default Value: NA
* Comments:
  1. (+/-) *Illustrates* a particular package.
  3. (+) Plot (Fig. 5) is a good time series
  4. (+) Has other time series plots too, but they are not probably what we are looking for.

### LAND-SE a software for statistically based landslide *

* File: ./Original/LAND-SE-master/LAND-SE_v1r0b30_20160118.R, ./Original/LAND-SE-master/LAND-SE_v1r0b32_20160923.R
* Type of Output: Map
* Parameter #1: (?)
* Parameter #1 Type: NA
* Parameter #1 Range: NA
* Parameter #1 Step size: NA
* Parameter #1 Default Value: NA
* Comments:
  1. (+) Very suitable ERC for maps!
  2. (+) Produces a lot of raw maps (TIFF, PDF) - Code can be changed to render as TIFF instead of PDF.
  3. (+/-) Produces a lot of output files (including data files, images etc.; mostly for its own internal use) amounting to >5GB (size of ./Reproduced.zip) when zipped (probably more when unpacked)
  4. (+) Output images are GeoTIFFs and has CRS information. Can be used directly to be overlayed on basemaps, if required!
  5. (+) Need to go through the text of the paper to find meaningful parameters which can be changed
  6. (+/-) Takes a long time to run completely (atleast >45 minutes) - Code can be edited to output the most relevant 2 or 3 maps.
  7. (+) Example data in the ERC as well as the code available online in GitHub at: maurorossi/LAND-SE
 * Description:
    Plots the landslide susceptibility zonation (how likely there will be a landslide in a given zone) of a region. It can be done on the basis of a region or on the basis of each pixel. The pixel-based analysis is computationally intensive and takes a lot of RAM (as per the author). However, the downside is that the primary output of interest ("./Reproduced/Example_datasets/pixel_Random_validation_entirearea/result_???_Model_Susceptibility_Map.tif") is not totally continious. So, instead we can use another output ("./Reproduced/Example_datasets/pixel_Random_validation_entirearea/result_???_Validation_Susceptibility_Map.tif") which validates the model. (??? represents the code for the algorithm used)
 * How the model works (filepaths corresponding to the region-wise implementation):
    The software, implemented in R, needs some training files ((a) a shapefile for the regions ./Original/LAND-SE-master/Example_datasets/polygon_Random_validation_entirearea/training.shp with polygon features (point features for pixel-based implementation) and (b) a tab-delimited text file ./Original/LAND-SE-master/Example_datasets/polygon_Random_validation_entirearea/training.txt with each row corresponding to the a polygon (or points) referenced by SU_ID and other columns representing variables which affect landslide), and some validation files ((a) a shapefile with polygons (or points) for which the model results will be validated ./Original/LAND-SE-master/Example_datasets/polygon_Random_validation_entirearea/validation.shp and (b) a similar tab-delimited text file ./Original/LAND-SE-master/Example_datasets/polygon_Random_validation_entirearea/validation.txt with the independent variables).
    However, as evident from the text files (training.txt and validation.txt), the independent variables (which can be used as the parameters) are not one particular value but rather a number of values for each polygon (or points). So, since it is impossible to use so many sliders in the UI, we can choose to have one slider for each of the independent variables. So, if we use the pixel-based implementation, there are 2 such variables - DEM and slope. Our sliders, can have a value which might represent the percentage change in slope and the DEM vectors (i.e. a value of "100%" on a particular slider will be the original scenario of all the values of that vector). The meaningfulness of this representation and other ideas on what will the sliders do (since the parameter is a vector) are to be explored further.

### Extracting and Enriching Ocean Biogeographic Information System

* File: ./Extracting and Enriching Ocean Biogeographic Information System/Extracting and Enriching Ocean Biogeographic Information System.Rmd
* Type of Output: Map
* Comments:
  1. Multiple maps are plotted in this Rmd file
