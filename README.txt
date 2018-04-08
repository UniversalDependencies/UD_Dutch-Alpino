# Summary

This corpus consists of samples from various treebanks annotated at the University of Groningen using the Alpino annotation tools and guidelines.

# Introduction

The data consists of samples from various treebanks annotated at the University of Groningen using the Alpino annotation tools and guidelines:

 * train consists of material from the original Alpino CD-ROM (file id 'cdb' 7000+ sentences from the Eindhoven corpus), questions using in a QA project (file ids with qa and wpspel), material from suites used for grammar maintenance (id: g_suite, h_suite, leuven_yellow_pages), example sentence from the Dutch reference grammar ANS (eans), and the WR-P-P-H section of the Lassy Small corpus
 * dev consists of material from the WR-P-P-H section of the Lassy Small corpus
 * test consists of material from the WR-P-P-H and WR-P-P-L sections of the Lassy Small corpus

The data was thoroughly revised by Gosse Bouma and Gertjan van Noord for UD 2.1 in November 2017.
The new version was created using the same conversion script as was used for Dutch LassySmall.
As sources, we used the (manually corrected) Alpino treebank annotation for this material as it is
available in Groningen. Links to original files have been added. Note that tokenization may differ
from the previous UD version.

The conversion script can be found here: https://github.com/gossebouma/lassy2ud

# Acknowledgements

# Older

Description of the material as it was included in UD 1.0 and 2.0:

The data were used in the CoNLL-X Shared Task in dependency parsing (2006); the CoNLL version
was taken and converted to the Prague dependency style as a part of HamleDT (since 2011).
Later versions of HamleDT added a conversion to the Stanford dependencies (2014) and to
Universal Dependencies (HamleDT 3.0, 2015). The conversion path from the original Alpino still
goes through the CoNLL-X format and the Prague dependencies, which may occasionally lead to
loss of information. The first release of Universal Dependencies that included this treebank
was UD v1.2 in November 2015. It was essentially the HamleDT conversion but the data was not
identical to HamleDT 3.0 because the conversion procedure had been further improved.


# References:

* http://odur.let.rug.nl/~vannoord/trees/
* http://ufal.mff.cuni.cz/hamledt ... HamleDT
* http://ufal.mff.cuni.cz/treex ... Treex is the software used for conversion
* http://ufal.mff.cuni.cz/interset ... Interset was used to convert POS tags and features

* Gosse Bouma and Gertjan van Noord Increasing Return on annotation investment: the automatic construction of a Universal Dependency treebank for Dutch in: Proceedings of the Universal Dependencies Workshop, Gothenburg, 22 May 2017
http://aclweb.org/anthology/W17-0403
* van Noord G. et al. (2013) Large Scale Syntactic Annotation of Written Dutch: Lassy. In: Spyns P., Odijk J. (eds) Essential Speech and Language Technology for Dutch. Theory and Applications of Natural Language Processing. Springer, Berlin, Heidelberg https://doi.org/10.1007/978-3-642-30910-6_9
* L. van der Beek, G. Bouma, R. Malouf, and G. van Noord. The alpino dependency treebank. In Computational Linguistics in the Netherlands (CLIN) 2001, Twente University, 2002. http://www.let.rug.nl/~gosse/papers/clin01c.pdf



# Changelog

* 2018-04-15 v2.2
  * Repository renamed from UD_Dutch to UD_Dutch-Alpino.
* 2017-11-15 v2.1
  * First version of thorougly revised data.
    It was created using the same conversion script as is being used for Dutch
    LassySmall. As sources, we used the (manually corrected) Alpino treebank
    annotation for this material as it is available in Groningen. Links to
    original files have been added. Issues:
    * tokenization may differ from the previous version.
    * some sentences are missing in the Alpino treebanks. In those cases UD 2.0
      annotation has been preserved.
* 2017-03-01 v2.0
  * Converted to UD v2 guidelines.
  * Reconsidered PRON vs. DET.
  * Changed advmod vs. obl distinction. This is a result of a general rule for
    the Prague deprel 'Adv'. However, we should extend it by a Dutch-specific
    rule for adjectives, which often act like adverbs and definitely not like
    obliques.
* 2016-05-15 v1.3
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



<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v1.2
License: CC BY-SA 4.0
Includes text: yes
Genre: news
Lemmas: converted from manual
UPOS: converted from manual
XPOS: manual native
Features: converted from manual
Relations: converted from manual
Contributors: Zeman, Daniel; Žabokrtský, Zdeněk; Bouma, Gosse; van Noord, Gertjan
Contributing: elsewhere
Contact: g.bouma@rug.nl
Paragraphs to web: 5
===============================================================================
</pre>
