# read2tree 

Given a set of reference OGs and sequencing reads this tool allows to automatically build phylogenetic trees of similar quality to a full blown genomics pipeline. 

## Getting Started

read2tree was build and tested with python 3.5.1. To set up read2tree on your local machine.
```
git clone https://github.com/dvdylus/read2tree.git
python setup.py install
```
### Prerequisites

read2tree integrates multiple software tools and allows to infer a phylogenetic tree skipping several steps of a usual pipeline such as assembly, annotation and orthology prediction. It offers a fast alternative to usual tree inference pipelines.

* [mafft](http://mafft.cbrc.jp/alignment/software/) - Mutliple sequence alignment software
* [fasttree](http://www.microbesonline.org/fasttree/) - Dependency Management
* [ngmlr](https://github.com/philres/ngmlr) - Long read mapper for nanopore or PacBio read data
* [ngm](https://github.com/Cibiv/NextGenMap) - Short read mapper for paired end reads
* [pyopa](...) - Implementation of Smith Waterman alignment algorithm in python
* [pyoma](...) - Library for retrieval of nucleotide sequences from oma run
* [pyham](...) - Library to work with HOGs
* [samtools](http://www.htslib.org/download/) - Set of programs to interact with high-throughput sequencing data

### Installing
    
For mafft, fasttree, ngmlr, ngm and samtools please follow the instructions provided by the individual packages.
Make sure that executables are in PATH.

#### CONDA

1. Install [miniconda](https://conda.io/miniconda.html)
2. Setup [bioconda](https://bioconda.github.io/) channels
```
    conda config --add channels defaults
    conda config --add channels conda-forge
    conda config --add channels bioconda
```
3. Install required tools
```
    conda install mafft
    conda install fasttree
    conda install ngmlr
    conda install nextgenmap
    conda install pysam
```
## Running the tests

Once successfully installed you can test the package using:
```
python -W ignore bin/read2tree --standalone_path tests/marker_genes/ --reads ~/Research/read2tree/read2tree/tests/mapper/test3/test_1a.fq ~/Research/read2tree/read2tree/tests/mapper/test3/test_2a.fq  --output_path test/output/

```

## Running 

#### Prerequisites

* Make sure that species names are clearly labeled by a 5 letter code (e.g. Amphiura filiformis = AMPFI)
* Needs either OMA standalone export or OMA marker gene export as reference input
* 


#### Using OMA Standalone RUN

Get couple of reference species from [omabrowser](https://omabrowser.org/oma/export/). Run locally oma standalone as described.

#### Using OMA marker genes

## Running on clusters

### LSF


### SGE

## Built With

* [pyCharm](https://www.jetbrains.com/pycharm) - Python IDE

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **David Dylus** - *Initial work* - [dvddylus](https://github.com/dvdylus)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Alex Warwick for help how to initiate such a package.
__