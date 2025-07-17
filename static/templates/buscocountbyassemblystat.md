```template
id: buscoCountByAssemblyStat
title: Scatter plot of BUSCO count by assembly statistic
description: |
  Show counts of BUSCO genes relative to values of an assembly statistic
valueA_example: assembly_span
valueA_label: Assembly statistic
valueA_description: |
  Assembly statistic to plot on the x-axis
valueB_example: eukaryota
valueB_label: BUSCO lineage
valueB_description: |
  BUSCO lineage to plot counts for on the y-axis
valueC_example: phylum[8]
valueC_label: Category
valueC_description: |
  Category to use to colour points on the plot. Optional value in square brackets is number of categories to show
url:
  path: /search
  query: "tax_tree({valueB}) AND {valueA} AND {valueB}_odb10_complete"
  y: "length({valueB}_odb10_complete)"
  rank: species
  cat: "{valueC}"
  report: scatter
  includeEstimates: false
  scatterThreshold: -1
  pointSize: 15
  result: taxon
  ratio: 1.5
  taxonomy: ncbi
```
