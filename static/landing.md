# Explore IsopoDB data

IsopoDB contains data for
:count{taxonomy=ncbi result=assembly query="tax_tree(2759)" inline description="assemblies in IsopoDB"} assemblies across
:count{taxonomy=ncbi result=taxon query="tax_tree(2759) AND tax_rank(species)" inline includeEstimates description="isopod species in IsopoDB"} species, including :count{taxonomy=ncbi result=taxon query="tax_tree(!29979) AND tax_rank(species)" inline includeEstimates description="isopod species in IsopoDB"} outgroup. The map below summarises the geographic distibutions of these species as a count of included species per country, based on [GBIF](https://www.gbif.org) occurrence data.

```report
report: map
x: country_code
rank: species
includeEstimates: true
mapThreshold: 2000
regionField: country_code
geoBounds: -180,90,180,-45
result: taxon
taxonomy: ncbi
ratio: 2.4
size: 12
```

## Search templates

We have created a set of advanced search templates to highlight some of the ways to explore the data in IsopoDB. The templates below can be used to generate an oxford plot to compare assemblies of two taxa and to plot assembly metrics in windows along each chromosome of an assembly.

Visit the [templates page](/templates) for more examples.

:::grid{container direction="row" spacing="1"}

::include{pageId=templates/oxfordPlotByTaxon.md size=6 className=unpadded}

::include{pageId=templates/windowPlotByTaxon.md size=6 className=unpadded}

::grid[&nbsp;&nbsp;more [oxford plot templates](/templates/oxford)]{size=6}
::grid[&nbsp;&nbsp;more [window-based templates](/templates/windows)]{size=6}

:::

## Ribbon plots

:hub allows exploration of synteny through ribbon plots between pairs of complete assemblies or subsets of chromosomes

```report
report: ribbon
x: assembly_id=queryA.assembly_id,queryB.assembly_id AND collate(sequence_id,name) AND feature_type=arthropoda_odb10-busco-gene AND status!=duplicated AND sequence_id=OZ239480.1,OZ242389.1
queryA: assembly--tax_name(Jaera ischiosetosa) AND refseq_category=representative genome,reference genome
queryB: assembly--tax_name(Jaera praehirsuta) AND refseq_category=representative genome,reference genome
xOpts: ;;;;Jaera ischiosetosa
compactLegend: true
reorient: true
result: feature
taxonomy: ncbi
ratio: 2
```

## Window statistic plots

```report
report: scatter
x: midpoint_proportion AND assembly_id=queryA.assembly_id AND feature_type=window-1000000 AND gc
xField: midpoint_proportion
queryA: assembly--tax_name(Asellus aquaticus)
y: gc
cat: sequence_id[8]
includeEstimates: true
plotRatio: auto
scatterThreshold: -1
pointSize: 15
result: feature
taxonomy: ncbi
ratio: 2
```

## BUSCO counts

Busco identities are recorded for each taxon, allowing plots of BUSCO counts against other assembly metrics.

```report
report: scatter
x: tax_tree(Isopoda) AND assembly_span AND arthropoda_odb10_complete
y: arthropoda_odb10_complete_proportion
rank: species
cat: genus[6]
includeEstimates: false
scatterThreshold: -1
result: taxon
taxonomy: ncbi
size: 12
ratio: 2
caption: Arthropoda BUSCO completeness against assembly span for the genera represented in IsopoDB
```
