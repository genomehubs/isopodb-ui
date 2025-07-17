```template
id: oxfordPlotByAssembly
title: Oxford plot using BUSCO genes by assembly
description: |
  Show locations of all BUSCO genes shared between a pair of assemblies
valueA_example: GCA_963676685.2
valueA_label: Assembly accession A
valueA_description: |
  Assembly GCA accession to plot on x-axis
valueB_example: GCA_017311375.1
valueB_label: Assembly accession B
valueB_description: |
  Assembly GCA accession to plot on y-axis
valueC_example: mollusca_odb10
valueC_label: BUSCO lineage
valueC_description: |
  Odb10 BUSCO lineage to use for comparison
url:
  path: /search
  query: assembly_id={valueA},{valueB} AND collate(sequence_id,busco_gene) AND feature_type={valueC}-busco-gene AND busco_status!=duplicated
  result: feature
  taxonomy: ncbi
  report: oxford
  reorient: true
  compactLegend: true
```
