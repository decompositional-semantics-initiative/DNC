#  Function Word Comprehension

Dataset from [Probing What Different NLP Tasks Teach Machines about Function Word Comprehension](https://www.aclweb.org/anthology/S19-1026) (Kim et al. StarSem 2019).
This directory contains nine challenge tasks that
test for the understanding of function words.

## Structure

As described in the paper, the challenges are formulated either as
acceptability judgment and natural language inference (NLI) tasks.
The challenge sets are in the corresponding `ACCEPTABILITY` & `NLI` directories.

## Acceptability-specific information
Since the acceptability challenges tasks are formulated as single sentence
classification, not all examples' `hypothesis` field are populated. For
these tasks, use the `context` field instead.

Additionally, as described in the paper, 
"<i>we use 10-fold cross validation where each fold is used as the test set exactly once, and report the average test set accuracy</i>." In the acceptability challenge examples' metadata, we include a field called `fold{1...10}` where
the value specifies whether the example is in the train, dev, or test set of that specific fold.


## Bibligoraphy

If you make use of our dataset or the models released here, please cite us using the following citations:

```
@inproceedings{kim-etal-2019-probing,
    title = "Probing What Different {NLP} Tasks Teach Machines about Function Word Comprehension",
    author = "Kim, Najoung  and Patel, Roma  and Poliak, Adam  and Xia, Patrick  and Wang, Alex  and McCoy, Tom  and 
      Tenney, Ian  and Ross, Alexis  and Linzen, Tal  and Van Durme, Benjamin  and Bowman, Samuel R.  and Pavlick, Ellie",
    booktitle = "Proceedings of the Eighth Joint Conference on Lexical and Computational Semantics (*{SEM} 2019)",
    month = jun,
    year = "2019",
    address = "Minneapolis, Minnesota",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/S19-1026",
    pages = "235--249",
}
```
