**Contents of this data release**:

        .
        ├── data/
        ├── ent2count-sorted.txt
        ├── etype2count-sorted.txt
        ├── fex-dev-fnames.txt
        ├── fex-test-fnames.txt
        ├── ner-dev-fnames.txt
        ├── ner-test-fnames.txt
        ├── ner-train-fnames.txt
        ├── README.md
        ├── sentcount2papercount-sorted.txt
        ├── sentlen2sentcount-sorted.txt
        └── tok2count-sorted.txt


**Description of contents**:

*Data Description:*

`data/`: Raw annotations created with the [BRAT annotation tool][1]. Every annotated
paper contains a .ann and a .txt file. The .ann file contains, entity and 
relation annotations. The .txt file contains 3 lines, the doi of the paper, the
title of the paper and the synthesis-procedure text of the paper. This directory
contains annotations for 230 papers. The annotations are in the [BRAT Standoff
format][2].

`fex-{dev/test}-fnames.txt`: The files in the "data/" subdirectory corresponding
to the dev and test splits for the frame extraction (fex) task. Since the task
is primarily trained on unlabelled data we only release test and development 
data.

`ner-{dev/test/train}-fnames.txt`: The files in the "data/" subdirectory 
corresponding to the dev, test and train files for the named entity extraction
(ner) task.

*Dataset statistics:*

`ent2count-sorted.txt`: The entities labelled in the data vs the number of 
times these entities were labelled.

`etype2count-sorted.txt`: The entity types labelled vs the number of 
times these entity types were labelled.

`sentcount2papercount-sorted.txt`: The number of sentences that in a given 
synthesis procedure vs the number of papers with the said number of sentences.
Sentence segmentation was performed automatically with the [ChemDataExtractor][3]
python package.

`sentlen2sentcount-sorted.txt`: The number of tokens in a sentence vs the number
of sentences with the said number of tokens. Sentence tokenization was performed
automatically with the ChemDataExtractor tool.

`tok2count-sorted.txt`: The tokens vs the number of times the tokens occur in 
the dataset. Sentence tokenization was performed automatically with the 
ChemDataExtractor tool.

`README.md`: This file.

**License**
TODO post acceptence.

**Contact**
edwardk@mit.edu, smysore@cs.umass.edu


[1]: http://brat.nlplab.org/index.html
[2]: http://brat.nlplab.org/standoff.html
[3]: https://pypi.org/project/ChemDataExtractor/1.2.2/
