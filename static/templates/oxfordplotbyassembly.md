```template
id: oxfordPlotByAssembly
title: Oxford plot using BUSCO genes by assembly
description: |
  Show locations of all BUSCO genes shared between a pair of assemblies
valueA_example: GCA_965208005.1
valueA_label: Assembly accession A
valueA_description: |
  Assembly GCA accession to plot on x-axis
valueB_example: GCA_977012755.1
valueB_label: Assembly accession B
valueB_description: |
  Assembly GCA accession to plot on y-axis
valueC_example: arthropoda_odb12
valueC_label: BUSCO lineage
valueC_description: |
  Odb10 BUSCO lineage to use for comparison
url:
  path: /search
  query: assembly_id={valueA},{valueB} AND collate(sequence_id,busco_name) AND feature_type={valueC}-busco-gene AND busco_status!=duplicated
  result: feature
  taxonomy: ncbi
  report: oxford
  reorient: true
  compactLegend: true
  plotRatio: 1
```
