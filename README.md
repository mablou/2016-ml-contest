# 2016-ml-contest

Welcome to the *Geophysical Tutorial* Machine Learning Contest 2016! Read all about the contest in [the October 2016 issue](http://library.seg.org/toc/leedff/35/10) of the magazine. Look for Brendon Hall's tutorial on lithology prediction with machine learning.

**You can run the notebooks in this repo in the cloud, just click the badge below:**

[![Binder](http://mybinder.org/badge.svg)](http://mybinder.org:/repo/seg/2016-ml-contest)

You can also clone or download this repo with the green button above, or just read the documents:

- [index.ipynb](index.ipynb) &mdash; All about the contest.
- [Facies_classification.ipynb](Facies_classification.ipynb) &mdash; Brendon's notebook with all the code you need to get started in machine learning in Python.


## Leaderboard

F1 scores of models against secret blind data in the STUART and CRAWFORD wells. The logs for those wells are available [in the repo](https://github.com/seg/2016-ml-contest/blob/master/validation_data_nofacies.csv), but contestants do not have access to the facies.

|   | Team                                          | F1         | Algorithm     | Language | Solution                 |
|:-:|-----------------------------------------------|:----------:|---------------|----------|--------------------------|
| 1 | geoLEARN                                      | **0.594**  | Random forest | Python | [Notebook](geoLEARN/Submission_3_RF_FE.ipynb) |
| 2 | [bestagini](https://github.com/bestagini)     | **0.581**  | RandomForest  | Python   | [Notebook](ispl/facies_classification_try01.ipynb) |
| 3 | [gccrowther](https://github.com/gccrowther)   | **0.580**  | Random forest | Python   | [Notebook](GCC_FaciesClassification/01%20-%20Facies%20Classification%20-%20GCC-VALIDATION.ipynb) |
| 4 | MandMs                                        | **0.579**  | Majority voting | Python | [Notebook](MandMs/Facies_classification-M%26Ms_plurality_voting_classifier.ipynb) |
| 5 | LA_Team                                       | **0.568**  | Deep neural net | Python   | [Notebook](LA_Team/Facies_classification_LA_TEAM_03.ipynb) |
| 5 | [thanish](https://github.com/thanish)         | **0.568**  | Deep neural net | R        | [Code](Mendacium/Mendacium/NN_sub_1.R) |
| 7 | HouMath                                       | **0.564**  | Boosted trees | Python   | [Notebook](HouMath/Face_classification_HouMath_XGB_02.ipynb) |
| 8 | [gganssle](https://github.com/gganssle)       | **0.561**  | Deep neural net | Lua      | [Notebook](gram/faye.ipynb) |
| 9 | [wouterk1MSS](https://github.com/wouterk1MSS) | **0.557**  | Random forest | Python   | [Notebook](MSS_Xmas_Trees/ml_seg_try1.ipynb) |
| 10| [CEsprey](https://github.com/CEsprey)         | **0.550**  | Majority voting | Python | [Notebook](CEsprey%20-%20RandomForest/Facies_Tree_Ensemble_Classifier.ipynb) |
| 11| [osorensen](https://github.com/osorensen)     | **0.549**  | Boosted trees | R        | [Notebook](boostedXmas/Facies%20Classification.ipynb) |
| 12| [evgenizer](https://github.com/evgenizer)     | **0.546**  | Majority voting | Python   | [Notebook](EvgenyS/Facies_classification_ES.ipynb) |
| 13| Bird Team                                     | **0.527**  | Random forest | Python   | [Notebook](Bird_Team/Facies_classification_3.ipynb) |
| 14 | [CannedGeo](https://github.com/cannedgeo)    | **0.512**  | Support vector machine | Python   | [Notebook](CannedGeo_/Facies_classification-BPage_CannedGeo_F1_56-VALIDATED.ipynb) |
| 15 | [daghra](https://github.com/dagrha)          | **0.506**  | k-nearest neighbours  | Python   | [Notebook](dagrha/KNN_submission_1_dagrha.ipynb) |
| 16 | SHandPR                                      | **0.484**  | Logistic regression | Python   | [Notebook](SHandPR/FaciesTrial.ipynb) |
| 17 | [JesperDramsch](https://github.com/JesperDramsch) | **0.456**  | Support vector machine | Python   | [Notebook](JesperDramsch/Facies_classification_NMM_Split-Jesper.ipynb) |
| 17 | [BrendonHall](https://github.com/brendonhall) | **0.412**  | Support vector machine | Python   | Initial score in article |

<sup>1</sup>&nbsp;Pending complete validation. This usually takes us a few days.


## Getting started with Python

Please refer to the [User guide to the geophysical tutorials](http://library.seg.org/doi/abs/10.1190/tle35020190.1) for tips on getting started in Python and find out more about Jupyter notebooks.


## Find out more about the contest

If you intend to enter this contest, I suggest you check [the open issues](https://github.com/seg/2016-ml-contest/issues) and read through  [the closed issues](https://github.com/seg/2016-ml-contest/issues?q=is%3Aissue+is%3Aclosed) too. There's some good info in there.

To find out more please read the article in [the October issue](http://library.seg.org/toc/leedff/35/10) or read the manuscript in the [`tutorials-2016`](https://github.com/seg/tutorials-2016) repo.


## Rules

We've never done anything like this before, so there's a good chance these rules will become clearer as we go. We aim to be fair at all times, and reserve the right to make judgment calls for dealing with unforeseen circumstances.

**IMPORTANT: When this contest was first published, we asked you to hold the SHANKLE well blind. This is no longer necessary. You can use all the published wells in your training. Related: I am removing the file of predicted facies for the STUART and CRAWFORD wells, to reduce confusion — they are not actual facies, only those predicted by Brendon's first model.**

- You must submit your result as code and we must be able to run your code.
- **Entries will be scored by a comparison against known facies in the STUART and CRAWFORD wells, which do not have labels in the contest dataset. We will use the F1 cross-validation score.** See [issue #2 regarding this point.](https://github.com/seg/2016-ml-contest/issues/2). The scores in the 'leaderboard' reflect this.
- The result we get with your code is the one that counts as your result.
- To make it more likely that we can run it, your code must be written in Python or R or Julia **or Lua** [updated 26 Oct].
- The contest is over at 23:59:59 UT (i.e. midnight in London, UK) on 31 January 2017. Pull requests made aftetr that time won't be eligible for the contest.
- If you can do even better with code you don't wish to share fully, that's really cool, nice work! But you can't enter it for the contest. We invite you to share your result through your blog or other channels... maybe a paper in *The Leading Edge*.
- This document and documents it links to will be the channel for communication of the leading solution and everything else about the contest.
- This document contains the rules. Our decision is final. No purchase necessary. Please exploit artificial intelligence responsibly. 

## Licenses

**Please note that the dataset is not openly licensed. We are working on this, but for now please treat it as proprietary. It is shared here exclusively for use on this problem, in this contest. We hope to have news about this in early 2017, if not before.**

All code is the property of its author and subject to the terms of their choosing. If in doubt — ask them.

The information about the contest, and the original article, and everything in this repo published under the auspices of SEG, is licensed CC-BY and OK to use with attribution.
