# AMS 4.0: consensus prediction of post-translational modifications in protein sequences #

#### Dariusz Plewczynski ####
Interdisciplinary Centre for Mathematical and Computational Modeling, University of Warsaw, 02-106 Warsaw, Poland, Email: darman AT icm.edu.pl

#### Subhadip Basu ####
Department of Computer Science and Engineering, Jadavpur University, Kolkata – 700032, India, Email: subhadip AT cse.jdvu.ac.in

#### Indrajit Saha ####
Interdisciplinary Centre for Mathematical and Computational Modeling, University of Warsaw, 02-106 Warsaw, Poland, Email: darman AT icm.edu.pl


## Abstract ##
We present here the 2011 update of the AutoMotif Service (AMS 4.0) that predicts the wide selection of 88 different types of the single amino acid post-translational modifications (PTM) in protein sequences. The selection of experimentally confirmed modifications is acquired from the latest UniProt and Phospho.ELM databases for training. The sequence vicinity of each modified residue is represented using amino acids physico-chemical features encoded using high quality indices (HQI) obtaining by automatic clustering of known indices extracted from AAindex database. For each type of the numerical representation, the method builds the ensemble of Multi-Layer Perceptron (MLP) pattern classifiers, each optimising different objectives during the training (for example the recall, precision or area under the ROC curve (AUC)). The consensus is built using brainstorming technology, which combines multi-objective instances of machine learning algorithm, and the data fusion of different training objects representations, in order to boost the overall prediction accuracy of conserved short sequence motifs. The performance of AMS 4.0 is compared with the accuracy of previous versions, which were constructed using single machine learning methods (artificial neural networks, support vector machine). Our software improves the average AUC score of the earlier version by close to 7 % as calculated on the test datasets of all 88 PTM types. Moreover, for the selected most-difficult sequence motifs types it is able to improve the prediction performance by almost 32 %, when compared with previously used single machine learning methods. Summarising, the brainstorming consensus meta-learning methodology on the average boosts the AUC score up to around 89 %, averaged over all 88 PTM types. Detailed results for single machine learning methods and the consensus methodology are also provided, together with the comparison to previously published methods and state-of-the-art software tools. The source code and precompiled binaries of brainstorming tool are available at http://code.google.com/p/automotifserver/ under Apache 2.0 licensing.

## Availability ##

[The PTM database and the software are available here](https://code.google.com/p/automotifserver/downloads/list)

[Pubmed link](http://www.ncbi.nlm.nih.gov/pubmed/22555647)

**Citation:**
Plewczynski, Dariusz, Subhadip Basu, and Indrajit Saha. "AMS 4.0: consensus prediction of post-translational modifications in protein sequences." Amino acids 43, no. 2 (2012): 573-582.



---


# AMS 3.0: Prediction of Post-Translational Modifications #

#### Subhadip Basu ####
Department of Computer Science and Engineering, Jadavpur University, Kolkata – 700032, India, Email: subhadip AT cse.jdvu.ac.in

#### Dariusz Plewczynski ####
Interdisciplinary Centre for Mathematical and Computational Modeling, University of Warsaw, 02-106 Warsaw, Poland, Email: darman AT icm.edu.pl


## Abstract ##
#### BACKGROUND: ####
We present here the recent update of AMS algorithm for identification of post-translational modification (PTM) sites in proteins based only on sequence information, using artificial neural network (ANN) method. The query protein sequence is dissected into overlapping short sequence segments. Ten different physicochemical features describe each amino acid; therefore nine residues long segment is represented as a point in a 90 dimensional space. The database of sequence segments with confirmed by experiments post-translational modification sites are used for training a set of ANNs.
#### RESULTS: ####
The efficiency of the classification for each type of modification and the prediction power of the method is estimated here using recall (sensitivity), precision values, the area under receiver operating characteristic (ROC) curves and leave-one-out tests (LOOCV). The significant differences in the performance for differently optimized neural networks are observed, yet the AMS 3.0 tool integrates those heterogeneous classification schemes into the single consensus scheme, and it is able to boost the precision and recall values independent of a PTM type in comparison with the currently available state-of-the art methods.
#### CONCLUSIONS: ####
The standalone version of AMS 3.0 presents an efficient way to identify post-translational modifications for whole proteomes. The training datasets, precompiled binaries for AMS 3.0 tool and the source code are available at http://code.google.com/p/automotifserver under the Apache 2.0 license scheme.

## Availability ##

The processed training PTM database of the software are available at http://bio.icm.edu.pl/~darman/ams3/

AMS-3 Web server is available at http://ams3.bioinfo.pl

[Pubmed link](http://www.ncbi.nlm.nih.gov/pubmed/20423529)

**Citation:**
Basu, Subhadip, and Dariusz Plewczynski. "AMS 3.0: prediction of post-translational modifications." BMC bioinformatics 11, no. 1 (2010): 210.



---

### Acknowledgement ###
This work was supported by EC BioSapiens (LHSG-CT-2003-503265), and OxyGreen (KBBE-2007-212281) 6FP projects as well as the Polish Ministry of Education and Science (N301 159735, PBZ-MNiI-2/1/2005 and others). Authors are also indebted to the contributions of the Centre for Microprocessor Applications for Training Education and Research (CMATER), Computer Science and Engineering Department, Jadavpur University, India, for providing necessary infrastructural facilities during the progress of the work. Authors also acknowledge the contributions of many students, researchers and colleagues of CMATER in developing several key modules of the training and prediction routines, now made available in public domain.