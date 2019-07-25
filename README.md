# ConektLegumes
Integrate CoNekT (Coexpression Network Toolkit) with legumes expression data into LIS. 

### CoNekT:
A platform dedicated to the visualization and analysis of plant co-expression and co-function networks.
CoNekT is an online platform that allows users to browse expression profiles, study expression specificty, co-expression networks and more across different species.

See the publication below & readme of the github repo (https://github.com/sepro/CoNekT). 

A python-flask backend which processes requests, fetches data from the database, provides search functionality and serves web pages and (ii) a front-end which includes various interactive visualizations based on charts.js, cytoscape.js (17), and phyD3.js (18). The Bootstrap CSS library is used to style all pages and is paired with jQuery.js and qtip2.js to add various dynamic elements such as tooltips and popups. Font-awesome is included for different glyphs and icons.

### Conekt Resources:
Publications:
CoNekT: an open-source framework for comparative genomic and transcriptomic network analyses. Proost et al. 2018. ( https://doi.org/10.1093/nar/gky336 )
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6030989/
LStrap: Add**

Websites:
Conekt Plant: (http://conekt.plant.tools/)   https://conekt.sbs.ntu.edu.sg/
Conekt Diurnal:   https://diurnal.sbs.ntu.edu.sg

github:
https://github.com/sepro/CoNekT  
(old) https://github.molgen.mpg.de/proost/CoNekT/  

### Goals:
Have a local instance of CoNekT for legumes at LIS and integrate it into LIS.

### What has already been done:

July 24 2019.
a. A local instance is already running in a VM (adf spun at fisher). It has glyma1, phavu1, cicar1, vigun1 datasets loaded. 
b. 'LegFed gene families' loaded
c. Trees loaded: legume.genefam.fam1.M65K.trees_ML_rooted_nameModifiedWithDOT.multi2di.subsetted.geneNamesModi.tar.gz	
    i.  legume.genefam.fam1.M65K.trees_ML_rooted trees have been converted to binary trees. Non-Binary trees are not loaded by Conekt, 
    ii. The names have been modified to replace `.` with 'DOT'. Conekt complains tree file names with `.` in them.
    iii. Only 4 species have been extracted from the entire tree structure, glyma, cicar, phavu and vigun to make a new tree file. To avoid a very very sparse tree.

Only after these steps, Conekt started working. 
By the way: Sebastian Proost, the developer made a generic tree loader for our need. Only trees generated from OrthoFinder could be used initially. (https://github.com/sepro/CoNekT/issues/3)
Generic tree import:  Currently trees can only be imported from OrthoFinder and to do so various assumptions are made about the filenames and data. This can be difficult to replicate for users that have a custom set of gene families with trees.




