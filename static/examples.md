<!--
Content to display immediately below the search box when the user toggles "show examples"
-->

Search the taxon, assembly or feature indexes with example queries:

## Taxon search

- [Show all complete, missing and fragmented BUSCO genes for species in the phylum Nematoda](/search?query=tax_tree%28nematoda%29%20AND%20nematoda_odb10_complete&result=taxon&includeEstimates=false&taxonomy=ncbi&offset=0&fields=nematoda_odb10_complete%2Cnematoda_odb10_fragmented%2Cnematoda_odb10_missing)
- [Lepidoptera families for which BUSCO gene `11066at7088` is missing from all analysed assemblies](/search?result=taxon&includeEstimates=true&taxonomy=ncbi&offset=0&fields=lepidoptera_odb10_missing&query=tax_rank%28family%29%20AND%20lepidoptera_odb10_missing%3D11066at7088)

## Assembly search

- [Assemblies with BUSCO lineage Metazoa completeness over 90%](/search?query=length%28metazoa_odb10_complete%29%3E856&result=assembly&taxonomy=ncbi&fields=metazoa_odb10_complete%2Cassembly_level%2Cassembly_span)
- [Assemblies from species in order Lepidoptera with N50 greater than 1Mbp but at least 5% missing BUSCO genes](/search?query=tax_tree%28lepidoptera%29%20AND%20scaffold_n50%3E1000000%20AND%20length%28lepidoptera_odb10_missing%29%3E264&result=assembly&taxonomy=ncbi&fields=assembly_level%2Cassembly_span%2Ccontig_n50%2Cscaffold_n50)

## Feature search

- [100kb windows from assembly GCA_905147045.1 with GC content between 30-50%](/search?query=assembly_id%3DGCA_905147045.1%20AND%20feature_type%3Dwindow-100000%20AND%20gc%3E0.3%20AND%20gc%3C0.5&result=feature&taxonomy=ncbi)
