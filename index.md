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
## Content

+ duration: 3 h teaching session; 1.5 h theory, 1.5 h practice on PC
+ audience: Msc., PhD students and post-docs

--- .lightbg
## Aims

+ introduce stable isotope tracer techniques
+ provide important terminology specific to tracers
+ give sources of important literature and help
+ give tools for calculations
+ ensure participants can design and analyse stable isotope tracer experiments

--- .lightbg
## Assessment

+ participation in mini excercises during teaching
+ complete excercises on PC
+ grading of students 1 page 'mock' isotope tracer experiment (optional?)

--- .lightbg
## Requirements

+ familiarity with general stable isotope terminology (see [lectures]())
+ access to PC with [R](https://cran.r-project.org) and [Rstudio](https://www.rstudio.com/) (try and get Shiny server up and then just a web browser) 
+ a basic idea for a tracer experiment (optional)

--- &twocol .lightbg
## Outline

*** {name: left, span: 6}

+ When natural abundance is not enough...
    + tracing nutrient cycling
        + biogeochemistry
        + foodwebs
+ Stable isotope tracer specific terminology
+ Where can I find some help?
    + Important literature
    + Forums, groups and software

*** {name: right, span: 6}

+ How do I calculate that?
    + Basic calculations
    + Using specific software packages
+ My 'first' stable isotope tracer experimental design
    + Setting up the basic calculations
    + Calculating costs
    + Analysing results

--- .segue .darkbg
## When 'natural abundance' is not enough...

--- .lightbg
## Stable isotope tracers

+ Material with a very different isotopic composition.
+ Allows tracing of material through systems.
+ Non-toxic and biodegradable.
+ No special handling or specific permits needed.

--- .lightbg
## Stable isotope tracers

Useful for examining the details of flows and processes, for example:

+ ^13 C uptake and fractionation by different photosynthetic organisms.
+ Nitrogen and carbon assimilation efficiency through food webs.
+ Nitrification and denitrification in the water column and sediments.
+ Whole ecosystem nutrient cycling; pelagic, benthic, wetlands, estuaries, rivers, lakes, aquaculture ponds, chemostats.

--- .lightbg
## Tracing nutrient cycling - Whole ecosystem approaches

include one or two examples of whole ecosystem tracer experiments and the highlight unique findings. 

--- .lightbg
## Tracing nutrient cycling - Cadiz Bay

~90% of Cadiz inner bay is covered in benthic plants (angiosperms and algae):

+ What role do they play in nutrient cycling?

![Cadiz bay benthic plant coverage]()

--- .lightbg
## Tracing nutrient cycling - Cadiz Bay

Strong human influence in the region; plenty of N sources.

+ Urban and aquaculture effluents are potential 'natural' tracers.

![Cadiz bay anthropogenic pressures]()

--- .lightbg
## Tracing nutrient cycling - Cadiz Bay

Collecting samples of macrophyte biomass and suspended solids near effluent discharges allows tracing of long-term nutrient loading.

![Morris_et_al_MEPS_2009_fig_]()

--- .lightbg
## Tracing nutrient cycling - Cadiz Bay

![Morris_et_al_MEPS_2009_fig_]()

--- .lightbg
## Tracing nutrient cycling - Cadiz Bay

![Morris_et_al_MEPS_2009_fig_]()

--- .lightbg
## Tracing nutrient cycling - Natural tracers

Interpretting sources is complicated by overlapping, variable stable isotope values and the influence of biogeochemical processes.

+ Using multiple isotopes may help.
+ Test hypothesis with independant data sources.
+ Test hypothesis with further experiments.
    + Increase the difference in isotopic composition between source and sink.

--- .lightbg
## Where to find material with a different isotopic compositions?

+ 'Man-made' nitrogen from fertilizer production; &delta;^15 N  ~ 0.
+ Biologically transformed N from effluent; &delta;^15 N  > 5.
+ Plant carbon; photosynthetic fractionation gives &delta;^13 C values between ~ -7 and -35.
+ Laboratory grade enriched stable isotopes; range of compounds and enrichment available.

--- .lightbg
## Adding stable isotope tracers

+ Aim for a significantly different isotopic composition of the source, without a sig. different concentration (within 5 %).
+ ^15 N relatively cheap.
+ ^13 C relatively expensive.

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
## Adding stable isotope tracers

+ Take isotopic composition measurements of the medium (i.e, water, biomass, DIN, DIC), *before* and *after* tracer addition.
    + measurements are ideal (take plenty of samples), however inert tracers can also be used to give a good indication.

+ Take isotopic composition measurements of the subject (i.e, water, biomass, DIN, DIC), *before* and *after* tracer addition.    
    + take plenty of samples (ensure good representation of 'natural abundance')
    + consider non-linear sampling in time and space.

--- .lightbg
## Adding stable isotope tracers

Semi-closed systems; incubation chambers, flume-tank, mesocosms, pilot plants, lakes, ponds, inter-tidal sediments.

+ Add tracer to *initial medium* at start of experiment.
+ Measure or calculate isotopic composition of the source.
    + Beware of changing concentration and isotopic composition of the source in time. 

--- .lightbg
## Adding stable isotope tracers

Semi-open systems; bays, rivers, estuaries, lakes, ponds, sub-tidal sediments, chemostat, pilot plants.

+ Add tracer to *inflow of medium* throughout experiment.
    + Ensure tracer addition matches inflow.
+ Measure or calculate isotopic composition of the source.
    + Use inert tracer to aid calculations.
    + Beware of changing concentration and isotopic composition of the source in space and time.

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


