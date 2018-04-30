# geopython-hekla

This repository contains the slides for my presentation at the [GeoPython
2018](http://2018.geopython.net) conference.  It uses
[reveal.js](https://github.com/hakimel/reveal.js) to render the slides in the
browser.


## REPRODUCIBLE GEOSCIENCE: VOLCANIC ERUPTION MASS CALCULATIONS USING PYTHON,
GRASS7 AND PANDAS

Dr John A Stevenson, British Geological Survey

> 3 cm thick here, 0.5 cm there, 3 metres thick over there! Volcanic eruptions
> cover the landscape in pumice and ash. But how much was erupted? Python is
> the glue that joins open source GIS (GRASS7) and data science (Pandas) tools
> used to create a reproducible method to calculate erupted mass.

### Abstract

Performing GIS analysis via scripts is the ultimate way to "show your working"
as each step is documented in code. Even better, the analysis can be repeated
with a single command and can be updated as new data become available. The
PyGRASS interface provides a simple way to run spatial analysis in GRASS and to
integrate it with pre- and post-processing steps within the same script.

We show how Python and GRASS were used to calculate the mass of material
erupted by two large (>10 cubic kilometres volume), pre-historic eruptions of
Iceland's Hekla volcano. Firstly, Python is used to read field and lab data
from CSV files into an SQLite database. Pyproj re-projects GPS locations to the
local coordinate reference system. Within GRASS, Voronoi tessellation is used
divide the area where the deposits are found into regions that each contain one
sample data point. Maps can be exported to visualise changes in thickness.
After calculating the areas of the Voronoi cells, the Python-based Pandas
library can connect to the same database and multiply the deposit thickness and
density by the calculated area to get the mass in each. These are summed to
give the total erupted mass.

Unlike traditional methods, this is an entirely objective and data-driven way
to calculate the erupted mass. The advantages and disadvantages of this, and
the best ways to incorporate manual steps where required will be discussed.
