# Graphemon - Grapheme Model for ontologies
This repository contains a complimentary ontology model to the Ontolex-Lemon model for dictionaries.
Its goal is the representation of grpahemes and grapheme variants and the connection of these variants to actual representations of graphemes, e.g. glyphs on given mediums.
Documentation: https://situx.github.io/graphemon/

# Foundations
To explain the core of the ontology model, the following fundamental concepts should be explored:
* **Glyph**: A physical representation of a written script as defined by the CIDOC CRMtex extension
* **GraphemeVariant**: A variant of a normalized form of a set of Glyphs
* **Grapheme**: The description of a set of GrapheVariants which share a common identifier such as a Unicode code point or dictionary entry
* **GraphemeManifestiation**: Superclass of Grapheme and GraphemeVariant: A manifestation of a grapheme in a written or non-written form

Each Grapheme is expected to be assigned a GraphemVariant which should be marked as the canonical or standard grapheme variant.
This variant might be defined by a community of scholars or it might be inferred by an algorithm (e.g. the most occurring grapheme variant could be classified as the canonical variant)
The method of detection of a canonical variant should be documented in the vocabulary.

It also should be noted that defining cnonical Grapheme vs. the GraphemeVariants is a script-dependent and usually not a language-dependent task.

For example: In the cuneiform script, we consider a Grapheme a new Graphemvariant if
* it depicts the same meaning as the canonical Grapheme
* adds or removes cuneiform wedges in comparison to the canonical form
* shifts the order or position of wedges as compared to the canonical Grapheme

The nature of these definitions need to be adjusted by language, possibly be individual scholars.

# Graphemon Ontology Model

## Representation of grapheme variants
Grapheme variants might be representated in the following different ways:
* Using a description model for graphemes for a particular script (e.g. PaleoCodage, Gottstein, Chinese Character Description Language)
* Using an image representation for a particular script (e.g. SVG)
* Using related representations such as a 3D volume of a written grapheme

A description in at least two of the aforementioned representations allows for the calculation of similarities between grapheme variants and their expression in RDF.

For grapheme description models: These may also be expressed directly in RDF triples.

## GraphemeVariant Etymology

Similar to the representation of [lemonETY](https://github.com/anasfkhan81/lemonEty), this ontology model supports to model etymology relations of grapheme variants.

### Similarity of GraphemeVariants

GraphemeVariants can be distinguished by etymological relations (on a semantic level), but can also be related by similarity metrics targeting the appearance of either the Grapheme shape or description or the glyph shape or representation.
For example, to distinguish cuneiform signs, one may use image similarity measurements on representations of Graphemes in PNG or SVG and may choose String similarity metrics to highlight differences on String descriptions such as character description languages.
Results of these similarity calculations can be added as relations in the ontology model.

# Relation to existing ontology models

## Relation to the Ontolex-Lemon model

## Relation to the CIDOC-CRM CRMtex model

# Usage examples of the ontology model

This repository highlights two usage examples of the ontology model using the cuneiform language. The first example represents two cuneiform words and their grapheme variants, the second example higlights the relationship of two grapheme variants.

## Representation example: Cuneiform word "A" vs. Cuneiform word 2(disz)

The cuneiform word "A", with a sense of water consists of exactly one grapheme, "A", which may be depicted in at least two grapheme variants which may occur as glyph instances on certain cuneiform tablets.
Using the ontology model, these relations can be described.

## Relationship between Graphemes: Cuneiform Grapheme "A" is part of Grapheme AxA

This example highlights the vocabulary of relations between two graphemes. Given a Grapheme one, this Grapheme might be included in another grapheme.

The example which highlights this relation is the example of the cuneiform sign "A" which is included in the cuneiform sign "AxA".

# Application of the ontology model

While we concepted the ontology model for the usage for modeling cuneiform graphemes, our goal was to keep the ontology so general that it can be applied to other languages as well. The following applications may also be performed on other language corpora.

## Creation of machine learning resources

The ontology model may be used to query targeted data to create machine learning datasets based on glyphs.

# Applicability to other scripts

