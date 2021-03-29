# NER Benchmarks



Data \ Entity type | Location | Person | Organization | Misc | Disease | Overall
--- | --- |--- | --- | --- | --- | ---
**Stanford NER** | | | | | |
CONLL 2003 pre-trained | 90 | 95 | 86 | 80 | |
CONLL 2003 custom-trained | 99 | 99 | 99 | 99 | |
SEC-Filings pre-trained | 40 | 29.7 | 26.1 | 4.3 | |
SEC-Filings custom-trained | 39 | 90 | 25.2 | 0 | |
NCBI-Disease | | | |  | |
 **Flair NER**|  | | | | |
CONLL 2003 pre-trained |  |  |  |  | |
CONLL 2003 custom-trained | 92.7 | 95.9 | 88.6 | 83 | | 91.2
SEC-Filings pre-trained |  |  |  |  | |
SEC-Filings custom-trained | 58.4 | 95 | 50.9 | 44.4 | | 81.5
NCBI-Disease | | | |  | 88.6 |
 **Allen NLP**|  | | | | |
CONLL 2003 pre-trained |  |  |  |  | |
CONLL 2003 custom-trained | 79 | 75 | 35 | 67 | |  65
SEC-Filings pre-trained |  |  |  |  | |
SEC-Filings custom-trained |  |  |  |  | |
NCBI-Disease | | | |  |  |
 **Spacy NLP**|  | | | | |
CONLL 2003 pre-trained |  |  |  |  | | 7.6
CONLL 2003 custom-trained |  |  |  |  | | 81.6
SEC-Filings pre-trained |  |  |  |  | | 3.4
SEC-Filings custom-trained |  |  |  |  | | 12.7
NCBI-Disease | | | |  |  |



FROM https://paperswithcode.com/task/named-entity-recognition-ner

FROM https://lionbridge.ai/datasets/15-free-datasets-and-corpora-for-named-entity-recognition-ner/

|DATASET|BEST METHOD|PAPER TITLE| License |links|Number of Documents|Entity types| Domain | Language |
| ------------- |:------------------:| -----:| -----:| -----:| -----:| -----:|-----:| -----:|
|CoNLL 2003 (English) | LUKE | LUKE: Deep Contextualized Entity Representations with Entity-aware Self-attention|open| wget https://data.deepai.org/conll2003.zip|||news|English|
|Ontonotes v5 (English)|BERT-MRC+DSC|Dice Loss for Data-imbalanced NLP Tasks|register, non free| https://catalog.ldc.upenn.edu/LDC2013T19|>1M||News BN BC Web Tele Pivot|English|
|ACE 2005|BERT-MRC|A Unified MRC Framework for Named Entity Recognition|register, non free| https://catalog.ldc.upenn.edu/LDC2006T06|>1M|Text|	weblogs, broadcast news, newsgroups, broadcast conversation|Mandarin Chinese, Standard Arabic, English|
|GENIA|Biaffine-NER|Named Entity Recognition as Dependency Parsing|free|wget http://www.nactem.ac.uk/GENIA/tagger/geniatagger-3.0.2.tar.gz https://files.ifi.uzh.ch/cl/kalju/download/depgenia/v1/|2000|||English|
|ACE 2004|Biaffine-NER|Named Entity Recognition as Dependency Parsing|register, non free| https://catalog.ldc.upenn.edu/LDC2005T09||Text|newswire, broadcast news, telephone conversations|English, Standard Arabic, Mandarin Chinese|
|CoNLL++|CrossWeigh + Pooled Flair|CrossWeigh: Training Named Entity Tagger from Imperfect Annotations|free|git clone https://github.com/pfliu-nlp/Named-Entity-Recognition-NER-Papers/tree/master/ner_dataset/CoNLL++|||news|English|
|Long-tail emerging entities|Flair embeddings|Contextual String Embeddings for Sequence Labeling|?|https://paperswithcode.com/sota/named-entity-recognition-ner-on-long-tail|
|BC5CDR|NER+PA+RL (PubMed)|Reinforcement-based denoising of distantly supervised NER with partial annotation|free, but register| https://biocreative.bioinformatics.udel.edu/tasks/biocreative-v/track-3-cdr/|||Chemicals, diseases, and their relations||
|JNLPBA|BLSTM-CNN-Char (SparkNLP)|Biomedical Named Entity Recognition at Scale|free|git clone https://github.com/openbiocorpora/jnlpba||||German|
|CoNLL 2003 (German)|ACE + document-context|Automated Concatenation of Embeddings for Structured Prediction|free|wget https://www.clips.uantwerpen.be/conll2003/deu.raw.tar git clone https://github.com/huggingface/datasets/tree/master/datasets/conll2003||||German|
|CoNLL 2002 (Spanish)|ACE + document-context|Automated Concatenation of Embeddings for Structured Prediction|free|https://www.clips.uantwerpen.be/conll2002/ner/ git clone https://github.com/huggingface/datasets/tree/master/datasets/conll2002|||news|Spanish|
|CoNLL 2002 (Dutch)|ACE + document-context|Automated Concatenation of Embeddings for Structured Prediction|free|https://www.clips.uantwerpen.be/conll2002/ner/ git clone https://github.com/huggingface/datasets/tree/master/datasets/conll2002|||news|Dutch|
|NCBI-disease|BioBERT|BioBERT: a pre-trained biomedical language representation model for biomedical text mining|free|https://www.ncbi.nlm.nih.gov/CBBresearch/Dogan/DISEASE/|793|disease||English|
|SciERC|SpERT|Span-based Joint Entity and Relation Extraction with Transformer Pre-training|free|http://nlp.cs.washington.edu/sciIE/|500|||Spanish|
|CoNLL 2003 (German) Revised|ACE|Automated Concatenation of Embeddings for Structured Prediction|free|wget https://www.clips.uantwerpen.be/conll2003/deu.raw.tar|||news|German|
|WLPC|DyGIE|A General Framework for Information Extraction using Dynamic Span Graphs|free|https://github.com/chaitanya2334/WLP-Dataset|622|||English|
|WetLab|BiLSTM-CRF with ELMo|Using Similarity Measures to Select Pretraining Data for NER|free|https://paperswithcode.com/sota/named-entity-recognition-ner-on-wetlab||||English|
|Species-800|BioFLAIR|BioFLAIR: Pretrained Pooled Contextualized Embeddings for Biomedical Sequence Labeling Tasks|free|git clone https://github.com/huggingface/datasets/tree/master/datasets/species_800|1K<n<10K|||English|
|LINNAEUS|BLSTM-CNN-Char (SparkNLP)|Biomedical Named Entity Recognition at Scale|free|git clone https://github.com/huggingface/datasets/tree/master/datasets/linnaeus|10K<n<100K|||English|
|Code-Switching English-Spanish NER|HME (word + BPE + char)|Hierarchical Meta-Embeddings for Code-Switching Named Entity Recognition|?|https://competitions.codalab.org/competitions/18725#phases||||English-Spanish|
|ontontoes chinese v5|DGLSTM-CRF|Dependency-Guided LSTM-CRF for Named Entity Recognition|?|https://paperswithcode.com/sota/named-entity-recognition-on-ontontoes-chinese||||Chinese|
|CoNLL 2000|SWEM-CRF|Baseline Needs More Love: On Simple Word-Embedding-Based Models and Associated Pooling Mechanisms|free|git clone https://github.com/huggingface/datasets/tree/master/datasets/conll2000|10k||news|English|
|French Treebank|CamemBERT (subword masking)|CamemBERT: a Tasty French Language Model|free|git clone https://github.com/nicolashernandez/free-french-treebank|87461 sentences and 2535396|||French|
|SoSciSoCi|Bi-LSTM-CRF (SSC->GSC)|Investigating Software Usage in the Social Sciences: A Knowledge Graph Approach|free|git clone https://github.com/dave-s477/SoSciSoCi-SSC|over 50.000|||English|
|LeNER-Br|LSTM-CRF|LeNER-Br: a Dataset for Named Entity Recognition in Brazilian Legal Text|free|git clone https://github.com/huggingface/datasets/tree/master/datasets/lener_br|10k|||Brazilian|
|Annotated Corpus for Named Entity Recognition|||open database|https://www.kaggle.com/abhinavwalia95/entity-annotated-corpus?select=ner.csv|1.3 mln words |geo,org,time,eve,per| | English |
|Enron Emails|||open|http://www.cs.cmu.edu/~enron/|500000 messages|names,dates,times||English|
|MIT Movie Corpus|||open|https://groups.csail.mit.edu/sls/downloads/movie/|||movies|English|
|MIT Restaurant Corpus|||open|https://groups.csail.mit.edu/sls/downloads/restaurant/|||restaurant|English|
|Annotated GMB Corpus|||open|https://www.kaggle.com/shoumikgoswami/annotated-gmb-corpus/home?select=GMB_dataset.txt|66k words|geo,org,per,eve||English|
|Emerging Entities dataset|||open|https://github.com/leondz/emerging_entities_17||person,location,group,corp,product||English|
|Europeana Newspapers|||open|https://github.com/EuropeanaNewspapers/ner-corpora||per,loc,org|news |dutch,french,german|
|Swedish NER corpus	|||open|https://www.kaggle.com/andreasklintberg/swedish-ner-corpus|8000 sentences|PER, LOC, ORG, MISC|news |swedish|
