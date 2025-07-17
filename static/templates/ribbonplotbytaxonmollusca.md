```template
id: ribbonPlotByTaxonMollusca
title: Ribbon plot using Mollusca BUSCO genes assigned to ALGs
description: |
  Show locations of all Mollusca BUSCO genes shared between a pair of species, coloured by ancestral linkage group
valueA_example: Cepaea hortensis
valueA_label: Taxon A
valueA_description: |
  Taxon name or ID to plot on x-axis
valueB_example: Achatina immaculata
valueB_label: Taxon B
valueB_description: |
  Taxon name or ID to plot on y-axis
url:
  path: /search
  query: assembly_id=queryA.assembly_id,queryB.assembly_id AND collate(sequence_id,busco_gene) AND feature_type=mollusca_odb10-busco-gene AND ancestral_unit AND busco_status!=duplicated AND ancestral_unit
  queryA: assembly--tax_name({valueA}) AND refseq_category=representative genome,reference genome
  queryB: assembly--tax_name({valueB}) AND refseq_category=representative genome,reference genome
  cat: "ancestral_unit[20]=moll1,moll2,moll3,moll4,moll5,moll6,moll7,moll8,moll9,moll10,moll11,moll12,moll13,moll14,moll15,moll16,moll17,moll18,moll19,moll20"
  xOpts: ";;;;{valueA}"
  yOpts: ";;;;{valueB}"
  result: feature
  taxonomy: ncbi
  report: ribbon
  reorient: true
  compactLegend: true
```
