::breadcrumbs[Window-based statistics]

Window-based statistics show patterns in values of properties such as GC content along the length of chromosomes. These plots can be uesd to identify centromeric regions and can offer insight into large-scale chromosome patterning.

This example plot shows values of GC in 1Mb windows along the length of each chromosome in the _Maniola hyperantus_ assembly GCA_902806685.1. Windows are plotted by their proportional midpoint along the chromosome length on the x-axis against their GC content on the y-axis.

:::grid{container direction="row" spacing="1" inline}

```report
report: scatter
x: midpoint_proportion AND assembly_id=GCA_964016885.1 AND feature_type=window-1000000
y: gc
cat: sequence_id[50]
includeEstimates: true
ratio: 2
scatterThreshold: -1
pointSize: 15
  compactLegend: true
result: feature
taxonomy: ncbi
size: 12
```

:::

BoaT provides templates to generate similar plots for all indexed statistics for a given assembly accession or taxon name at fixed window sizes of 1Mb and 100Kb or relative window sizes of 0.1 and 0.01 proportions of chromosome length.

:::grid{container direction="row" spacing="1"}

::include{pageId=templates/windowPlotByAssembly.md size=6}

::include{pageId=templates/windowPlotByTaxon.md size=6}

:::
