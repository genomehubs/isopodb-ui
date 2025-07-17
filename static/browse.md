<!--
Content to display immediately below the search box when the user toggles "browse tree"
-->

MolluscDB uses the [NCBI taxonomy](https://www.ncbi.nlm.nih.gov/taxonomy) tree as its default backbone taxonomy. Tap the tree nodes below to browse the taxa available in MolluscDB or long press to search for data on a particular taxon.

:::grid{container direction=row spacing="1"}

```report
report: tree
x: tax_tree(6447[Mollusca]) AND tax_rank(order)
y: mollusca_odb10_complete_percent
levels: species,order
includeEstimates: true
collapseMonotypic: true
yOpts: 50,100
pointSize: 15
result: taxon
caption: |
  Tree showing BUSCO completeness of taxa in MolluscDB
  *(BUSCO v5, mollusca_odb10)*"
ratio: 2
size: 12
```

:::
