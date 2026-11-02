::breadcrumbs[Oxford plots]

Oxford plots visualise synteny and rearrangements between pairs of genomes. Patterns in linkage group and gene order conservation differ across lineages.

As the distance between species increases for these species pairs, fewer shared genes remain in the same order and orientation, though remnants of ancestral linkage groups persist. Such plots help uncover genomic architecture evolution.

:::grid{container direction="row" spacing="1" inline}

```report
report: oxford
reorient: true
compactLegend: true
x: assembly_id=queryA.assembly_id,queryB.assembly_id AND collate(sequence_id,busco_name) AND feature_type=arthropoda_odb12-busco-gene AND busco_status!=duplicated
queryA: assembly--tax_name(Jaera praehirsuta)
queryB: assembly--tax_name(Jaera albifrons)
xOpts: ;;;;Jaera praehirsuta
yOpts: ;;;;Jaera albifrons
caption: Oxford plot of Jaera praehirsuta and Jaera albifrons using arthropoda BUSCO genes
plotRatio: 1
result: feature
taxonomy: ncbi
size: 4
```

```report
report: oxford
reorient: true
compactLegend: true
x: assembly_id=queryA.assembly_id,queryB.assembly_id AND collate(sequence_id,busco_name) AND feature_type=arthropoda_odb12-busco-gene AND busco_status!=duplicated
queryA: assembly--tax_name(Anilocra frontalis)
queryB: assembly--tax_name(Ceratothoa steindachneri)
xOpts: ;;;;Anilocra frontalis
yOpts: ;;;;Ceratothoa steindachneri
caption: Oxford plot of Anilocra frontalis and Ceratothoa steindachneri using arthropoda BUSCO genes
plotRatio: 1
result: feature
taxonomy: ncbi
size: 4
```

```report
report: oxford
reorient: true
compactLegend: true
x: assembly_id=queryA.assembly_id,queryB.assembly_id AND collate(sequence_id,busco_name) AND feature_type=arthropoda_odb12-busco-gene AND busco_status!=duplicated
queryA: assembly--tax_name(Hemioniscus balani)
queryB: assembly--tax_name(Niphargus gammariformis)
xOpts: ;;;;Hemioniscus balani
yOpts: ;;;;Niphargus gammariformis
caption: Oxford plot of Hemioniscus balani and Niphargus gammariformis using arthropoda BUSCO genes
plotRatio: 1
result: feature
taxonomy: ncbi
size: 4
```

:::

<hr />

## Oxford plot templates

Use the templates below to generate Oxford plots based on assembly accessions or taxon names.

:::grid{container direction="row" spacing="1"}

::include{pageId=templates/oxfordPlotByAssembly.md size=6}

::include{pageId=templates/oxfordPlotByTaxon.md size=6}

:::
