<!--
Content to display immediately below the search box when the user toggles "browse tree"
-->

IsopoDB uses the [NCBI taxonomy](https://www.ncbi.nlm.nih.gov/taxonomy) tree as its default backbone taxonomy. Tap the tree nodes below to browse the taxa available in IsopoDB or long press to search for data on a particular taxon.

:::grid{container direction=row spacing="1"}

```report
report: tree
x: tax_tree(6820[Peracarida]) AND tax_rank(species)
y: arthropoda_odb12_complete
includeEstimates: true
collapseMonotypic: true
yOpts: 1000,1600
pointSize: 15
result: taxon
caption: |
  Tree showing BUSCO v6 completeness of taxa in IsopoDB
  using the arthropoda_odb12 lineage
ratio: 3
plotRatio: 3
size: 12
treeStyle: rect
```

:::
