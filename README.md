# DeepTCR

## Deep Learning Methods for Parsing T-Cell Receptor Sequencing (TCRSeq) Data

DeepTCR is a python package that has a collection of unsupervised and supervised 
deep learning methods to parse TCRSeq data. To see examples of how the algorithms can 
be used on an example datasets, see the subdirectory 'tutorials' for a collection of tutorial 
use cases across multiple datasets. For complete documentation for all available methods,
see 'Documentation.txt' .

While DeepTCR will run with Tensorflow-CPU versions, for optimal training times, 
we suggest training these algorithms on GPU's (requiring CUDA, cuDNN, and tensorflow-GPU). 

DeepTCR now has the added functionality of being able to analyze paired alpha/beta chain inputs as well
as also being able to take in v/d/j gene usage and the contextual HLA information the TCR-Sequences
were seen in (i.e. HLA alleles for a repertoire from a given human sample). For detailed instructions on 
how to upload this type of data, refer to the documentation for loading data into DeepTCR.  

For questions or help, email: jsidhom1@jhmi.edu

## Publication

For full description of algorithm and methods behind DeepTCR, refer to the following manuscript:

Sidhom, J. W., Larman, H. B., Pardoll, D. M., & Baras, A. S. (2018). DeepTCR: a deep learning framework for revealing structural concepts within TCR Repertoire. bioRxiv, 464107.

https://www.biorxiv.org/content/10.1101/464107v4

## Dependencies

See requirements.txt for all DeepTCR dependencies. Installing DeepTCR from Github repository or PyPi will install all required dependencies.
It is recommended to create a virtualenv and installing DeepTCR within this environment to ensure proper versioning of dependencies.
Of note, DeepTCR is not compatible with tensorflow 2.0 at this time.

## Installation

In order to install DeepTCR:

```python
pip3 install DeepTCR

```

Or to install latest updated versions from Github repo:
 
Either download package, unzip, and run setup script:

```python
python3 setup.py install
```

Or use:

```python
pip3 install git+https://github.com/sidhomj/DeepTCR.git

```

## Release History

### 1.1
Initial release including two methods for unsupervised learning (VAE & GAN). Also included
ability to handle paired alpha/beta data.

### 1.2
Second release included major refactoring in code to streamline and share methods across 
classes. Included ability for algorithm to accept v/d/j gene usage. Added more analytical fetures and
visualization methods. Removed GAN from unsupervised learning techniques. 

#### 1.2.7
On-graph clustering method introduced for repertoire classifier to improve classification performance.

#### 1.2.13
Ability for HLA information to be incorporated in the analysis of TCR-Seq. 

#### 1.2.24
Added ability to do regression for sequence-based model.

### 1.3
Third release including improved repertoire classification architecture. Details in method will follow 
in manuscript.






