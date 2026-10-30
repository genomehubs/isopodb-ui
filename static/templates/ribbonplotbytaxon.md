```template
id: ribbonPlotByTaxon
title: Ribbon plot using BUSCO genes by taxon
description: |
  Show locations of all BUSCO genes shared between a pair of species
valueA_example: Jaera praehirsuta
valueA_label: Taxon A
valueA_description: |
  Taxon name or ID to plot on x-axis
valueB_example: Jaera albifrons
valueB_label: Taxon B
valueB_description: |
  Taxon name or ID to plot on y-axis
valueC_example: arthropoda_odb12
valueC_label: BUSCO lineage
valueC_description: |
  Odb10 BUSCO lineage to use for comparison
url:
  path: /search
  query: assembly_id=queryA.assembly_id,queryB.assembly_id AND collate(sequence_id,busco_name) AND feature_type={valueC}-busco-gene AND busco_status!=duplicated
  queryA: assembly--tax_name({valueA})
  queryB: assembly--tax_name({valueB})
  xOpts: ";;;;{valueA}"
  yOpts: ";;;;{valueB}"
  result: feature
  taxonomy: ncbi
  report: ribbon
  reorient: true
  compactLegend: true
  plotRatio: 3
  ratio: 3
```
