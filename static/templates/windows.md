::breadcrumbs[Window-based statistics]

Window-based statistics show patterns in values of properties such as GC content along the length of chromosomes. These plots can be uesd to identify centromeric regions and can offer insight into large-scale chromosome patterning.

This example plot shows values of GC in 1Mb windows along the length of each chromosome in the _Jaera albifrons_ assembly GCA_977012755.1. Windows are plotted by their proportional midpoint along the chromosome length on the x-axis against their GC content on the y-axis. Click a sequence name in the legend to highlight the points from that series.

:::grid{container direction="row" spacing="1" inline}

```report
report: scatter
x: midpoint_proportion AND assembly_id=GCA_977012755.1 AND feature_type=win-1M
y: gc
cat: sequence_id[11]
includeEstimates: true
ratio: 2
plotRatio: 2
scatterThreshold: -1
pointSize: 15
compactLegend: true
result: feature
taxonomy: ncbi
size: 12
```

:::

<hr />

## Window plot templates

Use the templates below to generate similar plots for any indexed statistics for a given assembly accession or taxon name across fixed 1Mb windows or relative windows of 5% chromosome length.

:::grid{container direction="row" spacing="1"}

::include{pageId=templates/windowPlotByAssembly.md size=6}

::include{pageId=templates/windowPlotByTaxon.md size=6}

:::
