## THIS IS NOT THE FINAL VERSION, BOTH THE README AND THE REST OF THE REPOSITORY ARE WIP

This repository is an attempt at transforming data from the [RAD-on system](https://radon.nauka.gov.pl/) into a knowledge graph using [yarrrml](https://rml.io/yarrrml/) and [RMLmapper](https://github.com/RMLio/rmlmapper-java). The idea of this project is to provide a querable knowledge graph which could be used to find information about Polish scientific institutions, scientists etc. and an easy way to recreate and develop the graph should it be necessary.

What can be found here? Let's take a look at the folders:

1. [yarrrml_files](https://github.com/kasprzakj/radon_kg_mapping/tree/main/yarrrml_files) contains yarrrml specific files in .yml format which can be used to generate RML mappings, which can then in turn be used with RMLmapper to generate the target turtle file.
2. [mappings](https://github.com/kasprzakj/radon_kg_mapping/tree/main/mappings) contains the middle-of-the-process RML mappings generated with yarrrml-parser.
3. [turtles](https://github.com/kasprzakj/radon_kg_mapping/tree/main/turtles) contains the final turtle files with the final knowledge graph.
4. [example_queries](https://github.com/kasprzakj/radon_kg_mapping/tree/main/example_queries) contains some example SPARQL queries performed on the graph and their results, together with an instruction on how to perform them.
5. [data_aquisition](https://github.com/kasprzakj/radon_kg_mapping/tree/main/data_acquisition) contains a Jupyter notebook with Python code showing a sample way of downloading the RAD-on data through a publically available API, as well as a requirements.txt file with all necessary dependencies.

A list of ontologies used for this project:
* [RDF](http://www.w3.org/1999/02/22-rdf-syntax-ns#)
* [RDFS](http://www.w3.org/2000/01/rdf-schema#)
* [XMLSchema](http://www.w3.org/2001/XMLSchema#)
* [Schema.org](http://schema.org/)
* [FOAF](<http://xmlns.com/foaf/0.1/>)
* [org](http://www.w3.org/ns/org#) – for relations between institutions and their branches
* [vcard](http://www.w3.org/2006/vcard/ns#) – for geolocational properties
* [VIVO](http://vivoweb.org/ontology/core#) – for university-specific properties 
* TBC (perhaps when we look into scientists more we will need something else)
