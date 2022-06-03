# Graphemon - Grapheme Model for ontologies
This repository contains a complimentary ontology model to the Ontolex-Lemon model for dictionaries.
Its goal is the representation of grpahemes and grapheme variants and the connection of these variants to actual representations of graphemes, e.g. glyphs on given mediums.

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

## GraphemeVariant Etymology

Similar to the representation of (https://github.com/anasfkhan81/lemonEty)[lemonETY], this ontology model supports to model etymology relations of grapheme variants.

### Similarity of GraphemeVariants

GraphemeVariants can be distinguished by etymological relations (on a semantic level), but can also be related by similarity metrics targeting the appearance of either the Grapheme shape or description or the glyph shape or representation.
For example, to distinguish cuneiform signs, one may use image similarity measurements on representations of Graphemes in PNG or SVG and may choose String similarity metrics to highlight differences on String descriptions such as character description languages.
Results of these similarity calculations can be added as relations in the ontology model.

# Relation to existing ontology models

## Relation to the Ontolex-Lemon model

## Relation to the CIDOC-CRM CRMtex model

# Usage examples of the ontology model

## Cuneiform word "A"

# Application of the ontology model

## Creation of machine learning resources

The ontology model may be used to query targeted data to create machine learning datasets based on glyphs.

# Applicability to other scripts


