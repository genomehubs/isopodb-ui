```template
id: windowPlotByAssembly
title: Window statistic plot by assembly
description: |
  Show values of a statistic for windows along each chromosome in an assembly
valueA_example: GCA_964016885.1
valueA_label: Assembly accession
valueA_description: |
  Assembly GCA accession
valueB_example: gc
valueB_label: Statistic
valueB_description: |
  Window-based statistic to plot along chromosomes. Options include: gc, masked, busco_count
valueC_example: 1000000
valueC_label: window-size
valueC_description: |
  Window size. Options include: 1000000, 100000, 0.1 & 0.01
url:
  path: /search
  query: midpoint_proportion AND assembly_id={valueA} AND feature_type=window-{valueC} AND {valueB}
  report: scatter
  y: "{valueB}"
  cat: sequence_id[50]
  includeEstimates: true
  scatterThreshold: -1
  result: feature
  taxonomy: ncbi
```
