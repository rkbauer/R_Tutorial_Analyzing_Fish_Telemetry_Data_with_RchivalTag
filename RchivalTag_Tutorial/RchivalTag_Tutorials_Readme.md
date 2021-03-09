

<p align="center">
  <img src="./img/RchivalTag_logo.svg" alt="Size Limit CLI" width="300">
</p>


<h4 align="center">An R-Package for Analyzing and Interactive Visualization of Archival Tagging Data</h4>
<h4 align="center">Package Tutorial</h4>

<p align="center">
  <a href="#author">Author</a> •
  <a href="#motivation">Motivation</a> •
  <a href="#details">Details</a> •
  <a href="#compatability">Compatability</a> •
  <a href="#references">References</a> •
  <a href="#license">License</a>
</p>


![Screenshot](./img/example.jpg)

## Author

[Dr. Robert Bauer | Fishery Biologist & Data Scientist](https://scholar.google.com/citations?hl=en&user=J-0_tdbR2tgC)

## Motivation

The idea behind the
[RchivalTag](https://github.com/rkbauer/R_Package_RchivalTag)-package
and this tutorial is to facilitate the analysis and visualization of
archival and pop-up archival tagging data within R. The package (and tutorial) focuses mainly on the following data products:

1.  Time-at-Depth (TaD) and Time-at-Temperature (TaT) Histogram data
2.  Time series data (e.g. depth and temperature)
3.  PAT-style Depth Temperature profiles (PDT) data
4.  Tracks (Geolocation Estimates and Likelihood Areas from light
    levels, depth and temperature)

The package inlcudes specific functions to read in, clean, transform and visualize each of these data products with 2-3 lines of code. The package and tutorial do not require deep coding skills and are therefore suitable for beginners as well as more advanced users.

For more details see below as well as the package-documentation.


``` r
## install or load package
# install.packages("RchivalTag")
library("RchivalTag")

## Package overview:
?RchivalTag 
help(package="RchivalTag") ## list of functions
```

## Details

### TaD-/TaT-histogram data

-   The package allows to read and generate standard summary data
    products (TaD-/TaT-profiles, see above) from recovered or
    transmitted time series data sets as well as to merge and visualize
    such summary data products from different tag setups/tagging
    programs. For more information on these data products, please see:
    (Wildlife Computers 2019; Bauer et al. 2017)

### Depth and temperature time series data

-   (interactive) data visualization, optionally highlighting
    temperature records and daytime differences (dawn, day, dusk,
    night).

### Daily Depth-temperature time series data

-   data visualization and examination of the thermal stratification of
    the water column (i.e. thermocline depth, gradient and
    stratification index), based on previously interpolated
    depth-temperature time series data or PAT Style depth temperature
    profiles (PDT). The paper by (Bauer, Forget, and Fromentin 2015) is
    highly recommended in this context.

### Visualizing Geolocation Estimates and Likelihood Areas

-   The newest version of
    [RchivalTag](https://github.com/rkbauer/R_Package_RchivalTag)
    includes a set of functions to illustrate geolocation estimates and
    likelihood areas from archival tags in (interactive) figures
    (e.g. see *ggplot\_geopos()*, *ggplotly\_geopos()* and
    *leaflet\_geopos()*).

## Compatability

So far, the package is mainly adapted for (pop-up) archival tagging data
from [Wildlife Computers](https://wildlifecomputers.com/) and
[LOTEK](https://www.lotek.com/) PSAT tags, but can also be applied to
data from other tag manufacturers (e.g. see *ts2histos()* in order to
calculate TaD & TaT-frequencies from time series data). Function
examples are based on the transmitted data sets of a miniPAT-tag from
the [BLUEMED-project](http://bluemed-project.com/), funded by the French
National Research Agency
([ANR](http://www.agence-nationale-recherche.fr)).


## You may also like...

- [IRATER](https://cran.r-project.org/web/packages/IRATER/index.html) - A R Interface for the Instantaneous RATEs (IRATE) Model to assess band recovery (conventional tagging) data (i.e. age-dependent or independent fishing and natural mortality rates).
- [oceanmap](https://github.com/rkbauer/R_Package_oceanmap) - A R-Package to map oceanographic data.


## References

Bauer, Robert Klaus; Fabien; Forget, and Jean-Marc Fromentin. 2015.
“Optimizing PAT data transmission - assessing the accuracy of
temperature summary data to estimate environmental conditions.”
*Fisheries Oceanography* 24 (6): 533–39.
<https://doi.org/10.1111/fog.12127>.

Bauer, Robert Klaus, Fabien Forget, Jean Marc Fromentin, and Manuela
Capello. 2020. “Surfacing and vertical behaviour of Atlantic bluefin
tuna (Thunnus thynnus) in the Mediterranean Sea: implications for aerial
surveys.” *ICES Journal of Marine Science* 77 (5): 1979–91.
<https://doi.org/10.1093/icesjms/fsaa083>.

Bauer, Robert Klaus, Jean Marc Fromentin, Hervé Demarcq, and Sylvain
Bonhommeau. 2017. “Habitat use, vertical and horizontal behaviour of
Atlantic bluefin tuna (Thunnus thynnus) in the Northwestern
Mediterranean Sea in relation to oceanographic conditions.” *Deep-Sea
Research Part II: Topical Studies in Oceanography* 141 (April 2017):
248–61. <https://doi.org/10.1016/j.dsr2.2017.04.006>.

Wildlife Computers. 2019. “Spreadsheet File Descriptions v.201903.”

## License

GPL (>= 3)

