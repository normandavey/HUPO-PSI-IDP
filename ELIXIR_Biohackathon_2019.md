# ELIXIR Hackathon 2019
**Venue:** Campus Les Berges de Seine, Paris

**Date:** November 18th-22nd

## Title

Improving the interoperability of the core intrinsically disordered protein (IDP) resource 


## Goals
The intrinsically disordered protein field generates large amounts of structural data. The raw data is stored in experimental method specific data repositories including SASBDB (Valentini et al. 2015), PCDDB (Whitmore et al. 2017) and the BMRB (Ulrich et al. 2008), and structural properties inferred from the data is curated directly from the literature by the DisProt resource (Piovesan et al. 2017). Currently, there is no data sharing between these resources. A key responsibility of the IDP community is the development of a framework to improve the reproducibility, interpretation, and dissemination of experimental data. The hackathon project will improve data sharing of the core IDP resources. Furthermore, IDP annotations are significantly underrepresented in the ELIXIR core data resources, the standardisation of data-sharing between the core IDP resources will accelerate the inclusion of IDP data into these central repositories.

The project has the following specific aims:
* Completion of the exchange format based on MIADE defining the minimal fundamental parameters to describe a structural disorder experiment
* Define and apply rules for the structural classification of the raw data stored in each experimental method specific data repository.
* Create RESTful APIs for each resource to distribute structural classification data using a standardised dissemination formats based on the Minimum Information About Disorder Experiments (MIADE) standard. 
* Add cross-links between the resources to improve the visibility of the complementary data in each resource.
* Develop a single RESTful API portal aggregating and distributing the structural classification level IDP data to streamline the integration of IDP data into the ELIXIR core data resources.

### Milestones:
**Milestone 1** Completion of the exchange format based on MIADE defining the minimal fundamental parameters to describe a structural disorder experiment

>**Task 1:** 

## Contributors

* Norman Davey, Institute for Cancer Research, London, UK **norman.davey@icr.ac.uk**
* Sergio Gomes Ramalli, Birkbeck, UK - Protein Circular Dichroism Data Bank (PCDDB)
* Al Kikhney, EMBL Hamburg, Germany - Small Angle Scattering Biological Data Bank (SASBDB)
* Cy Jefferies, EMBL Hamburg, Germany - Small Angle Scattering Biological Data Bank (SASBDB)
* Jonathan Wedell, University of Wisconsin, USA - Biological Magnetic Resonance Data Bank (BMRB)

## Expected outcomes from Biohackathon and beyond

Improved interoperability in the IDP resources and the development of a single point of access for the  IDP data.

## Expected Audience: 
Type of participant needed to help with the project:

* Database developers - developers from the core data repositories in the IDP field.
* Experimentalist in IDP structural field - data producers for each of the experimental approaches tackled in the project.
* Standards experts - researchers with a background in the development of dissemination standards.
* FAIR experts - researchers with an understanding of FAIR approaches to data storage and dissemination.
* Programmers - coders with an interest in RESTful APIs, storage/dissemination standards and data FAIRification.

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

