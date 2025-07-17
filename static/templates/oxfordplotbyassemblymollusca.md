```template
id: oxfordPlotByAssemblyMollusca
title: Oxford plot using BUSCO genes by assembly showing ancestral linkage groups
description: |
  Show locations of all BUSCO genes shared between a pair of assemblies with ancestral linkage groups
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
  query: assembly_id={valueA},{valueB} AND collate(sequence_id,busco_gene) AND feature_type={valueC}-busco-gene AND busco_status!=duplicated AND ancestral_unit
  cat: "ancestral_unit[20]=moll1,moll2,moll3,moll4,moll5,moll6,moll7,moll8,moll9,moll10,moll11,moll12,moll13,moll14,moll15,moll16,moll17,moll18,moll19,moll20"
  result: feature
  taxonomy: ncbi
  report: oxford
  reorient: true
  compactLegend: true
```
