This is the Chicago Rhyming Poetry Corpus, consisting of annotated poetry in English and French.

Much of the English data was collected and annotated by Morgan Sonderegger (morgan@cs.uchicago.edu). The English data was expanded and edited, and the French data added, by Sravana Reddy (sravana@cs.uchicago.edu).

This directory contains raw data files with annotations (english_raw and french_raw), as well as files containing only stanza end-words, which is what is used by our code for training and evaluation (english_gold and french_gold). 

All poetry in the corpus is in the public domain and freely available electronically. 

*Description of raw txt files:*

Each file contains a collection of poems by a single poet. For example, here is an extract from wyatt.txt:

AUTHOR Thomas Wyatt  <= Name of poet.

TITLE Satire II  <= Title of poem that follows.

RHYME-POEM a b a
RHYME a b a 

MY mother's maids, when they did sew and spin,
They sang sometime a song of the field mouse
That, for because her livelihood was but thin,

RHYME-POEM b c b <= If relevant, scheme in the context of the whole poem (here, this stanza shares rhymes with the previous stanza). If there is no rhyme sharing, this field is omitted.
RHYME a b a <= Rhyme scheme of the stanza independent of others in the poem. 

Would needs go seek her townish sister's house.
She thought herself endured too much pain;
The stormy blasts her cave so sore did souse
...

TITLE A Love Song <= Title of next poem. Also denotes the ending of the above poem.

Sometimes, we use a shorthand for the rhyme scheme, like 

RHYME a a *

This denotes the rhyme scheme aabbccdd...

*Description of gold files:*

These are derived from the raw data by extracting only the end-words of each stanza.  The file corresponding to Wyatt looks like this:

POEM0 spin mouse thin  <= Indicates the id of the poem that the stanza belongs to, and a list of the end-words.
1 2 1  <= Rhyme scheme of stanza
1 2 1

POEM0 house pain souse
1 2 1   
2 3 2    <= Rhyme scheme in context of poem (indicating that 1st word rhymes with 2nd word in previous stanza)

This corpus is under development; we hope to expand it to cover more texts and languages. Please e-mail sravana@cs.uchicago.edu if you would like to contribute, or if you find an error in the annotations.
