<!-- ABOUT THE PROJECT -->
## About The Project
ChEmbed v0.1 - is a [sentence-transformers](https://www.SBERT.net) based on [MiniLM-L6-H384-uncased](https://huggingface.co/nreimers/MiniLM-L6-H384-uncased) fine-tuned on around 1 million pairs of valid natural compounds' SELFIES [(Krenn et al. 2020)](https://github.com/aspuru-guzik-group/selfies) taken from COCONUTDB [(Sorokina et al. 2021)](https://coconut.naturalproducts.net/). It maps compounds' *Self-Referencing Embedded Strings* (SELFIES) into a 768-dimensional dense vector space, potentially can be used for similarity search, classification, clustering, and more.

Here, we will use the above model to embed ~407K natural product molecular SELFIES representations (from [COCONUTDB](https://coconut.naturalproducts.net/)) and utilize [Meta's FAISS](https://github.com/facebookresearch/faiss) for indexing and doing fast searches for structurally similar compounds based on one or more inputs.

[![How This WOrks][aboutposter]](https://example.com)

### Disclaimer: For Academic Purposes Only
The information and model provided is for academic purposes only. It is intended for educational and research use, and should not be used for any commercial or legal purposes. The author do not guarantee the accuracy, completeness, or reliability of the information.

<!-- GETTING STARTED -->
## Getting Started
Please clone/download this repo and extract the archives provided then,
see [Demo.ipynb](./Demo.ipynb) for tutorial on:
- Part I: Importing and Loading Model
- Part II: Preparing the Dataset and its FAISS-Index (You can skip Part II for direct use)
- Part III: Querying One Molecule as Input
- Part IV: Querying Multiple Molecule and using Averaged Embedding

### Prerequisites
```
sentence_transformers, pandas, rdkit, tqdm, selfies, numpy, scikit-learn, faiss, pyarrow, matplotlib, pickle
```

### Data Attribution

#### COCONUTDB
```bibtex
@article{sorokina2021coconut,
  title={COCONUT online: Collection of Open Natural Products database},
  author={Sorokina, Maria and Merseburger, Peter and Rajan, Kohulan and Yirik, Mehmet Aziz and Steinbeck, Christoph},
  journal={Journal of Cheminformatics},
  volume={13},
  number={1},
  pages={2},
  year={2021},
  doi={10.1186/s13321-020-00478-9}
}
```

<!-- LICENSE -->
## License
Creative Commons Attribution Share Alike 3.0

<!-- CONTACT -->
## Contact
GP Bayu - HF:[@gbyuvd](https://huggingface.co/gbyuvd) - e-mail:gbyuvd@proton.me

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/O4O710GFBZ)

<!-- ACKNOWLEDGMENTS -->
## Acknowledgments
- Thanks to [othneildrew](https://github.com/othneildrew/Best-README-Template/) for the README template.
- Thanks to HF:[@nreimers](huggingface.co/nreimers) for the base [MiniLM-L6-H384-uncased](https://huggingface.co/nreimers/MiniLM-L6-H384-uncased) model.
- For more information on SELFIES, you could read this [blogpost](https://aspuru.substack.com/p/molecular-graph-representations-and) or check out [their github.](https://github.com/aspuru-guzik-group/selfies)

<!-- Citations -->
## Citations
If you find this project useful in your research and wish to cite it, please use the following BibTex entries:

#### ChEmbed-v0.1
```bibtex
@software{chembed_selfies01,
  author = {GP Bayu},
  title = {{ChEmbed}: Fine-tuning A Lightweight Sentence Transformer Model on Molecular SELFIES},
  url = {https://huggingface.co/gbyuvd/ChemEmbed-v01},
  version = {0.1},
  year = {2024},
}
```

#### Sentence Transformers
```bibtex
@inproceedings{reimers-2019-sentence-bert,
    title = "Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks",
    author = "Reimers, Nils and Gurevych, Iryna",
    booktitle = "Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing",
    month = "11",
    year = "2019",
    publisher = "Association for Computational Linguistics",
    url = "https://arxiv.org/abs/1908.10084",
}
```

#### COCONUTDB
```bibtex
@article{sorokina2021coconut,
  title={COCONUT online: Collection of Open Natural Products database},
  author={Sorokina, Maria and Merseburger, Peter and Rajan, Kohulan and Yirik, Mehmet Aziz and Steinbeck, Christoph},
  journal={Journal of Cheminformatics},
  volume={13},
  number={1},
  pages={2},
  year={2021},
  doi={10.1186/s13321-020-00478-9}
}
```

#### SELFIES
```bibtex
@article{krenn2020selfies,
  title={Self-referencing embedded strings (SELFIES): A 100\% robust molecular string representation},
  author={Krenn, Mario and H{\"a}se, Florian and Nigam, AkshatKumar and Friederich, Pascal and Aspuru-Guzik, Alan},
  journal={Machine Learning: Science and Technology},
  volume={1},
  number={4},
  pages={045024},
  year={2020},
  doi={10.1088/2632-2153/aba947}
}
```
#### FAISS
```bibtex
@article{douze2024faiss,
      title={The Faiss library},
      author={Matthijs Douze and Alexandr Guzhva and Chengqi Deng and Jeff Johnson and Gergely Szilvasy and Pierre-Emmanuel Mazaré and Maria Lomeli and Lucas Hosseini and Hervé Jégou},
      year={2024},
      eprint={2401.08281},
      archivePrefix={arXiv},
      primaryClass={cs.LG}
}
```


[aboutposter]: images/aboutposter.png


