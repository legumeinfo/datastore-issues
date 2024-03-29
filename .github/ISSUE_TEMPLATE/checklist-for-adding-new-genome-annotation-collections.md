---
name: Checklist for adding new genome+annotation collections
about: Checklist of tasks associated with new genome and annotation collections
title: ''
labels: ''
assignees: ''

---

---
name: New genomes+annotations checklist
about: Checklist of tasks associated with new genome and annotation collections
---

### Main steps for adding new genome and annotation collections

# Genus/species/collection names: 
What are the collection types and names? Example: 
- Lens/culinaris/genomes/CDC_Redberry.gnm2.7C5P 
- Lens/culinaris/annotations/CDC_Redberry.gnm2.ann1.5FB4

- [ ] Add collection(s) to the Data Store, including commits to datastore-metadata
- [ ] Validate the README(s)
- [ ] Update about_this_collection.yml
- [ ] Calculate AHRD functional annotations 
- [ ] Calculate gene family assignments (.gfa) 
- [ ] Add to pan-gene set 
- [ ] Load relevant mine 
- [ ] Add BLAST targets 
- [ ] Incorporate into GCV 
- [ ] Update the jekyll collections listing 
- [ ] Update browser configs
- [ ] run BUSCO
- [ ] Update DSCensor
- [ ] Add LINKOUTS to datastore, refresh linkout service
