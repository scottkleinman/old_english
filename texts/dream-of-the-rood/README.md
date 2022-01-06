# README

## Introduction

_The Dream of the Rood_ is based on the text given by Peter Baker in his _Old English Aerobics_. The CONLL-U file was compiled by Scott Kleinman (scott.kleinman@csun.edu).

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
|VBZP|Present tense verb, 3rd person plural      |
|VBZS|Present tense verb, 3rd person singular    |

## `FEATS Labels`

- Relative, indefinite, and interrog pronouns are identified with `PronType=Rel`, `PronType=Indef`, and `PronType=Interrog`
- Personal pronouns are identified with `PronType=Prs`.
- Plural forms of verbs without distinct first, second, and third person inflections may not have a `Number` attribute in the `FEATS` column.
- There is only one contraction: "nah". This has been expanded into two separate tokens (_ne_, _ah_), and the latter has an additional `Neg=Yes` attribute in the `FEATS` column. This may not be canonical UD version 2.
- Weak adjectives are labelled with `Strength=Weak`, but strong adjectives are not labelled.

**Last Update**: 2022-01-05
