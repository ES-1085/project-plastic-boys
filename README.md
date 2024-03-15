Leslie Hart’s Sarasota Bay Microplastics Data Visualization
================
by Mabon Young, Gordon Maguire, John Calzini

## Summary

The data we used from our project was pulled from a 2023 study performed
by Leslie Hart investigating microplastic presence in fish in Sarasota
Bay. A microplastic is defined as, “extremely small pieces of plastic,
manufactured as such (in the form of nurdles or microbeads) or resulting
from the disposal and breakdown of plastic products and waste.” (Oxford
English Dictionary). Our data was looking at the presence of these
plastics within fishes. We received our dataset through the database
Dryad, a platform that provides free information and accessible data for
anyone interested. It is a helpful tool for up-and-coming researchers
looking to get their work out. Within the data, 29 fish across four
species were looked at; Hardhead catfish, Ariopsis felis (n=2), Pigfish,
Orthopristis chrysoptera (n=12), Pinfish, Lagodon rhomboides (n=10), and
Gulf toadfish, Opsanus beta (n=5). Our data analysis mainly consisted of
formulating different types of visualizations, such as bar and column
graphs, scatter plots, ridgeline plots, and spatial plots using the
Leaflet package.

Our central questions when exploring the data were as follows: One, are
there significant differences in the microplastic concentrations between
the two sampling stations in the data, and two, what are the notable
properties of the most widespread microplastics? The two research
stations were located in Longboat Key and Sarasota, with the Longboat
Key samples having much higher microplastic counts. The data collected
show that most of the microplastics found were single fibers, and the
most common colors were transparent, blue, black, and yellowed. Most of
the non-single fibers were transparent, except for TWP particles, which
were all black as expected. The majority of the microplastics were found
within the GI tract of the fish, but the amount found in muscle tissue
stayed relatively consistent between Sarasota and Longboat Key. In
addition to this, the samples taken from the fish in Sarasota generally
had lower microplastic counts, despite the samples being heavier than
the ones from Longboat Key, implying that not only do the fish near
Longboat Key contain more microplastics, the plastics are also much more
densely concentrated in them. We also found that all of the samples that
contained more than 40 microplastic particles were taken from the GI
tracts of the Longboat Key fish. We additionally created a ridgeline
density plot showing the quantity distribution density of plastics
within each fish. Most of the fish had similar density distributions
with few outliers, despite the skewed distribution of species
collection. Our main findings as a result showed that: 1. The most
common particle type was a single fiber. 2. The most common particle
color was transparent. 3. The fish from Longboat Key had higher
microplastic concentrations. 4. The GI tracts contained more
microplastics than the muscle samples.

The data had a few limitations, but there were two main ones that
impacted our analysis. The low number of sampling sites makes drawing
any broad spatial conclusions challenging, as we can only effectively
compare two locations. There was also a relatively small number of fish
sampled in this study, and the amount of samples taken from each species
was inconsistent, which also makes it difficult to establish any
wide-scale patterns in microplastic presence in different species. That
being said, the data do still make it clear that there is a strong
microplastic presence in Sarasota Bay, especially near Longboat Key. The
vast majority of particles are also difficult to trace the origins of,
as a single transparent or black fiber could have come from any number
of things.

data: Contains dataset and codebook leaflet_stations: Leaflet map of
sampling stations plastics_analysis: Main R analysis file presentation:
Contains images used in presentation slides proposal: Contains project
proposal writeup

## Presentation

Our presentation can be found
[here](https://docs.google.com/presentation/d/1VtSjx993S1fUaJIVKVAaUgEzgAhsIhMoO2r_tcoFpJQ/edit?usp=sharing).

## Data

Hart, Leslie (2023). Suspected microplastic counts and characteristics
in fish muscle and gastrointestinal tissue \[Dataset\]. Dryad.
<https://doi.org/10.5061/dryad.fn2z34v1d>

## References

Hart, Leslie (2023). Suspected microplastic counts and characteristics
in fish muscle and gastrointestinal tissue \[Dataset\]. Dryad.
<https://doi.org/10.5061/dryad.fn2z34v1d> (slide 3)

Who we are. Dryad. (n.d.). <https://datadryad.org/stash/about> (slide 3)

<https://mote.org/news/article/record-year-for-dolphin-calves-in-sarasota-bay-and-vicinity>
(slide 11 image)

<https://ncfishes.com/marine-fishes-of-north-carolina/orthopristis-chrysoptera/>
(slide 9 image)

<https://www.scientificamerican.com/article/from-fish-to-humans-a-microplastic-invasion-may-be-taking-a-toll/>
(slide 2 image)
