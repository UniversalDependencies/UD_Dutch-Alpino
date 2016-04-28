The UD Dutch treebank is based on the Alpino treebank.
The data were used in the CoNLL-X Shared Task in dependency parsing (2006); the CoNLL version
was taken and converted to the Prague dependency style as a part of HamleDT (since 2011).
Later versions of HamleDT added a conversion to the Stanford dependencies (2014) and to
Universal Dependencies (HamleDT 3.0, 2015). The conversion path from the original Alpino still
goes through the CoNLL-X format and the Prague dependencies, which may occasionally lead to
loss of information. The first release of Universal Dependencies that includes this treebank
is UD v1.2 in November 2015. It is essentially the HamleDT conversion but the data is not
identical to HamleDT 3.0 because the conversion procedure has been further improved.


References:

http://odur.let.rug.nl/~vannoord/trees/
http://ufal.mff.cuni.cz/hamledt ... HamleDT
http://ufal.mff.cuni.cz/treex ... Treex is the software used for conversion
http://ufal.mff.cuni.cz/interset ... Interset was used to convert POS tags and features

@inproceedings{nl,
  author    = {Leonoor van der Beek and Bouma, Gosse and Daciuk, Jan and Gaustad, Tanja and Malouf, Robert and Gertjan van Noord and Prins, Robbert and Villada, Begoña},
  year      = {2002},
  title     = {Chapter 5. The {Alpino} Dependency Treebank},
  booktitle = {Algorithms for Linguistic Processing {NWO PIONIER} Progress Report},
  address   = {Groningen, The Netherlands},
  url       = {http://odur.let.rug.nl/~vannoord/trees/Papers/report_ch5.pdf}
}


Changelog

2016-05-15 v1.3
  * Multi-word expressions that were collapsed into one node (with underscores)
    are split again. This needs to be revisited and POS tags and MWE-internal
    relations improved.
  * Fixed adverbs that were attached as nmod; correct: advmod.
  * Copulas with clausal complements are now heads.
  * Relative pronouns are no longer treated as subordinating conjunctions.
    More work is needed: now all are attached as 'dobj', which may not be correct;
    noun phrases with relative determiners (welke boeken) and relative prepositional
    phrases (bij wat) are not handled properly.
  * Reversed relation finite auxiliary "heb" – participle.
  * Infinitives under modal verbs are now 'xcomp', not 'aux'.


=== Machine-readable metadata =================================================
Documentation status: stub
Data source: automatic
Data available since: UD v1.2
License: GNU GPL 3.0
Genre: news
Contributors: Zeman, Daniel; Žabokrtský, Zdeněk
===============================================================================
