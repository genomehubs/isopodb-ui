::breadcrumbs[BUSCO lists]

MolluscDB compiles lists of BUSCO IDs for each status at all ranks in the tree so it is possible to obtain a list of all duplicated BUSCOs in an assembly or all BUSCOs that are missing across all assemblies for a class.

<!-- A plot of Eukaryota BUSCO count against assembly span for phyla with at least 10 assemblies in BoaT helps to highlight differences between lineages. The minimum count threshold filters out lower quality assemblies to focus on more complete genome representations. _All plots on BoaT are interactive, click on a phylum in the legend to highlight the associated points, click on the plot to search within a bin, or click the icon to the top right of the plot to expand the plot and view more options._ -->

:::grid{container direction="row" spacing="1" inline}

<!-- ```report
report: scatter
x: assembly_span AND length(eukaryota_odb10_complete)>=130
y: length(eukaryota_odb10_complete)
rank: species
cat: phylum[11]
includeEstimates: false
yOpts: 130;260;14
ratio: 2
scatterThreshold: -1
pointSize: 15
result: taxon
taxonomy: ncbi
size: 12
``` -->

:::

MolluscDB provides templates to generate tables of busco counts including lists of BUSCO IDs with a given status.

:::grid{container direction="row" spacing="1"}

::include{pageId=templates/buscoStatusList.md size=6}

:::
