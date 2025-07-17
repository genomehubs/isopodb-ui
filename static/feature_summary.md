::recordlink{result=feature url="https://metazoa.ensembl.org/{assembly.identifiers[class:ensembl_metazoa_id].identifier}/Location/View?r={attributes.sequence_id}:{attributes.start}-{attributes.end}" condition="assembly.identifiers[class:ensembl_metazoa_id]" label="Ensembl Metazoa" color=#015365 description="Click to view this region in the Ensembl Metazoa Genome Browser"}

::recordlink{result=feature url="https://rapid.ensembl.org/{assembly.identifiers[class:ensembl_rapid_id].identifier}/Location/View?r={attributes.sequence_id}:{attributes.start}-{attributes.end}" condition="assembly.identifiers[class:ensembl_rapid_id]" label="Ensembl Rapid" color=#2378a9 description="Click to view this region in the Ensembl Rapid Genome Browser"}

::recordlink{result=feature url="https://boat.genomehubs.org/record?recordId={feature_id}&result=feature" condition="assembly.identifiers[class:boat_id]" label="BoaT" color=#31323f description="Click to view this region in BoaT" icon="/boat-icon.png"}
