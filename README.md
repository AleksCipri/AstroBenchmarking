![](images/Astro-MNIST.png)

# ABOUT THE PROJECT
* Currently there are no official benchmarking datasets in astronomy (astro-MNIST) that can be used by the community to compare different ML models and techniques in order to understand the improvements and benefits of novel approaches.
* It is becoming increasingly hard to compare results to previous ML studies by other groups and authors. Not everyone uploads their dataset/code/detailed instructions to reproduce the published results. 
* Goal of the project - gather resources in one spot - links to available simulators (for dataset generation) and simulated / observed datasets; links to hosted datasets we prepared for various astronomical research fields (galaxy images, variable stars, supernova spectra etc.). Produce example Jupyter files for using datasets to facilitate easier use and learning and include a set of guidelines for astro-ML "best practices".

# ASTRO + ML BEST PRACTICES
* We believe in fair, transparent, open and reproducible science. 
* Below, we summarize what we believe are best practices for achieving these goals. Modern research (especially if it includes novel computing or machine learning techniques) has to comply with a set of requirements in order for other researchers to be able to understand, compare and reproduce the results. 
* Without transparency in both data acquisition/ preprocessing, coding and hyperparameter fine tuning, but also without model benchmarking on standardized but simple datasets (before applying models to specialized datasets unique to that research topic), we cannot produce trustworthy and reliable scientific results. 


## DATA
* **Data Acquisition**

- State all steps used to extract data from a database (if not as detailed instructions in the paper or the appendix of the paper, then point to the online resources you have that accompany the paper you published, i.e. GitHub repo or similar). 
- It would be useful to other researchers looking into your work if you also included SQL code or any other code you used to query the data.

* **Data Preprocessing**

- State all the steps taken chronologically to transform raw data to processed/tidy data (see [this](https://vita.had.co.nz/papers/tidy-data.pdf) paper). For example, you could write "created new columns for the mean and median of cols 1 and 2", "removed NaNs".
- It may also be useful if you provide images of or tables of the head of the data at each step of the preprocessing.

* **Data Description**

- State at what time and from where (which telescope/database) the data was collected.
- Include a “codebook” describing each variable and its units. 
- Perform exploratory analysis! Include visualizations from this analysis. This can be included in the repo page as additional content for readers.

* **Datasets in the Context of ML**

- The data sets for the supervised ML should be always clearly separated: validation set, training set and test set. Make sure you clearly state which subset is used when, since especially validation and test set names are often used interchangeably. 
- Explain in what ways the sets were chosen. Were images shuffled before separation? If so, is the random seed fixed and which seed was used? Were techniques such as k-fold cross validation involved?

## CODE

- Provide source code or pseudocode used to create plots/interact with data publicly or host a notebook/interface from which people can interact with the raw/tidy data. 
- Consider having a GitHub (or similar) repo where you can host all additional material and code and provide links to the datasets used (provided you are hosting them somewhere). Also include all the relevant links in the published paper.
- Mention the programming language, OS type and version, and version of software packages used.

* **Neural networks**

- If possible visualize your neural network.
- Briefly explain model architecture and give details about all hyperparameters used when training was performed. State which loss function was used, as well as the name of the optimizer and its parameters. 
- Justify your chosen metric in the choice of best parameters.
- Provide plots with training metric (training and validation loss/accuracy), and also report multiple performance metrics (precision, recall, F1 score etc.). If relevant, provide confusion matrices.
- Provide details about the best model chosen for testing phase. What is the reason for choosing the particular model? Is the goal of the model to maximize accuracy, precision or some other metric? Why?


# SIMULATIONS 

## DeepBench
<img src="images/DeepBench.png" width="300">

Simulation library for very simple simulations to benchmark machine learning algorithms. 
- Simple geometrical shapes that can resemble different astronomical objects

Access the repo [here](https://github.com/deepskies/DeepBench).

## SkyPy
<img src="images/skypy.png" width="300">

This package contains methods for modelling the Universe, galaxies and the Milky Way. Also included are methods for generating observed data.
- Galaxy morphology, luminosity and redshift distributions
- Halo and subhalo mass distributions
- Gravitational Wave binary merger rates
- Power Spectra using CAMB and Halofit
- Pipelines to generate populations of astronomical objects

Access the repo [here](https://github.com/skypyproject/skypy).

## Galaxy2Galaxy

This is a [library](https://github.com/ml4astro/galaxy2galaxy) of models, datasets, and utilities to build generative models for astronomical images. Next to usfull models using Variational Auto-Encoders, Self-Attention GANs, PixelCNNs and Normalizing Flows, it also has packages that can be used to generate usefull datasets:

- Framework for building image datasets using GalSim, a framework for simualting astronomical objects like stars or galaxies (read more about GalSim [here](https://github.com/GalSim-developers/GalSim)).

- Tools for building an image dataset from HSC Public data release.


# SIMULATED DATASETS

## Bolognia Lens Factory
<img src="images/lenses.png" width="300">

The BLF collects simulated gravitational lenses of different kinds and from different projects and makes them available to the community for any possible usage. Data sets can be in different formats (tables, maps, images) and some projects consist of simulated observations of gravitational lensing systems, mimicking the observing capabilities of existing or future facilities. Available datasets target lenses on a broad range of scales - lensing by galaxies, galaxy clusters and the large scale structure of the universe. You can acces these datasets [here](http://metcalf1.difa.unibo.it/blf-portal/index.html).

# REAL DATASETS

## AstroML
<img src="images/astroML.gif" width="300">

AstroML constains various datasets. Below we are presenting review.
AstroML has available routines for downloading and working on the astronomical data sets. For more details, see the documentation [therein](https://www.astroml.org/modules/classes.html#module-astroML.datasets).

### Sloan Digital Sky Survey (SDSS) Data

The survey obtained photometry for hundreds of millions of stars, quasars, and galaxies, and spectra for several million of these objects. In addition, the second phase of the survey performed repeated imaging over a small portion of the sky, called Stripe 82, enabling the study of the time-variation of many objects.

SDSS photometric data are observed through five filters, u, g, r, i, and z. A visualization of the range of these filters is shown below:

- [SDSS filters](https://www.astroml.org/examples/datasets/plot_sdss_filters.html)  

<img src="images/plot_sdss_filters_1.png" width="600">

- [SDSS Spectra](https://www.astroml.org/examples/datasets/plot_sdss_spectrum.html) 

<img src="images/plot_sdss_spectrum_1.png" width="600">

- [SDSS photometry](https://www.astroml.org/examples/datasets/plot_sdss_galaxy_colors.html)

<img src="images/plot_sdss_galaxy_colors_1.png" width="600">

- Other datasets:

There are several other avalable adtasets to chose from: [SDSS corected Spectra](https://www.astroml.org/examples/datasets/plot_corrected_spectra.html), [SDSS Spectroscopic Sample](https://www.astroml.org/examples/datasets/plot_sdss_specgals.html), [SDSS DR7 Quasar Catalog](https://www.astroml.org/examples/datasets/plot_dr7_quasar.html); data from other surveys such as [Nasa Sloan Atlas](https://www.astroml.org/examples/datasets/plot_nasa_atlas.html) and [Stripe 82 Standards + 2MASS](https://www.astroml.org/examples/datasets/plot_sdss_S82standards.html),
time Domain Data like [RRLyrae](https://www.astroml.org/book_figures/chapter10/fig_rrlyrae_reconstruct.html) or [LIGO data](https://www.astroml.org/examples/datasets/plot_LIGO_spectrum.html) and [WMAP temperature map](https://www.astroml.org/examples/datasets/plot_wmap_power_spectra.html).

<img src="images/WMAP.png" width="800">

For more plese see [here](https://www.astroml.org/user_guide/datasets.html).


### Example notebooks

AstroML also contains many example notebooks that can help the user extract and use the available datasets:

- One of many examples available in the astroML package is a notebook for using a Convolutional Neural Network for classifying SDSS galaxiy images. It can be accessed [here](https://www.astroml.org/book_figures/chapter9/fig_morph_nn.html). Note that there are many more examples available.

- Example (by Stephen Portillo) for using a dataset from astroML (RR Lyrae) with a decision tree algorithm can be found [here](https://github.com/AleksCipri/AstroBenchmarking/blob/master/examples/astro-ML_RRLyrae.ipynb).



# WANT TO CONTRIBUTE?
* We need combined knolwedge from the entire astro comunity and researchers from different fields! Are you working in ML? Do you have a suitable dataset that can be used for benchmarking? Do you have experience in coding, open-source software? Please reach out if you want to help!




