# References for original datasets

## Factuality

```
@inproceedings{neural-models-of-factuality,
  author    = {Rudinger, Rachel  and  White, Aaron Steven  and  Van Durme, Benjamin},
  title     = {Neural Models of Factuality},
  booktitle = {Proceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long Papers)},
  month     = {June},
  year      = {2018},
  address   = {New Orleans, Louisiana},
  publisher = {Association for Computational Linguistics},
  pages     = {731--744},
  abstract  = {We present two neural models for event factuality prediction, which yield significant performance gains over previous models on three event factuality datasets: FactBank, UW, and MEANTIME. We also present a substantial expansion of the It Happened portion of the Universal Decompositional Semantics dataset, yielding the largest event factuality dataset to date. We report model results on this extended factuality dataset as well.},
  url       = {http://www.aclweb.org/anthology/N18-1067}
}
```


```
@inproceedings{lee2015event,
  title={Event detection and factuality assessment with non-expert supervision},
  author={Lee, Kenton and Artzi, Yoav and Choi, Yejin and Zettlemoyer, Luke},
  booktitle={Proceedings of the 2015 Conference on Empirical Methods in Natural Language Processing},
  pages={1643--1648},
  year={2015}
}
```

```
@inproceedings{minardmeantime,
  title={MEANTIME, the NewsReader Multilingual Event and Time Corpus},
  author={Minard, Anne-Lyse and Speranza, Manuela and Urizar, Ruben and Altuna, Begona and van Erp, Marieke and Schoen, Anneleen and van Son, Chantal},
  year={2016},
  booktitle={Language Resources and Evaluation Conference (LREC)}
}
```

## NER
```
@incollection{bos2017groningen,
  title={The groningen meaning bank},
  author={Bos, Johan and Basile, Valerio and Evang, Kilian and Venhuizen, Noortje J and Bjerva, Johannes},
  booktitle={Handbook of Linguistic Annotation},
  pages={463--496},
  year={2017},
  publisher={Springer}
}
```

```
@inproceedings{TjongKimSang:2003:ICS:1119176.1119195,
 author = {Tjong Kim Sang, Erik F. and De Meulder, Fien},
 title = {Introduction to the CoNLL-2003 Shared Task: Language-independent Named Entity Recognition},
 booktitle = {Proceedings of the Seventh Conference on Natural Language Learning at HLT-NAACL 2003 - Volume 4},
 series = {CONLL '03},
 year = {2003},
 location = {Edmonton, Canada},
 pages = {142--147},
 numpages = {6},
 url = {https://doi.org/10.3115/1119176.1119195},
 doi = {10.3115/1119176.1119195},
 acmid = {1119195},
 publisher = {Association for Computational Linguistics},
 address = {Stroudsburg, PA, USA},
}
```

## Gendered Anaphora

```
@inproceedings{gender-bias-in-coreference-resolution,
  author    = {Rudinger, Rachel  and  Naradowsky, Jason  and  Leonard, Brian  and  Van Durme, Benjamin},
  title     = {Gender Bias in Coreference Resolution},
  booktitle = {Proceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 2 (Short Papers)},
  month     = {June},
  year      = {2018},
  address   = {New Orleans, Louisiana},
  publisher = {Association for Computational Linguistics},
  pages     = {8--14},
  abstract  = {We present an empirical study of gender bias in coreference resolution systems. We first introduce a novel, Winograd schema-style set of minimal pair sentences that differ only by pronoun gender. With these "Winogender schemas," we evaluate and confirm systematic gender bias in three publicly-available coreference resolution systems, and correlate this bias with real-world and textual gender statistics.},
  url       = {http://www.aclweb.org/anthology/N18-2002}
}
```

## Lexicosyntactic Inference

```
@inproceedings{hartshorne2013verbcorner,
  title={The VerbCorner project: Toward an empirically-based semantic decomposition of verbs},
  author={Hartshorne, Joshua K and Bonial, Claire and Palmer, Martha},
  booktitle={Proceedings of the 2013 Conference on Empirical Methods in Natural Language Processing},
  pages={1438--1442},
  year={2013}
}
```

```
@inproceedings{white_role_2018,
        address = {Amherst, MA},
        title = {The role of veridicality and factivity in clause selection},
        booktitle = {Proceedings of the 48th {Annual} {Meeting} of the {North} {East} {Linguistic} {Society}},
        publisher = {GLSA Publications},
        author = {White, Aaron Steven and Rawlins, Kyle},
        year = {2018},
        pages = {to appear}
}
```

```
@article{schuler2005verbnet,
  title={VerbNet: A broad-coverage, comprehensive verb lexicon},
  author={Schuler, Karin Kipper},
  year={2005}
}
```

## Puns

```
@InProceedings{D15-1284,
  author =      "Yang, Diyi
                and Lavie, Alon
                and Dyer, Chris
                and Hovy, Eduard",
  title =       "Humor Recognition and Humor Anchor Extraction",
  booktitle =   "Proceedings of the 2015 Conference on Empirical Methods in Natural      Language Processing    ",
  year =        "2015",
  publisher =   "Association for Computational Linguistics",
  pages =       "2367--2376",
  location =    "Lisbon, Portugal",
  doi =         "10.18653/v1/D15-1284",
  url =         "http://www.aclweb.org/anthology/D15-1284"
}
```

```
@InProceedings{miller-hempelmann-gurevych:2017:SemEval,
  author    = {Miller, Tristan  and  Hempelmann, Christian  and  Gurevych, Iryna},
  title     = {SemEval-2017 Task 7: Detection and Interpretation of English Puns},
  booktitle = {Proceedings of the 11th International Workshop on Semantic Evaluation (SemEval-2017)},
  month     = {August},
  year      = {2017},
  address   = {Vancouver, Canada},
  publisher = {Association for Computational Linguistics},
  pages     = {58--68},
  abstract  = {A pun is a form of wordplay in which a word suggests two or more meanings by
        exploiting polysemy, homonymy, or phonological similarity to another word, for
        an intended humorous or rhetorical effect.  Though a recurrent and expected
        feature in many discourse types, puns stymie traditional approaches to
        computational lexical semantics because they violate their
        one-sense-per-context assumption.  This paper describes the first competitive
        evaluation for the automatic detection, location, and interpretation of puns.
        We describe the motivation for these tasks, the evaluation methods, and the
        manually annotated data set.  Finally, we present an overview and discussion of
        the participating systems' methodologies, resources, and results.},
  url       = {http://www.aclweb.org/anthology/S17-2005}
}
```

## Relationship Extraction

```
@article{gabrilovich2013facc1,
  title={FACC1: Freebase annotation of ClueWeb corpora, Version 1 (Release date 2013-06-26, Format version 1, Correction level 0)},
  author={Gabrilovich, Evgeniy and Ringgaard, Michael and Subramanya, Amarnag},
  journal={Note: http://lemurproject. org/clueweb09/FACC1/Cited by},
  volume={5},
  year={2013}
}
```

## Sentiment Analysis
```
@inproceedings{kotzias2015group,
  title={From group to individual labels using deep features},
  author={Kotzias, Dimitrios and Denil, Misha and De Freitas, Nando and Smyth, Padhraic},
  booktitle={Proceedings of the 21th ACM SIGKDD International Conference on Knowledge Discovery and Data Mining},
  pages={597--606},
  year={2015},
  organization={ACM}
}
```
