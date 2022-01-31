## QC

### all filenames must contain KEY4:
gensp.strain.gnm.[.ann].KEY4.[...]

### YAML in general
- do not use tab characters anywhere
- place quotes around values containing ":" and other YAML-relevant characters, including line breaks
- separate documents within a file (e.g. strains descriptions file) with **---**, not **###** or something else

### README.yaml:
- fields may be _none_ other than:
scientific_name_abbrev, license, publication_title, taxid, geoseries, expression_unit, dataset_release_date, related_to, bioproject, data_curators, synopsis, genotype, source, local_file_creation_date, provenance, identifier, keywords, publication_doi, citations, genbank_accession, dataset_doi, contributors, original_file_creation_date, description, public_access_level, scientific_name, genotyping_method, sraproject, genotyping_platform
- identifier must be full name of collection (e.g. **PI483463.gnm1.ann1.3Q3Q**, not just **3Q3Q**)
- content shared between READMEs must be **identical**: for example, if a publication is in a genomic README and an annotation README, the publication titles must match exactly.

### gene_models_main.gff3
- must have ID and/or Name attributes in every record
  1. If ONLY ID present, then it must be an LIS conformant ID: gensp.strain.gnm.ann.ShortName.
  2. If Name is also present, then it can be ShortName and the mine loader will ignore ID and prepend the full yuck to Name for the primaryIdentifier.
  3. A third option is to set primaryIdentifier=ID and secondaryIdentifier=Name with a loader option.
- IDs must match IDs in corresponding FASTA files (.transcript, .cds) 

### transcript FASTA files
- IDs match IDs in GFFs
- use transcript, not mrna, filename suffix
  - WRONG: glyso.F_IGA1003.gnm1.ann1.G61B.mrna.fna.gz
  - CORRECT: glyso.F_IGA1003.gnm1.ann1.G61B.transcript.fna.gz
