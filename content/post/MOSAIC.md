+++
title = "New Paper out in GENETICS"

date = 2019-06-25T00:00:00
lastmod = 2019-06-25T00:00:00
draft = false
tags = ["publications", "genetics"]
summary = "A paper I wrote with [Prof. Simon Myers](http://www.stats.ox.ac.uk/~myers) on admixture was chosen by the [GENETICS](https://www.genetics.org/) Editors as one of the July 2019 Highlights."
[header]
#image = "headers/getting-started.png"
#caption = "Image credit: [**Academic**](https://github.com/gcushen/hugo-academic/)"

+++


**Admixture is a pervasive and important element of human demographic history.**

## Summary

Our new highlighted paper in the journal [GENETICS](https://www.genetics.org/) deals with modelling complex human population histories.
We're particularly interested in something called "admixture", which is when two or more previously separated populations 
come together, typically due to migration or the removal of some other barrier ^[e.g. cultural or religious] to
procreation between the groups. By examining modern genetic samples, we report evidence for such admixture globally and persistently, reflecting the importance of migration 
in shaping modern human populations. 

Our method, which we term **MOSAIC**, ^[MOSAIC stands for "MOSAIC Organises Segments of Ancestry In Chromosomes"]
allows for the decryption of how such admixture events unfolded; i.e. which groups mixed, in what ratios, and when did this happen? It relies only
on modern genetic samples to achieve this and crucially does not require assumptions about how these modern samples might relate to the unseen ancient (ad)mixing groups ^[or are descended either directly or indirectly from]. Previous methods exclusively rely on known ^[or assumed known...] direct correspondence between modern populations and the mixing ancestor groups, 
whereas **MOSAIC** makes inference on potentially complex patterns of relatedness, based only on the data. This is achieved by fitting a flexible model ^[specifically
a two-layer (a.k.a. coupled a.k.a. nested) Hidden Markov Model] of "haplotype copying"; this is essentially a method that ranks how closely related each
stretch of chromosome in each individual is to the chromosome stretches in individuals from other populations 
^[Such models are often referred to as Li and Stephens models after [Li and Stephens 2003](https://www.genetics.org/content/165/4/2213.long).
Essentially, this forms the lower layer of our two-layer Hidden Markov Model.]. 
Not only does **MOSAIC** infer how and when admixture arose
within a population, but it attributes "local ancestry" to every part of every chromosome for each individual in the dataset. 

We analyse 95 modern populations using this new approach and identify previously unknown admixture events. 
Highlight findings include the discovery of a complex 4-way admixture in San-Khomani individuals
from South Africa. We also show that Eastern European populations possess between 1% and 3% ancestry from a group resembling modern-day central Asians. 
In addition the method identifies evidence of recent natural selection favouring sub-Saharan ancestry at the "HLA" region, ^[The **H**uman **L**eukocyte **A**ntigen is a gene complex that includes many proteins responsible for regulation of the immune system and are therefore a region of the genome upon which natural selection is believed to act] 
across North African individuals. 

-  **Read the new [paper here](https://doi.org/10.1534/genetics.119.302139) for full details.**

-  **See [The MOSAIC Project Website](https://maths.ucd.ie/~mst/MOSAIC/) for an interactive results browser, manual, and source code.**

## Bullet Point Summary
- By examining modern genetic samples from around the world, we can demonstrate that observed "populations" are really a mixture of
older populations. 
- Such mixing events occur globally and throughout history and can be complex, and sudden or ongoing. 
- We have developed a new tool that can probe such events back in time using the patterns left on modern DNA samples by such events. 
- The key contribution is that we do not require specification of surrogate "reference populations" for the mixing ancestral groups. 
- More accurate characterisation of admixture than previously possible is demonstrated in a variety of situations.
- We identify previously unknown admixture events including a complex 4-way admixture in San-Khomani individuals from Southern Africa. 
- We show that Eastern European populations possess 1% to 3% ancestry from a group resembling modern-day central Asians. 
- We identify evidence of recent natural selection favouring sub-Saharan ancestry at the HLA region, across North African individuals. 
- Results for all 95 analysed populations are viewable through a browser at [https://maths.ucd.ie/~mst/MOSAIC/HGDP_browser)](https://maths.ucd.ie/~mst/MOSAIC/HGDP_browser).


## Additional Detail
All populations are admixed when you look at the right time depth and compare to the right mixing sources. In other words, admixture
is pervasive and 

> there's no such thing as a "pure" European - or anyone else
([Gibbons, 2016](https://www.sciencemag.org/news/2017/05/theres-no-such-thing-pure-european-or-anyone-else)).^[Nor has there ever been; ancient DNA shows that much older populations were no exception ([Jeong et al, 2019](https://www.nature.com/articles/s41559-019-0878-2)).]


When a population is isolated ^[even partially isolated] from other populations random genetic differences between them accrue; the longer the separation, the more "drifted" these populations become from each other. Eventually, given enough such differences, we can statistically tell one group from another 
and assign (albeit noisily) an individual to a population based on which mutations they might carry. Such "population structure"
has been shown to [mirror geography](https://doi.org/10.1038/nature07331) for example. 

It's been shown before that admixture (the coming together of previously separated populations) is a feature of many 
human populations ([Hellenthal et al, 2014](http://dx.doi.org/10.1126/science.1243518)). Through sophisticated statistical procedures, heavily informed by known
biology, ^[The process of chromosomal recombination means that individuals inherit shorter segments from each ancestral 
source with each passing generation since the admixture event.]
the demographic history can be inferred by careful examination of the telltale patterns of shared 
genetic variation within and between such populations. 

This is possible because 
the distribution of these ancestral segments (were they known) would enable us to estimate when the event(s) took
place and what proportion of each source was involved. Although we don't get to directly observe the ancestry of these segments, 
we can accurately infer them when we have "reference" populations to compare to ^[something called ["chromosome painting"](http://paintmychromosomes.com/)].
For such a direct approach to work, these reference populations need to be good surrogates for the (ad)mixing groups. However, since we use modern populations, they'll typically
be drifted somewhat themselves ^[with respect to the mixing groups] and perhaps even admixed with other populations, hence not direct surrogates. This has formed a central challenge in fitting 
admixture models and motivates the need for our new approach. 

Our new tool, **MOSAIC**, is novel in that we replace knowledge of these direct surrogates with a more flexible model. The model
not only allows for more complex relationships between observed surrogates and the unseen mixing ancestral groups, but it doesn't require prior
knowledge of these relationships. Rather, we let the data do the talking and make estimates of "copying probabilities" that can adapt to the 
observed complexity as required ^[MOSAIC also finds estimates of the level of drift between the observed modern populations and the mixing ancestral groups].
This also allows us to use more reference populations; whereas an admixed population would be unsuitable for use by a tool that assumes 
reference populations are direct surrogates for mixing groups, ^[as they will be heavily confounded by this] 
MOSAIC not only allows this but it can boost the power of the method. ^[compared to leaving such a reference population out of the analysis. In fact MOSAIC can return accurate local ancestry estimates
and thus accurate admixture summaries when one or more ancestries has no good direct surrogates among the reference populations. 
For example, when it is only observed in admixed form, which is particularly common when looking at older admixture events.]
MOSAIC is shown to yield more accurate results than previously possible and can be applied to any sexually reproducing species. 

