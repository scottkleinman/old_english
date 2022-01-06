# README

## Introduction

_Beowulf_ is based on the [edition by Giuseppe Brunetti](http://www.maldura.unipd.it/dllags/brunetti/OE/TESTI/Beowulf/index.htm). The CONLL-U file was compiled by Scott Kleinman (scott.kleinman@csun.edu).

## Lemmas

- Hyphens are retained in proper noun lemmas like 'Gār-Dene'.

## `UPOS Labels`

- Demonstrative pronouns are labelled `DET` where they function as determiners, although they also have `PronType=Dem,` in the `FEATS` column.
- Possessive adjectives are labelled `ADJ` in the `UPOS` column, although they also have `PronType=Poss` in the `FEATS` column.

## `XPOS Labels`

|Tag |Description                                |
|----|-------------------------------------------|
|CC  |Coordinate Conjunction                     |
|CD  |Cardinal Number                            |
|DT  |Determiner                                 |
|IN  |Equivalent to UPOS ADP or SCONJ            |
|JJ  |Adjective                                  |
|JJR |Comparative Adjective                      |
|JJS |Superlative Adjective                      |
|NN  |Noun, singular or mass                     |
|NNP |Proper noun, singular                      |
|NNS |Noun, plural                               |
|PR  |Pronoun, not personal or possessive        |
|PRP |Personal pronoun                           |
|RB  |Adverb                                     |
|RBR |Comparative Adverb                         |
|RBS |Superlative Adverb                         |
|UH  |Interjection                               |
|VB  |Verb infinitive                            |
|VBDP|Past tense verb, plural                    |
|VBDS|Past tense verb, singular                  |
|VBG |Verb, gerund or present participle         |
|VBI |Verb, imperative                           |
|VBN |Verb, past participle                      |
|VBPS|Present tense verb, non-3rd person singular|
|VBPP|Present tense verb, non-3rd person plural  |
|VBZP|Present tense verb, 3rd person plural      |
|VBZS|Present tense verb, 3rd person singular    |

## `FEATS Labels`

- Relative, indefinite, and interrog pronouns are identified with `PronType=Rel`, `PronType=Indef`, and `PronType=Interrog`
- Personal pronouns are identified with `PronType=Prs`.
- Plural forms of verbs without distinct first, second, and third person inflections may not have a `Number` attribute in the `FEATS` column.
- Contractions have been expanded into two separate tokens (e.g. _ne_, _ah_ for _nah_), and the latter has an additional `Neg=Yes` attribute in the `FEATS` column. This may not be canonical UD version 2.
- Weak adjectives are labelled with `Strength=Weak`, but strong adjectives are not labelled.

## Notes

- Brunetti occasionally brackets text where words or letters are missing due to manuscript damage. Where it is possible to reconstruct words, the reconstructed words are used without indication. In one instance, reconstructed text is borrowed from Kevin Kiernan's _Electronic Beowulf_ in order to maximise the tokens available for machine learning.
- Certain phrasal expressions such as _þæs þe_ are parsed into separate tokens and part of speech and feature labels added as appropriate based on consultation with Kiernan's edition.
- Brunetti employs the `.` symbol as a sentence-internal punctuation mark, as well as a sentence final punctuation mark. The use of this symbol does not seem to correspond clearly to pointing in the manuscript, and there is no explanation of the mark's significance in his edition. Brunetti's usage has been preserved &mdash; but distinguished from punctuation marking sentence division &mdash; by recording the sentence-internal symbol as `.,`.
- On the whole, the text could use some improvements to the sentence segmentation.

**Last Update**: 2022-01-06
