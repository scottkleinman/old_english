# README

## Introduction

This folder contains texts in various states of completion which intended for training an Old English language model. Each text subfolder contains its own `README` file with a description of the subfolder's contents. This `README` file provides a general overview of text format and annotation process.

The texts were initially produced by Scott Kleinman at California State University, Northridge (scott.kleinman@csun.edu). Some texts were annotated by undergraduate and MA students at CSUN. Contributors for each text are credited in the individual `README` files.

Each text file is in [CONLL-U](https://universaldependencies.org/format.html) format with `ID`, `FORM`, `LEMMA`, `UPOS`, and `FEATS` labels. Where available, preliminary `XPOS` labels are also provided (see the discussion on *XPOS Labels* below). Sentences are divided by blank lines, and no sentence metadata is provided. This is to allow relatively easy import procedures to tools like [spaCy](https://spacy.io/). Where metadata is available, it is provided in a separate file.

Texts are not intended to be digital editions; their primary function is for training and use by NLP tools. As a result information such as line numbers in poetry is not included. Texts are normally based a published edition but do not correspond exactly to the edition since they are modified to conform to this project's formatting and annotation principles. In some cases, labels have been applied automatically by pattern matching or machine learning tools, and the results have not been fully checked by a human eye. The state of completion will be indicated in the text's `README` file.

## `FORM` Labels

Whatever is found in the edition on which the text is based, diacritics have been removed from the form given for each token. In general, contractions such as _næs_ are broken into multiple token lines with the following format:

```markdown
1-2 næs
1 ne
2 wæs
```

If this procedure is not followed in an individual text, it will be noted in the text's `README` file.

## `LEMMA` Labels

Assigning labels to words in languages without standard spellings is an immense problem. In Old English, dialectal and scribal variation &mdash; particularly in vowels &mdash; make it difficult to choose consistently a single lemma for a word. Dictionaries and editions are often at odds, making them unsuitable for use as a single frame of reference. In general, lemmas are coerced to West Saxon spellings but little attempt has been made to reflect earlier or later spellings consistently. Where the published edition provides a glossary, lemmas are based on the glossary headwords, subject to West-Saxonification and the normalising principles discussed below. This means that lemmas may differ between texts, and the project as a whole does not yet have a unified gazeteer of lemmas or a plan to resolve or link alternative forms.

All lemmas are normalised to lower case (except proper nouns), and all instances of _ð_ are changed to _þ_. Unless noted in an individual text's `README`, all punctuation marks are removed. Hence frequent glossary forms like _(ġe)sēon_ will appear either as _ġesēon_ or _sēon_, with the version chosen generally the one that most resembles the word's form. Hyphens are removed from compound words unless otherwise noted in an individual text's `README`. Long vowels are noted using diacritics and palatal _ċ_ and _ġ_ are also noted using a rapid "best guess" assignment. Whilst these are only pronunciation guides, they may be valuable if the data is used to generate glossaries for digital editions.

## `UPOS` Labels

`UPOS` labels are confined to the UD version 2 tags listed on the [Universal Dependencies website](https://universaldependencies.org/u/pos/index.html
): `ADJ`, `ADP`, `ADV`, `AUX`, `CCONJ`, `DET`, `INTJ`, `NOUN`, `NUM`, `PART`, `PRON`, `PROPN`, `PUNCT`, `SCONJ`, `SYM`, `VERB`, `X`. At the time of writing (5 January 2022), the `AUX` and `PART` labels are not used. Words that can be categorised as auxiliaries or particles are labelled with parts of speech most closely associated with the forms from which the words are etymologically derived.

This still leaves some areas of inconsistency, such as whether froms like _se_ are determiners or pronouns. Labelling may not be entirely consistent, especially between different texts. Individual texts will provide notes of the guidelines used in their `README` files. In some cases, `UPOS` labels need to be read alongside the contents of the `FEATS` column in order to disambuate grammatical functions.

## `XPOS` Labels

`XPOS` labels are intended to provide more language-specific information about the forms and functions of words. Because they provide more detailed information, they take longer to produce and have thus been given a lower priority in the annotation process. Additionally, there is no standard set of tags for Old English, and devising what is required really needs to be a collaborative effort.

It is worth considering two bases for comparison. The [York-Helsinki Corpus](https://www-users.york.ac.uk/~lang18/pcorpus.html) (and its derivatives) contains texts annotated with a wealth of morphosyntactic information. In some cases, this includes labels not typically found in the large language models that drive current machine-learning tools. Some annotations are also overkill for those who wish to generate glossaries, since the information is rarely found in the glossaries of printed or even digital editions. In other cases, the York-Helsinki Corpus does not provide information that would enable the production of a complete CONNL-U file. That said, it does provide tag forms that provide some guidance for producing a set of tags appropriate for Old English. Another basis for comparison might be the [treebank for Gothic](https://universaldependencies.org/treebanks/got_proiel/index.html), another early Germanic language. Whilst this provides a closer analogue to what we are trying to produce for Old English, the differences between the two languages are significant enough that a simple mapping of tags is insufficient.

As a result of the uncertainty about what `XPOS` labels to provide for Old English, it has been deemed necessary to use a simplified set of tags used commonly in Modern English treebanks, even if they are manifestly inadequate for Old English. In some cases, these may be converted from annotations in corpora based on the York-Helsinki Corpus, and their primary intent has been for use in developing the contents of the `FEATS` column. Suffice to say, `XPOS` labels, where they exist, will need to be thoroughly revisited in all the texts.

## The `FEATS` Labels

Labels of morphosyntactic are confined to the UD version 2 tags listed on the [Universal Dependencies website](https://universaldependencies.org/u/feat/index.html
). Only a subset of tags are used, and the labelling system may not be entirely consistent between different texts. There is likely to be the greatest inconsistency around pronouns and determiners, but some forms may be also be missing features in some texts that are labelled in other texts. This is a result of the growing familiarity with the labelling system and the materials to be labelled over time. Eventually, it will be necessary to standardise.

## The Other Columns

The other CONLL-U columns are devoted to syntactic information, particularly syntactic dependencies. Due to time constraints, it has not been possible to label texts with this information.

**Last Update**: 2022-01-05
