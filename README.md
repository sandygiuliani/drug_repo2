# drug_repo2 #  
_a bio-/chemoinformatics pipeline for drug repositioning applied to schistosomiasis_  

![drug_repo_img](https://github.com/sandygiuliani/media/blob/master/drug_repo_img.png)
  
## Table of contents 
- [FAQ](#faq)
- [Contents of the repository](#contents-of-repository)
- [Requirements](#requirements)
- [Instructions](#instructions)
- [License](#license)
- [Diclaimer](#disclaimer)
- [Contact](#contact)



## FAQ  
Q. What is drug repositioning?   
A. The usage of a known drug for a different therapeutic indication. If you are not familiar with this at all, try [Wikipedia](http://en.wikipedia.org/wiki/Drug_repositioning)  
Q. What is schistosomiasis?  
A. A very nasty parasitic disease affecting over 200 million people. Learn more about schistosomiasis on the [World Health Organization website](http://www.who.int/topics/schistosomiasis/en/)  
Q. How does the tool work?  
A. By mapping! known drugs -> their targets -> their domain architecture -> parasite targets  
Q. I am reading this README on my local machine, why is the formatting all weird?  
A. This README is formatted in GitHub markdown, please open it on GitHub. I will include an instructions-only plain text readme soon  
  

## <a name="contents-of-repository"></a>Contents of repository

| File  | Description | Accession date |
| ------------- | ------------- | ------------- |
| **drug_repo.py**  | Python script that reads input files (chemb/drugbank), filters data, extracts relevant info for mapping with domain architecture info. It is being developed at the moment.    | n/a |
| **config.py**    | configuration file    |  n/a |
| **README.md**    | this readme file   | n/a |
| **LICENSE.md**    | license    | n/a |
| chembl\_drugs.txt    | ChEMBL drugs; downloaded from [ChEMBL](http://www.ebi.ac.uk/chembl/drugstore/), Dec 15 data freeze| 20/09/2016  |
| chembl\_drugtargets.txt    | ChEMBL drug targets; downloaded from [ChEMBL](http://www.ebi.ac.uk/chembl/drug/targets/), Dec 15 data freeze, no manual edits| 20/09/2016  |
| chembl\_uniprot\_mapping.txt    | ChEMBL uniprot mapping, chembl ID to UniProt codes; downloaded from the ChEMBL 18 release page: ftp://ftp.ebi.ac.uk/pub/databases/chembl/ChEMBLdb/releases/chembl_18/|TBD     |  
|small\_molecule\_target\_ids\_all.csv    |   DrugBank Drug Target Identifier/Small Molecule Drugs; downloaded from [DrugBank](http://www.drugbank.ca/downloads#protein-identifiers) (if necessary, all\_target\_ids\_all.csv is also available) |TBD   |
|  uniprot_pdb.csv  |  Uniprot to pdb mapping file; downloaded from [SIFTS](http://www.ebi.ac.uk/pdbe/docs/sifts/quick.html) (if necessary, a tsv version is also available)|TBD     |  
|  lig\_pairs.lst  |   pdb to ligand mapping file; downloaded from [PDBsum downloads](http://www.ebi.ac.uk/thornton-srv/databases/cgi-bin/pdbsum/GetPage.pl?doc=TRUE&template=downloads.html&pdbcode=n/a) (if necessary, the het\_pairs.lst version is also available)  |  TBD | 
|  Components-smiles-oa.smi  |   chemical components dictionary in smiles format; downloaded from [RCSB Ligand Expo Downloads](http://ligand-expo.rcsb.org/ld-download.html), in the SMILES/InChi data files (if necessary, stereo versions and CACTVS-generated versions available)  |  TBD | 
|  pointless_het.csv  |  contains list of 'pointless' het ligands, including aminoacids, nucleotides, metals and crystallographic solvets/aids     |  n/a | 
|all.sdf|DrugBank drugs in sdf format; downloaded from [DrugBank](http://www.drugbank.ca/downloads#structures)|16/07/2014 |
|speclist.txt| taxonomic codes and mnemonic codes for all species; downloaded from [UniProt](http://www.uniprot.org/docs/speclist.txt)|TBD|  
|pdb_pfam_mapping.txt| PDB IDs to Pfam domains and residue numbers; downloaded from ftp://ftp.ebi.ac.uk/pub/databases/Pfam/mappings/| TBD |  
  

  

##Requirements   
* BioPhython - Freely available on the [BioPython website](http://biopython.org/)(we have used release 1.64)  
* ArchIndex/ArchSchema - kindly provided by Dr Laskowski. For more information, please visit the [ArchSchema website](http://www.ebi.ac.uk/thornton-srv/databases/archschema), or read the [main reference for ArchSchema](http://www.ncbi.nlm.nih.gov/pubmed/20299327)  
* SMSD (Small Molecule Subgraph Detector). For more information, please visit the [SMSD website](http://www.ebi.ac.uk/thornton-srv/software/SMSD/), the [GitHub repository](https://github.com/asad/SMSD), or read the [main reference for SMSD](http://www.jcheminf.com/content/1/1/12)  
* MODELLER, for homology modelling (only for step 10). See [MODELLER website](https://salilab.org/modeller/)  
* arch_schema_cath.tsv (UniProt IDs to CATH domains and residue numbers), to be downloaded from ftp://ftp.biochem.ucl.ac.uk/pub/gene3d_data/CURRENT_RELEASE/  


##Instructions  
* clone the repository  
* check requirements
* modify the config.py file according to your needs  
* run the script (>python drug_repo.py)
  

##License  
Copyright &copy; 2016 Sandra Giuliani  
This repository is licensed under the terms of the MIT license. Please see the [license file](LICENSE.md) for more information. The MIT license is approved by the [Open Source Initiative](http://opensource.org/licenses)  
  


##Disclaimer   
THIS IS A WORK IN PROGRESS.  This is version 2 of the original [drug_repo](https://github.com/sandygiuliani/drug_repo).  
  

##Contact     
Feedback is very welcome, please drop me a line at: sandraxgiuliani [at] gmail [dot] com  
You might also want to follow me on Twitter [@sandygiuliani](https://twitter.com/sandygiuliani) or visit my [personal website](http://www.sandragiuliani.com/).  
