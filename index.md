---
title       : "Using Stable Isotopes as Tracers"
subtitle    : "Use of stable isotopes in Marine Ecology, 11-15 Jan 2016, EIDEMAR."
author      : "Edward P. Morris (UCA-CEIMAR)"
job         : "University of Cadiz"
date        : "2016-01-12"
bibliography: "bibliography.bib"
#logo       : UCA-ceimar-logo-480-198-transparent.png # not used
#biglogo    : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax, quiz, bootstrap, interactive]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
font-import : 'https://fonts.googleapis.com/css?family=Fira+Sans'
font-family : 'Fira Sans'

--- .lightbg
## Unit structure

### Content
+ duration: 3 h teaching session; 1.5 h theory, 1.5 h practice on PC
+ audience: Msc., PhD students and post-docs

### Aims

+ introduce stable isotope tracer techniques
+ provide important terminology specific to tracers
+ give sources of important literature and help
+ give tools for calculations
+ ensure participants can design and analyse stable isotope tracer experiments

--- .lightbg
## Unit structure
### Assessment

+ participation in mini excercises during teaching
+ complete excercises on PC
+ grading of students 1 page 'mock' isotope tracer experiment (optional?)

### Requirements

+ familiarity with general stable isotope terminology (see [lectures](https://av02-ext.uca.es/moodle/mod/resource/view.php?id=19911))
+ access to PC with [R](https://cran.r-project.org) and [Rstudio](https://www.rstudio.com/) (try and get Shiny server up and then just a web browser) 
+ a basic idea for a tracer experiment (optional)

--- &twocol .lightbg
## Outline

*** {name: left, span: 6}

When natural abundance is not enough...
  + tracing nutrient cycling

Stable isotope tracer specific terminology

Where can I find some help?
  + Important literature
  + Forums, groups and software

*** {name: right, span: 6}

How do I calculate that?
  + Basic calculations
  + Using specific software packages

Design a stable isotope tracer experiment
  + Setting up the basic calculations
  + Calculating costs
  + Analysing results

--- .segue .darkbg
## When 'natural abundance' is not enough...

--- .lightbg &twocol
## Stable isotope tracers

*** {name: left, span: 8}

+ Material with a very different isotopic composition.
+ Allows tracing of material through systems.
+ Non-toxic and biodegradable.
+ No special handling or specific permits needed.

*** {name: right, span: 4}

<pw style="text-align:center;"><img alt ="single_C_stable_isotope" src=assets/img/single_C_stable_isotope.png width=300px>
<br>^13 C stable isotope; 6 protons (light blue) and 7 nuetrons (yellow), difference in atomic weight, but chemically equal. </pw>

--- .lightbg
## Stable isotope tracers

Useful for examining the details of flows and processes, for example:

+ Carbon uptake and fractionation by different photosynthetic organisms (see [lecture](https://av02-ext.uca.es/moodle/mod/resource/view.php?id=20605)).
+ Nitrogen and carbon assimilation efficiency through food webs (see [lecture](https://av02-ext.uca.es/moodle/mod/resource/view.php?id=19910)).
+ Nitrification and denitrification in the water column and sediments (see [article](https://av02-ext.uca.es/moodle/mod/resource/view.php?id=19994)).
+ Whole ecosystem nutrient cycling; pelagic, benthic, wetlands, estuaries, rivers, lakes, aquaculture ponds, chemostats.

--- .lightbg
## Tracing nutrient cycling - Whole ecosystem approaches

include one or two examples of whole ecosystem tracer experiments and the highlight unique findings. 

--- .lightbg
## Tracing nutrient cycling - Cadiz Bay

~90% of Cadiz inner bay is covered in benthic plants (angiosperms and algae).

<pw style="text-align:center;"><img alt ="Cadiz_Inner_Bay_Macrofitos" src=assets/img/Cadiz_Inner_Bay_Macrofitos.png width=650px>
<br>Morris et al., FUNDIV, Regional government of Andalucia project of excellence P07-RNM- 2516.</pw>

--- .lightbg &twocol
## Tracing nutrient cycling - Cadiz Bay

*** {name: left, span: 6}
Strong human influence in the region; plenty of N sources.

+ Urban and aquaculture effluents are potential 'natural' tracers.

*** {name: right, span: 6}
<pw style="text-align:center;"><img alt ="pressures_cadiz_bay" src=assets/img/pressures_cadiz_bay.png width=400px>
<br>Morris et al., FUNDIV, Regional government of Andalucia project of excellence P07-RNM- 2516.</pw>

--- .lightbg 
## Tracing nutrient cycling - Cadiz Bay

Collecting samples of macrophyte biomass and suspended solids near effluent discharges allows tracing of long-term nutrient loading.

<pw style="text-align:center";><img alt ="fig3_morris_et_al_meps_2009" src=assets/img/fig3_morris_et_al_meps_2009.png width=450px>
<img alt ="fig5A_morris_et_al_meps_2009" src=assets/img/fig5A_morris_et_al_meps_2009.png width=450px>
<br>Morris EP., Peralta G., Benavente J., Freitas R., Rodrigues AM., Quintino V., Alvarez O., Valcárcel-Pérez N., Vergara JJ., Hernández I., Pérez-Lloréns JL. 2009. Caulerpa prolifera stable isotope ratios reveal anthropogenic nutrients within a tidal lagoon. Marine Ecology Progress Series 390:117–128, doi: [10.3354/meps08184](https://dx.doi.org/10.3354/meps08184).
</pw>


--- .lightbg &twocol
## Tracing nutrient cycling - Cadiz Bay

*** {name: left, span: 5}

Benthic macrophytes give an indication of N loading

+ loading is highest near discharges, in the deepest and highest water velocity regions.

*** {name: right, span: 7}
<pw style="text-align:center";><img alt ="krigged_d15N_cadiz_bay_2006" src=assets/img/krigged_d15N_cadiz_bay_2006.png width=480px>
<br>Morris EP., Peralta G., Benavente J., Freitas R., Rodrigues AM., Quintino V., Alvarez O., Valcárcel-Pérez N., Vergara JJ., Hernández I., Pérez-Lloréns JL. 2009. Caulerpa prolifera stable isotope ratios reveal anthropogenic nutrients within a tidal lagoon. Marine Ecology Progress Series 390:117–128, doi: [10.3354/meps08184](https://dx.doi.org/10.3354/meps08184).
</pw>

--- .lightbg
## Tracing nutrient cycling - Natural tracers

Interpretting sources is complicated by overlapping, variable stable isotope values and the influence of biogeochemical processes.

+ Using multiple isotopes may help.
+ Test hypothesis with independant data sources.
+ Test hypothesis with further experiments.
    + Increase the difference in isotopic composition between source and sink.

--- .lightbg
## Where to find material with different isotopic compositions?

+ 'Man-made' nitrogen from fertilizer production; &delta;^15 N  ~ 0.
+ Biologically transformed N from effluent; &delta;^15 N  > 5.
+ Plant carbon; photosynthetic fractionation gives &delta;^13 C values between ~ -7 and -35.
+ Laboratory grade enriched stable isotopes; range of compounds and enrichment available.

--- .segue bg:url(assets/img/questions-UCA-ceimar-background-dark-1100px700px.png);
## Questions?

--- .segue .darkbg
## Adding stable isotope tracers

--- .lightbg
## Golden rules of isotope addition experiments

+ Aim for a *significantly different isotopic composition of the source, without a sig. different concentration (within 5 %)*.
    + ^15 N relatively cheap.
    + ^13 C relatively expensive.

+ Take isotopic composition measurements of the medium (i.e, water, biomass, DIN, DIC), *before* and *after* tracer addition.
    + Measurements are ideal (take plenty of samples), however inert tracers can also be used to give a good indication.

+ Take isotopic composition measurements of the subject (i.e, water, biomass, DIN, DIC), *before* and *after* tracer addition.    
    + Take plenty of samples (ensure good representation of 'natural abundance').
    + Consider non-linear sampling in time and space.

--- .lightbg
## Semi-closed systems

Incubation chambers, flume-tank, mesocosms, pilot plants, lakes, ponds, inter-tidal sediments.

+ Add tracer to *initial medium* at start of experiment.
+ Measure or calculate isotopic composition of the source.
    + Beware of changing concentration and isotopic composition of the source in time.
    + Using an inert tracer (Uranine, Bromide, ect.) can help define the initial concentration of tracer in systems with unkown or variable volume.

--- .lightbg
## Semi-open systems

Bays, rivers, estuaries, lakes, ponds, sub-tidal sediments, chemostat, pilot plants.

+ Add tracer to *inflow of medium* throughout experiment.
    + Ensure tracer addition matches inflow.
+ Measure or calculate isotopic composition of the source.
    + Use an inert tracer to aid calculations.
    + Beware of changing concentration and isotopic composition of the source in space and time.

--- .lightbg
## Collecting samples

+ **Completely seperate all handling and processing of labelled and non-labelled samples!**
+ Collect and process samples in the same way as for measuring elemental composition.
    + Take adequate steps to reduce cross-contamination; wash off excess medium, flush with 'clean' water, handle with gloves/tweezers.
    + Biomass and suspended matter samples should be weighed and dried to constant weight (freeze dried or 48h @60ºC).
       + Avoid high temperatures to avoid volatisation of C and N compounds.
       + Store frozen or dried (should have minor changes in isotopic composition).
    + Suspended material must be collected on inert filters; pre-combusted (4h @550ºC) or specially designed.    
    + Water samples should be processed as soon as possible; add compound to stop biological activity.
       + See [Sigman et al. 1997](www.sciencedirect.com/science/article/pii/S0304420397000091) and [Lehmann et al. 2001](http://pubs.acs.org/doi/abs/10.1021/ac010212u) for details of DIN extraction.

--- .lightbg
## Preparing samples for analysis

+ Consider if interfering compounds can/should be seperated/removed.
    + Epiphytes on benthic macrophytes.
    + Calcium carbonate in suspended matter and sediments affects 13C measurments.
    + Mechanical and acid removal are options, although note there is a trade off as acidification may affect 15N values.

+ Ensure subject material is well mixed.
    + Grind organic material to a fine powder.
    + Assume material on filters represents a random sample.
    
+ For material trapped on filters consider checking if filters are really inert.

--- .lightbg
## Preparing samples for analysis

+ Optionally send samples for further processing to a certified laboratory (at a cost) or prepare them yourself and send.
    + Weigh (accuracy 0.001 mg) specified amount of sample and securely close in a specially designed 'tin combustion cup'.
    + Talk to the lab who will do the analysis, *before preparing the sample*.
    + Amount of material depends on the elemental content of the material.
        + For example see [Colorado Plateau Stable Isotope Laboratory](http://www.isotope.nau.edu/submit.html)); ^15 N analysis of fresh plants (3% N content) 3.000 to 4.000 mg. 

--- .lightbg
## Preparing samples for analysis

+ **Not all labs will take labelled material!** Check possibilities and prices before starting experiment; expect to pay a little more for labelled material as it requires a different setup and excludes natural abundance measurements.

+ Finally, **shop around**; stable isotope samples travel well and are cheap to ship, hence look around for a lab that suits your price and turn-around time.
    + [CPSIL Pricing](http://www.isotope.nau.edu/pricing.html)
    + [Tarifas SAI-UTIA](https://www.sai.udc.es/es/unidades/UTIA)

--- .segue bg:url(assets/img/questions-UCA-ceimar-background-dark-1100px700px.png);
## Questions?

--- .lightbg &multitext
## Questions?
The price of ^13 C and ^15 N tracers are both relatively similar per gram.

1. What are the natural concentrations of dissolved inorganic carbon and nitrogen (DIC and DIN) in water?
2. What is the approximate maximum amount of DIC and DIN tracer that can be added to the system?
3. Can  you explain why the costs of using each are so different?

*** .explanation
1. <span class='answer'>
The concentration of dissolved inorganic carbon in water (DIC, 1000 - 4000 mmol/m3) is about 2 orders of magnitude higher than dissolved inorganic nitrogen (DIN, 1 - 100 mmol/m3).
</span>

2. <span class='answer'> Applying the 5% rule, we can estimate that the maximum tracer to be used is 20 x 0.05 = 1 mmol/m3 or ~ 14 mg/m3 of DIN and 2000 * 0.05 = 100 mmol/m3 or 1200 mg/m3 of DIC.
</span>

3. <span class='answer'> Allot more DIC tracer is required to 'increase the difference in isotopic composition between source and sink'.
</span>

*** .hint
Use the '5% rule' and the range of natural concentrations in aquatic systems.

--- .lightbg
## Semi-closed system - N uptake of benthic macrophytes in a flume-tank

--- .lightbg
## Semi-open system - N uptake of benthic macrophytes insitu



--- .segue .darkbg
## Tracer specific terminology

--- .lightbg
## Stable isotope-amount fraction or atom fraction (*x*)

Previously called 'AP', 'Atom %'.

> Amount of a specified atom (isotope) (*n*) of a chemical element (E) divided by the total amount of atoms of the element within the mixture (P).

> $$x ( ^{i} \mathrm{E} ) _{ \mathrm{P} } = n ( ^{i} \mathrm{E} ) _{\mathrm{P}} / Σ n ( ^{k} \mathrm{E}) _{ \mathrm{P}}$$

For example, the ^15 N fraction, *x*(^15 N), of dissolved inorganic nitrogen was *x*(^15 N) ~DIN~ = 98 %.

For a full overview see @coplen_guidelines_2011.

--- .lightbg
## Excess atom fraction, *x*^E (^*i* E) ~P/reference

Also called excess (stable) isotope-amount fraction, previously 'atom percent excess', 'atom % excess' or 'APE'.

> Difference between the *mole fraction* of an isotope ^*i* E of element E in substance P and that of a reference. The superscript E signifies an excess quantity.

> $$x ^{\mathrm{E}} ( ^{i} \mathrm{E} _{\mathrm{P/reference}} = x ( ^{i} \mathrm{E} ) _{ \mathrm{P} } - x ( ^{i} \mathrm{E} ) _{ \mathrm{reference} }$$

For example, the excess atom fraction of plant above-ground biomass (AGB) compared to the reference atom fraction of dissolved inorganic nitrogen (*x*(^15 N) ~DIN),  *x* ^E (^15 N) ~AGB/DIN = 10 %.

For a full overview see @coplen_guidelines_2011.

--- .segue .darkbg
## Where can I find some help?

--- .lightbg
## Useful literature

### Books

Stable Isotope Ecology (2006). B. Fry. Springer, New York. ISBN: 0387305130

Stable Isotope Geochemistry (2009). Jochen Hoefs. Springer, New York. ISBN: 978-3-540-70708-0 (Online)

Theory and application of tracers (1993). D. S. Schimel. Academic press Inc., London. ISBN: 0126246505

Stable isotopes in ecology and environmental science (1994). K. Lajtha & R. H. Michener. Blackwell scientific publications, Oxford. ISBN: 0632031549

--- .lightbg
## Forums and web resources

--- .lightbg
## Software tools

--- .segue .darkbg
## How do I calculate that?

--- .lightbg
## Basic calculations

--- .lightbg
## Using specific software packages

--- .segue .darkbg
## Design a stable isotope tracer experiment

--- .lightbg
## Setting up the basic calculations

--- .lightbg
## Calculating costs

--- .lightbg
## Analysing results



