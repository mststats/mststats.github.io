+++
title = "Fine-scale Inference of Ancestry Segments without Prior Knowledge of Admixing Groups"
date = 2019-05-30T00:00:00

# Authors. Comma separated list
authors = ["Michael Salter-Townshend", "Simon R. Myers"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference proceedings
# 2 = Journal
# 3 = Work in progress
# 4 = Technical report
# 5 = Book
# 6 = Book chapter
publication_types = ["2"]

# Publication name and optional abbreviated version.
publication = "Genetics"
#publication_short = "In "

# Abstract and optional shortened version.
abstract = "We present an algorithm for inferring ancestry segments and characterizing admixture events, which involve an arbitrary number of genetically differentiated groups coming together. This allows inference of the demographic history of the species, properties of admixing groups, identification of signatures of natural selection, and may aid disease gene mapping. The algorithm employs nested hidden Markov models to obtain local ancestry estimation along the genome for each admixed individual. In a range of simulations, the accuracy of these estimates equals or exceeds leading existing methods. Moreover, and unlike these approaches, we do not require any prior knowledge of the relationship between sub-groups of donor reference haplotypes and the unseen mixing ancestral populations. Our approach infers these in terms of conditional 'copying probabilities'. In application to the Human Genome Diversity Project we corroborate many previously inferred admixture events (e.g. an ancient admixture event in the Kalash). We further identify novel events such as complex 4-way admixture in San-Khomani individuals, and show that Eastern European populations possess 1-3% ancestry from a group resembling modern-day central Asians. We also identify evidence of recent natural selection favouring sub-Saharan ancestry at the HLA region, across North African individuals. We make available an R and C++ software library, which we term MOSAIC (which stands for MOSAIC Organises Segments of Ancestry In Chromosomes)."
abstract_short = "MOSAIC Organises Segments of Ancestry In Chromosomes"

# Featured image thumbnail (optional)
image_preview = ""

# Is this a selected publication? (true/false)
selected = true 

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
projects = ["statgen"]

# Links (optional).
#url_pdf = "#"
#url_preprint = "#"
#url_code = "#"
#url_dataset = "#"
#url_project = "#"
#url_slides = "#"
#url_video = "#"
#url_poster = "#"
#url_source = "#"

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
url_custom = [{name = "DOI", url = "https://doi.org/10.1534/genetics.119.302139"},
{name="preprint",url="https://www.biorxiv.org/content/10.1101/376137v1"}, {name = "Software", url = "https://maths.ucd.ie/~mst/MOSAIC/"}]

# Does the content use math formatting?
math = true

# Does the content use source code highlighting?
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
#[header]
#image = "headers/bubbles-wide.jpg"
#caption = "My caption :smile:"

+++

