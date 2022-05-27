# graphemon
Extension of the lemon model for graphemes, grapheme variants, glyphs and beyond

# Foundations

The ontology model consists of three fundamental concepts:
* **Glyph**: A physical representation of a written script as defined by the CIDOC CRMtex extension
* **Grapheme**: A normalized version of a set of glyphs defined in a written language
* **GraphemeVariant**: A variant of a normalized form of a Grapheme

Defining the canonical Grapheme vs. the GraphemeVariants is a script-dependent task.

For example: In the cuneiform script, we consider a grapheme a new graphemvariant if
* it depicts the same meaning as the canonical Grapheme
* adds or removes cuneiform wedges in comparison to the canonical form
* shifts the order or position of wedges as compared to the canonical Grapheme

The nature of these definitions need to be adjusted by language, possibly be individual scholars.

## Representation of grapheme variants


