# DNC: <u>*D*</u>iverse <u>*N*</u>atural Language Inference <u>*C*</u>ollection

Dataset associated and released as part of [*Collecting Diverse Natural Language Inference Problems for Sentence Representation Evaluation*](http://www.cs.jhu.edu/~apoliak1/papers/COLLECTING-DIVERSE-NLI-PROBLEMS--EMNLP-2018.pdf) (EMNLP 2018).

## Structure of repo

There are three subdirectories, one for each part of the data split: `train`, `dev`, `test`.

Each subdirectory contains 2 json files for each recast dataset: one data file and one metadata file (except for the recast relation extraction which does not have a metadata file).

The directory [function_words](https://github.com/decompositional-semantics-initiative/DNC/tree/master/function_words) contains the data associated and released as part of [*Probing What Different NLP Tasks Teach Machines about Function Word Comprehension*](https://www.aclweb.org/anthology/S19-1026) (Kim et al. StarSem 2019).

## Structure of json files:

#### Data files:
Each datafile has the following keys and values:

- `context`: The context sentence for the NLI pair. The context is already tokenized.
- `hypothesis`: The hypothesis sentence for the NLI pair. The hypothesis is already tokenized.
- `label`: The label for the NLI pair
- `label-set`: The set of possible labels for the specific NLI pair
- `binary-label`: A `True` or `False` label. See the paper for details on how we convert the `label` into a binary label.
- `split`: This can be `train`, `dev`, or `test`.
- `type-of-inference`: A string indicating what type of inference is tested in this example.
- `pair-id`: A unique integer id for the NLI pair. The `pair-id` is used to find the corresponding metadata for any given NLI pair

#### Metadata files:

- `pair-id`: A unique integer id for the NLI pair. 
- `corpus`: The original corpus where this example came from.
- `corpus-sent-id`: The id of the sentence (or example) in the original dataset that we recast.
- `corpus-license`: The license for the data from the original dataset.
- `creation-approach`: Determines the method used to recast this example. Options are `automatic`, `manual`, or `human-labeled`.
- `misc`: A dictionary of other relevant information. This is an optional field.

## Notes:

1. The training data for recast NER is split into 2 files since we cannot upload files larger than 100MB to GitHub.
2. Recast `kg_relations` does not have a metadata file:
    1. The data file for that recast dataset includes another key called `annotations` that contains the original multi-way annotations. 

## Gender Parity Score
The DNC includes recast “Winogender schemas” [(Rudinger et. al. NAACL 2018)](https://www.aclweb.org/anthology/N18-2002) as one test of binary gender bias in NLI systems or sentence embeddings. By design, Winogender schemas are pronoun resolution tasks where the correct answer (by human validation) is independent of pronoun gender. Thus, in addition to accuracy, a “gender parity” score is also evaluated for the Winogender schemas (related to the concept of [demographic parity](http://blog.mrtz.org/2016/09/06/approaching-fairness.html), from the ML fairness literature). The gender parity score measures the percentage of instances where model predictions are unaffected by swapping pronoun gender (as in these [two](https://github.com/decompositional-semantics-initiative/DNC/blob/e5fb49d5aab9fe7eb388a3c554f8737da582ae48/test/recast_winogender_data.json#L15-L27) [examples](https://github.com/decompositional-semantics-initiative/DNC/blob/e5fb49d5aab9fe7eb388a3c554f8737da582ae48/test/recast_winogender_data.json#L41-L53)). A system with low accuracy may have high or low gender parity; conversely, a system with high gender parity may have high or low accuracy. Thus, both metrics are computed to capture this (potential) trade-off.

### Computing Gender Parity Score
We provide a [python script](https://github.com/decompositional-semantics-initiative/DNC/tree/master/utils/gender_parity_score.py) that computes the score. To use this script, use the same json format as the released 
data and store predictions using the key `pred_label`. 
    
## Contributing to the DNC
We encourage dataset creators to recast
their datasets into NLI and invite them to add
their recast datasets into the DNC. Please add your recast data as a pull request.
We hope that this can lead to collaborations! 

If you find any issues in the DNC, please create an issue on this repo. If you fix the issue, please submit a pull request as well. We will make sure to note your contribution to the DNC.

## Previous Recast datasets
[White et. al. (2017)](http://www.aclweb.org/anthology/I17-1100) previously recast 3 datasets into NLI when they proposed to unify semantic classification tasks under the heading of NLI. Our repo includes their recast datasets and can be downloaded [here](https://github.com/decompositional-semantics-initiative/DNC/raw/master/inference_is_everything.zip).


## Bibligoraphy

If you make use of our dataset or the models released here, please cite us using the following citations:

```
@inproceedings{poliak2018emnlp-DNC,
  title = {{Collecting Diverse Natural Language Inference Problems for Sentence Representation Evaluation}},
  author = {Poliak, Adam and Haldar, Aparajita and Rudinger, Rachel and Hu, J. Edward and Pavlick, Ellie and White, Aaron Steven and {Van Durme}, Benjamin},
  booktitle = {Empirical Methods in Natural Language Processing (EMNLP)},
  year = {2018}
}

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

When using specific datasets within the DNC, we ask that you also cite the original dataset that we recast. We include a bibtex entry for each of the original dataset that we recast in [additional_references.md](https://github.com/decompositional-semantics-initiative/DNC/blob/master/additional_references.md)

## Questions

If you have any questions, comments, or feedback, please email [azpoliak@cs.jhu.edu](mailto:azpoliak@cs.jhu.edu) 
