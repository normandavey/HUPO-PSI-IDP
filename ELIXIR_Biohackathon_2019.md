# ELIXIR Hackathon 2019
**Venue:** Campus Les Berges de Seine, Paris

**Date:** November 18th-22nd

## Title

Improving the interoperability of the core intrinsically disordered protein (IDP) resource 


## Goals
The intrinsically disordered protein field generates large amounts of structural data, largely from Nuclear Magnetic Resonance (NMR), Small-angle X-ray scattering (SAXS), circular dichroism (CD) or Förster resonance energy transfer (FRET) experiments (Plitzko et al. 2017; Tompa 2011; Holmstrom et al. 2018; Felli and Pierattelli 2015; Tolchard et al. 2018). The raw data is stored in experimental method specific data repositories including SASBDB (Valentini et al. 2015), PCDDB (Whitmore et al. 2017) and the BMRB (Ulrich et al. 2008), and structural properties inferred from the data is curated directly from the literature by the DisProt resource (Piovesan et al. 2017). Currently, there is no data sharing between these resources. No standards or guidelines exist for the annotation, curation, storage and dissemination of IDP data and this has an adverse effect on reproducibility, interpretation, and dissemination of experimental IDP data. Furthermore, IDP annotations are significantly underrepresented in the ELIXIR core data resources, the standardisation of data-sharing between the core IDP resources will accelerate the inclusion of IDP data into these central repositories.

A key responsibility of the IDP community is the development of a framework to improve the reproducibility, interpretation, and dissemination of experimental data. The hackathon project will improve data sharing of the core IDP resources by achieving the following specific goals:
* Completion of the exchange format based on MIADE defining the minimal fundamental parameters to describe a structural disorder experiment
* Define and apply rules for the structural classification of the raw data stored in each experimental method specific data repository.
* Create RESTful APIs for each resource to distribute structural classification data using a standardised dissemination formats based on the Minimum Information About Disorder Experiments (MIADE) standard. 
* Develop a single RESTful API portal aggregating and distributing the structural classification level IDP data to streamline the integration of IDP data into the ELIXIR core data resources.
* Add cross-links between the resources to improve the visibility of the complementary data in each resource.


## Expected outcomes from Biohackathon and beyond

Improved interoperability in the IDP resources and the development of a single point of access for the  IDP data.

## Expected Audience: 
Type of participant needed to help with the project:

* Database developers - developers from the core data repositories in the IDP field.
* Experimentalist in IDP structural field - data producers for each of the experimental approaches tackled in the project.
* Standards experts - researchers with a background in the development of dissemination standards.
* FAIR experts - researchers with an understanding of FAIR approaches to data storage and dissemination.
* Programmers - coders with an interest in RESTful APIs, storage/dissemination standards and data FAIRification.

## Milestones:

<ins>**Milestone 1**</ins>
 
Definition of the exchange format based on MIADE defining the minimal fundamental parameters to describe a structural disorder experiment

**Task 1:** Formal definition of a JSON/TDT/XML exchange format for the dissemination of structural data using [MIADE](https://docs.google.com/document/d/1vVGQ40wyZAT27CBaWFdg2FTJK-AoAfPo2b1H-Uk6Fgo/edit?usp=sharing) as a guide. MIADE document should be updated to reflect development of the exchange format.
* Data should include:
  * **Unique Identifier (required):**  The primary identifier of the experimentally tested protein in a database describing the protein. The protein identifier should preferentially be a UniProt Accession from the UniProt database (e.g. UniProt:P47074) as most major IDP resource use UniProt accessions for protein mapping. The identifier should include an isoform and a version number if possible (e.g. UniProt:P47074-2.4).
  * **Alternative Identifier (optional):**  An alternative identifier for the protein. As identifiers are often not persistent, if possible, an alternative identifier(s) should be given, for example, a UniProt Identifier (e.g. UniProt:MAD3_YEAST), UniParc Accession (e.g. UniParc:UPI000012EB19) or an EnsEMBL Identifier (e.g. EnsEMBL:YJL013C)  . 
  * **Alias (optional):**  A commonly used name for the protein. For example, the recommended protein and gene name. If possible, the name that is used to describe the protein in the publication should be given (e.g. “Spindle assembly checkpoint component MAD3 ” ).
  * **Region Start (required):**  The start position of the experimental construct as mapped from the protein sequence defined in “Unique Identifier”.
  * **Region End (required):**  The end position of the experimental construct as mapped from the protein sequence defined in “Unique Identifier”.
  * **Region Sequence (required):**  The full sequence of the experimentally tested construct including any tags, alterations or modifications.
  * **Region Structure State (required):**  The structure state of the region as defined by the experimental data or as inferred by the experimentalist. Currently, limited to the binary classification of “Ordered” or “intrinsically disordered”.
  * **Experimental Method (required):**  The experimental method used to define the structural state of the protein region. Currently, these terms should be defined using the ECO controlled vocabulary.
  * **Reference Identifier (required):**  A link to the source of the experimental data underlying the entry. Ideally, this should describe a peer-reviewed publication (e.g. PubMed:12345678). Cross-references to experimental data in experimental method specific data repositories such as  SASBDB, PCDDB and BMRB can also be given. If none of these identifiers are available the details of the data producers should be given.
  * **Source Database Identifier (optional):**  If the experiment is annotated in an IDP database, the entry should be referenced (e.g. DisProt:DP12345).
  * **Attributes (optional):** Descriptive attributes that can be determined for the experimental data produced by the methods (e.g. Radius of gyration, mean and std dev of the chemical shifts.

<ins>**Milestone 2**</ins>
 
Define and apply rules for the structural classification of the raw data stored in each experimental method specific data repository.

**Task 1:** Define the structural properties (ordered/disordered/etc) determinable by each experimental method

**Task 2:** Define rules/algorithms to determine the structural properties (ordered/disordered/etc) determinable by each experimental method
 * This will require the input of experimentalists:
    * Pedro Romero - NMR
    * Hari Arthanari - NMR
    * Bonnie Wallace - CD
    * Cy Jefferies - SAXS
    * Dmitri Svergun - SAXS
  
**Task 3:** Apply rules/algorithms to determine structural properties of the region analysed by the structural disorder experiment

<ins>**Milestone 3**</ins>
Create RESTful APIs for each resource to distribute structural classification data using a standardised dissemination formats based on the Minimum Information About Disorder Experiments (MIADE) standard. 

**Task 1:** Each resource will implement a RESTful API for the dissemination of structural data
* server the following:
  * data on a structural disorder experiment in JSON/tdt/XML exchange format 
  * index of available data
 * mapped to common identifiers (UniProt,PubMed) and multiple entry points (protein, article, local identifier)

<ins>**Milestone 4**</ins>
Develop a single RESTful API portal aggregating and distributing the structural classification level IDP data to streamline the integration of IDP data into the ELIXIR core data resources.
* Aggregate data from:
  * PDB, DisProt, SASBDB, PCDDB and the BMRB 
* Docker 
* RESTful API
* Combined index
* Simple web frontend

<ins>**Milestone 5**</ins>
Improve the visibility of the complementary data in each resource.
**Task 1:** Add cross-links to other sources of data on the same region in other resources.

<ins>**Milestone 6**</ins>
Perform a meta analysis by cross-referencing data from each resource and PDB. 

**Task 1:** Calculate a range of summary statistics including:
* Overall coverage of each resource
* Overlap of each resource
* Overlap with DisProt/PDB
* Simple comparison of the metrics for overlapping datasets

## Contributors
| Contributor        | Affiliation   | Resource |
| ------------- |:-------------:|:-------------:|
| Norman Davey | Institute for Cancer Research, London, UK |
| Damiano Piovesan | University of Padua, Italy |  [Database of Intrisically Disordered Proteins (DisProt)](https://www.disprot.org/) |
| Ivan Mičetić | University of Padua, Italy|  [Database of Intrisically Disordered Proteins (DisProt)](https://www.disprot.org/) |
| Sergio Gomes Ramalli | Birkbeck, UK | [Protein Circular Dichroism Data Bank (PCDDB)](http://pcddb.cryst.bbk.ac.uk) |
| Al Kikhney | EMBL Hamburg, Germany | [Small Angle Scattering Biological Data Bank (SASBDB)](https://www.sasbdb.org*) |
| Cy Jefferies | EMBL Hamburg, Germany | [Small Angle Scattering Biological Data Bank (SASBDB)](https://www.sasbdb.org*) |
| Jonathan Wedell | University of Wisconsin, USA |  [Biological Magnetic Resonance Data Bank (BMRB)](http://www.bmrb.wisc.edu) |


## Reference Material: 
#### HUPO-PSI MIADE guidelines:
Full details are available [here](https://docs.google.com/document/d/1vVGQ40wyZAT27CBaWFdg2FTJK-AoAfPo2b1H-Uk6Fgo/edit?usp=sharing).

#### HUPO-PSI-ID XML format:
An annotated example of the HUPO-PSI-ID XML format is available [here](./HUPO-PSI-ID_XML_format_full_annotated.xml)

A simple example of the HUPO-PSI-ID XML format holding a IDR annotation is available [here](./HUPO-PSI-ID_XML_format_compact_NFAT_example.xml)

#### HUPO-PSI-ID TAB format:
An annotated example of the HUPO-PSI-ID TAB format is available [here](./HUPO-PSI-ID_TAB_format.xlsx)

#### Documentation:
The draft report "Preliminary draft of the standards and guidelines for the exchange of structural data relating to intrinsically disordered protein regions" is available [here](https://docs.google.com/document/d/1vVGQ40wyZAT27CBaWFdg2FTJK-AoAfPo2b1H-Uk6Fgo/edit?usp=sharing).
