# ExampleErcs
List of suitable example ercs. Please specify which output type it creates (map/timeseries) and what are possible parameters that can be changed (type of value, allowed ranges, default value, etc.).

## ERC Summaries:

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
  4. (-) Deals with reservoir operations (no prominent geospatial component)

### Aspacetimemodel

* File: ./Aspacetimemodel/figure1_interactive.Rmd
* Type of Output: Map
* Parameter #1: Intensity
* Parameter #1 Type: Integer
* Parameter #1 Range: (1,50)
* Parameter #1 Step size: 1
* Parameter #1 Default Value: 30
* Comments:
  1. (-) The plotted map doesn't look interesting.
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
  1. (-) Does not have a strong geospatial component.
  2. (-) The plots (Fig. 2 & Fig. 3) are not a good timeseries for our project (only 7 observations)
  3. (+/-) 5 data series in each plot
  4. (-) It seems some functions are from packages which are not loaded in the Markdown.

### Dates and Times Made Easy with lubridate

* File: ./Dates and Times Made Easy with lubridate/Dates and Times Made Easy with lubridate.Rmd
* Type of Output: Timeseries
* Parameter #1: (?)
* Parameter #1 Type: NA
* Parameter #1 Range: NA
* Parameter #1 Step size: NA
* Parameter #1 Default Value: NA
* Comments:
  1. (-) Probably not suitable - *illustrates* a particular package.
  2. (-) Does not have a geospatial component.
  3. (+) Plot (Fig. 5) is a good time series
  4. (+) Has other time series plots too, but they are not probably what we are looking for.

### LAND-SE a software for statistically based landslide

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
