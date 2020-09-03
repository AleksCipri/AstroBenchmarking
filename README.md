![](images/Astro-MNIST.png)

# ABOUT THE PROJECT
* Currently there are no official benchmarking datasets in astronomy (astro-MNIST) that can be used by the community to compare different ML models and techniques in order to understand the improvements and benefits of novel approaches.
* It is becoming increasingly hard to compare results to previous ML studies by other groups and authors. Not everyone uploads their dataset/code/detailed instructions to reproduce the published results. 
* Goal of the project - gather resources in one spot - links to available simulators (for dataset generation) and simulated / observed datasets; links to hosted datasets we prepared for various astronomical research fields (galaxy images, variable stars, superova spectra etc.). Produce example jupyter files for using datasets to facilitate easier use and learning.

# ASTRO + ML BEST PRACTICES
* We believe in fair, transparent, open and reproducible science. 
* Here we summarize what we believe are best practices for achieving these goals. Modern research (especially if it includes novel computing or machine learning techniques) has to comply with a set of requirements in order for other researchers to be able to understand, compare and reproduce the results. 
* Without transparency in both data acquisition/ preprocessing, coding and hyperparameter fine tuning, but also without model benhmarking on standardized but simple datasets (before applying models to specialized datasets unique to that research topic), we cannot produce trustworthy and reliable scientific results. 
* The file can be found [here](https://github.com/AleksCipri/AstroBenchmarking/). 


## DATA
* **Data Acquisition**

-State all steps used to extract data from a database (if not as detailed instructions in the paper or the appendix of the paper, then point to the online resources you have that accompany the paper you published, i.e. GitHub repo or similar). 
- It would be useful to other researchers looking into your work if you also included SQL code or any other code you used to query the data.

* **Data Preprocessing**

-State all the steps taken chronologically to transform raw data to processed/tidy data (see [this](https://vita.had.co.nz/papers/tidy-data.pdf) paper). For example, you could write "created new columns for the mean and median of cols 1 and 2", "removed NANs".
-It may also be useful if you provide images of or tables of the head of the data at each step of the preprocessing.

* **Data Description**

-State at what time and from where (which telescope/database) the data was collected.
-Include a “codebook” describing each variable and its units. 
-Perform exploratory analysis! Include visualizations from this analysis. This can be included in the repo page as additional content for readers.

* **Datasets in the Context of ML**
- The data sets for the supervised ML should be always clearly separated: validation set, training set and test set. Make sure you clearly state which subset is used when, since especially validation and test set names are often used interchangeably. 
- Explain in what ways the sets were chosen. Were images shuffled before separation? If so, is the random seed fixed and which seed was used? 

## CODE
.......fill in......


# SIMULATIONS 

## DeepBench
![](images/DeepBench.png)

Simulation library for very simple simulations to benchmark machine learning algorithms. 
- Simple geometrical shapes that can resemble different astronomical objects

Access the repo [here](https://github.com/deepskies/DeepBench).

## SkyPy
![](images/skypy.png)

This package contains methods for modelling the Universe, galaxies and the Milky Way. Also included are methods for generating observed data.
- Galaxy morphology, luminosity and redshift distributions
- Halo and subhalo mass distributions
- Gravitational Wave binary merger rates
- Power Spectra using CAMB and Halofit
- Pipelines to generate populations of astronomical objects

Access the repo [here](https://github.com/skypyproject/skypy).




# SIMULATED DATASETS
.......fill in......



# REAL DATASETS

## AstroML
....fill in ......

Example for using a dataset from astroML (RR Lyrae) with a decision tree algorithm can be found [here](https://github.com/AleksCipri/AstroBenchmarking/blob/master/examples/astro-ML_RRLyrae.ipynb).



# WANT TO CONTRIBUTE?
* We need combined knolwedge from the entire astro comunity and researchers from different fields! Are you working in ML? Do you have a sutable dataset that can be used for benchmaring? Do you have experience in coding, open-source software? Please reach out if you want to help!




