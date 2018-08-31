# DNC: <u>*D*</u>iverse <u>*N*</u>atural Language Inference <u>*C*</u>ollection

Dataset associated and released as part of [*Collecting Diverse Natural Language Inference Problems for Sentence Representation Evaluation*](http://www.cs.jhu.edu/~apoliak1/papers/COLLECTING-DIVERSE-NLI-PROBLEMS--EMNLP-2018.pdf) (EMNLP 2018).

## Structure of repo

There are three subdirectories, one for each part of the data split: `train`, `dev`, `test`.

Each subdirectory contains 2 json files for each recast dataset: one data file and one metadata file (except for the recast relation extraction which does not have a metadata file).

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
    
## Contributing to the DNC
We encourage dataset creators to recast
their datasets into NLI and invite them to add
their recast datasets into the DNC. Please add your recast data as a pull request.

If you find any issues in the DNC, please create an issue on this repo. If you fix the issue, please submit a pull request as well. We will make sure to note your contribution to the DNC.

## Bibligoraphy

If you make use of our dataset or the models released here, please cite us using the following citation:

```
@inproceedings{poliak2018emnlp-DNC,
  title = {{Collecting Diverse Natural Language Inference Problems for Sentence Representation Evaluation}},
  author = {Poliak, Adam and Haldar, Aparajita and Rudinger, Rachel and Hu, J. Edward and Pavlick, Ellie and White, Aaron Steven and {Van Durme}, Benjamin},
  booktitle = {Empirical Methods in Natural Language Processing (EMNLP)},
  year = {2018}
}
```

When using specific datasets within the DNC, we ask that you also cite the original dataset that we recast. We include a bibtex entry for each of the original dataset that we recast in [additional_references.md](https://github.com/decompositional-semantics-initiative/DNC/additional_references.md)

## Questions

If you have any questions, comments, or feedback, please email [azpoliak@cs.jhu.edu](mailto:azpoliak@cs.jhu.edu) 
