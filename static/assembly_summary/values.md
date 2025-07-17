::valuerow{suffix="span" description="The total length of assembly {assemblyId} is {count} base pairs" value="assembly.attributes.assembly_span.value" unit=b}

::valuerow{suffix="level" description="Assembly {assemblyId} has been assembled to the {lc_attributes.assembly_level.value} level" value="assembly.attributes.assembly_level.value"}

::valuerow{suffix="chromosomes" description="Assembly {assemblyId} has {count} chromosomes" value="assembly.attributes.chromosome_count.value"}

::valuerow{condition="{attributes.assembly_level.value}=Chromosome" suffix="scaffolds" description="Assembly {assemblyId} has {count} scaffolds" value="assembly.attributes.scaffold_count.value"}

::valuerow{condition="{attributes.assembly_level.value}=Chromosome" suffix="n50" description="The scaffold N50 of assembly {assemblyId} is {count}" value="assembly.attributes.scaffold_n50.value" unit=b}

::valuerow{condition="{attributes.assembly_level.value}=Contig,Scaffold" suffix="{assembly.lc_attributes.assembly_level.value}s" description="Assembly {assemblyId} has {count} {assembly.lc_attributes.assembly_level.value}s" value="assembly.attributes.scaffold_count.value"}

::valuerow{condition="{assembly.attributes.assembly_level.value}=Contig,Scaffold" suffix="n50" description="The {assembly.lc_attributes.assembly_level.value} N50 of assembly {assemblyId} is {count}" value="attributes.scaffold_n50.value" unit=b}

::valuerow{suffix="BUSCO complete" description="Assembly {assemblyId} has a BUSCO {assembly.attributes.busco_lineage.value} completeness score of {count}" value="assembly.attributes.busco_completeness.value" unit=%}
