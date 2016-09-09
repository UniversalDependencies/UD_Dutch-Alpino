=== Machine-readable metadata =================================================
Documentation status: stub
Data source: automatic
Data available since: UD v1.2
License: CC BY-SA 4.0
Genre: news
Contributors: Zeman, Daniel; Žabokrtský, Zdeněk
Contact: zeman@ufal.mff.cuni.cz
===============================================================================

The UD Dutch treebank is based on the Alpino treebank.
The data were used in the CoNLL-X Shared Task in dependency parsing (2006); the CoNLL version
was taken and converted to the Prague dependency style as a part of HamleDT (since 2011).
Later versions of HamleDT added a conversion to the Stanford dependencies (2014) and to
Universal Dependencies (HamleDT 3.0, 2015). The conversion path from the original Alpino still
goes through the CoNLL-X format and the Prague dependencies, which may occasionally lead to
loss of information. The first release of Universal Dependencies that includes this treebank
is UD v1.2 in November 2015. It is essentially the HamleDT conversion but the data is not
identical to HamleDT 3.0 because the conversion procedure has been further improved.

Alpino and the Dutch CoNLL-X data were released under the GNU GPL license, hence that license
can be used for UD_Dutch as well. However, since GPL is more suitable for programs than for
data (see https://github.com/UniversalDependencies/docs/issues/296 for a discussion), we asked
for and Gertjan van Noord was kind enough to grant the permission to use the Creative Commons
license as an alternative.


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


===============================================================================
ARCHIVE: LICENSE PERMISSION, from Gertjan van Noord, 8 Sep 2016:
Dan,

it is ok to use the CreativeCommons license.

The GPL came about because of the circumstance that the
treebank was/is distributed as part of the Alpino parser distribution.

GJ


On Thu, Sep 08, 2016 at 05:32:32PM +0200, Dan Zeman wrote:
> Dear Gertjan,
>
> I am writing to you regarding the license of the Alpino treebank (or, better, the Dutch treebank in the CoNLL 2006 shared task, which I believe was based on Alpino). We have been playing with this data, converting it first to the Prague style in the HamleDT project (http://ufal.mff.cuni.cz/hamledt), then to Universal Dependencies (http://universaldependencies.org/).
>
> All this happened with the GPL license in mind, which means we also attach the same license to any conversions we create. However, the vast majority of treebanks in UD are under one of the CreativeCommons licenses, and there is now a discussion about how much GPL is actually suitable for data (as opposed to software code). The discussion is here:
>
> https://github.com/UniversalDependencies/docs/issues/296#issuecomment-245569728
>
> Hence I was wondering whether you would mind allowing a CreativeCommons license as an alternative to GPL?
>
> Thanks and all the best,
>
> Dan Zeman