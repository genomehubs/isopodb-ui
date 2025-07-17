```template
id: buscoStatusList
title: Table of BUSCO genes
description: |
  Show per lineage counts for each BUSCO status including a list of IDs for one status
valueA_example: class
valueA_label: Taxonomic rank
valueA_description: |
  Taxonomic rank  to show results for
valueB_example: mollusca_odb10
valueB_label: BUSCO lineage
valueB_description: |
  BUSCO lineage to show results for
valueC_example: missing
valueC_label: BUSCO status
valueC_description: |
  BUSCO status to include a list of IDs for
url:
  path: /search
  query: "tax_rank({valueA})"
  fields: "{valueB}_complete,{valueB}_duplicated,{valueB}_fragmented,{valueB}_missing,{valueB}_single,{valueB}_{valueC}:value"
  includeEstimates: true
  result: taxon
  taxonomy: ncbi
```
