::breadcrumbs[Ribbon plots]

Ribbon plots allow you to visualize synteny and rearrangements between pairs of genomes. Patterns in linkage group and gene order conservation differ across lineages.

As the distance between species increases for these bivalves, fewer shared genes remain in the same order and orientation, though remnants of ancestral linkage groups persist. Such plots help uncover genomic architecture evolution.

:::grid{container direction="row" spacing="1" inline}

```report
report: ribbon
reorient: true
compactLegend: true
x: assembly_id=queryA.assembly_id,queryB.assembly_id AND collate(sequence_id,busco_gene) AND feature_type=metazoa_odb10-busco-gene AND busco_status!=duplicated AND ancestral_unit
queryA: assembly--tax_name(Mytilus edulis)
queryB: assembly--tax_name(Mytilus coruscus)
cat: "ancestral_unit[20]=moll1,moll2,moll3,moll4,moll5,moll6,moll7,moll8,moll9,moll10,moll11,moll12,moll13,moll14,moll15,moll16,moll17,moll18,moll19,moll20"
xOpts: ;;;;Mytilus edulis
yOpts: ;;;;Mytilus coruscus
caption: Ribbon plot of Mytilus edulis and Mytilus coruscus using metazoa BUSCO genes
ratio: 3
result: feature
taxonomy: ncbi
size: 12
```

```report
report: ribbon
reorient: true
compactLegend: true
x: assembly_id=queryA.assembly_id,queryB.assembly_id AND collate(sequence_id,busco_gene) AND feature_type=metazoa_odb10-busco-gene AND busco_status!=duplicated AND ancestral_unit
queryA: assembly--tax_name(Mytilus edulis)
queryB: assembly--tax_name(Mytilisepta virgata)
cat: "ancestral_unit[20]=moll1,moll2,moll3,moll4,moll5,moll6,moll7,moll8,moll9,moll10,moll11,moll12,moll13,moll14,moll15,moll16,moll17,moll18,moll19,moll20"
xOpts: ;;;;Mytilus edulis
yOpts: ;;;;Mytilisepta virgata
caption: Ribbon plot of Mytilus edulis and Mytilisepta virgata using metazoa BUSCO genes
ratio: 3
result: feature
taxonomy: ncbi
size: 12
```

```report
report: ribbon
reorient: true
compactLegend: true
x: assembly_id=queryA.assembly_id,queryB.assembly_id AND collate(sequence_id,busco_gene) AND feature_type=metazoa_odb10-busco-gene AND busco_status!=duplicated AND ancestral_unit
queryA: assembly--tax_name(Mytilus edulis)
queryB: assembly--tax_name(Crassostrea virginica)
cat: "ancestral_unit[20]=moll1,moll2,moll3,moll4,moll5,moll6,moll7,moll8,moll9,moll10,moll11,moll12,moll13,moll14,moll15,moll16,moll17,moll18,moll19,moll20"
xOpts: ;;;;Mytilus edulis
yOpts: ;;;;Crassostrea virginica
caption: Ribbon plot of Mytilus edulis and Crassostrea virginica using metazoa BUSCO genes
ratio: 3
result: feature
taxonomy: ncbi
size: 12
```

:::

BoaT provides templates to generate Ribbon plots based on assembly accessions or taxon names, and color BUSCO loci by ancestral linkage groups.

:::grid{container direction="row" spacing="1"}

::include{pageId=templates/ribbonPlotByAssembly.md size=6}

::include{pageId=templates/ribbonPlotByTaxon.md size=6}

:::

:::grid{container direction="row" spacing="1"}

::include{pageId=templates/ribbonPlotByAssemblyMollusca.md size=6}

::include{pageId=templates/ribbonPlotByTaxonMollusca.md size=6}

:::
