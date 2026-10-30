::breadcrumbs[Ribbon plots]

Ribbon plots allow you to visualize synteny and rearrangements between assemblies. This example plot shows the conservation of synteny between 2 _Jaera_ species.

:::grid{container direction="row" spacing="1" inline}

```report
report: ribbon
reorient: true
compactLegend: true
x: assembly_id=queryA.assembly_id,queryB.assembly_id AND collate(sequence_id,busco_name) AND feature_type=arthropoda_odb12-busco-gene AND busco_status!=duplicated
queryA: assembly--tax_name(Jaera praehirsuta)
queryB: assembly--tax_name(Jaera albifrons)
xOpts: ;;;;Jaera praehirsuta
yOpts: ;;;;Jaera albifrons
caption: Ribbon plot of Jaera praehirsuta and Jaera albifrons using Arthropoda BUSCO genes
plotRatio: 3
ratio: 3
result: feature
taxonomy: ncbi
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
