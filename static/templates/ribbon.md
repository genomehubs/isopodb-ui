::breadcrumbs[Ribbon plots]

Ribbon plots visualise synteny and rearrangements between assemblies. This example plot shows the conservation of synteny between 2 _Jaera_ species and breakdown of synteny as the evolutionary distance increases to _Asellus aquaticus_.

:::grid{container direction="row" spacing="1" inline}

```report
report: ribbon
x: assembly_id=GCA_977012755.1,GCA_965208005.1,GCA_964212115.1 AND feature_type=arthropoda_odb12-busco-gene AND busco_status!=duplicated AND collate(sequence_id,busco_name)
cat: sequence_id[20]+
compactLegend: true
reorient: true
ribbonAlign: reference
ribbonPassThrough: true
result: feature
taxonomy: ncbi
ratio: 2
size: 12
```

:::

<hr />

## Ribbon plot templates

Use the templates below to generate Ribbon plots based on assembly accessions or taxon names.

:::grid{container direction="row" spacing="1"}

::include{pageId=templates/ribbonPlotByAssembly.md size=6}

::include{pageId=templates/ribbonPlotByTaxon.md size=6}

:::
