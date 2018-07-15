# Sardinia Fires

Exploratory data analysis and visualization of fires in Sardinia from 2005 to 2016.

![An image showing the fires in Sardinia from 2005 to 2016](https://raw.githubusercontent.com/jackdbd/sardinia-fires/master/screenshots/sardinia-fires.png "Fires in Sardinia from 2005 to 2016.")

![A GIF showing an animation of the dataset on Kepler.gl](https://raw.githubusercontent.com/jackdbd/sardinia-fires/master/screenshots/sardinia-fires.gif "Fires in Sardinia from 2005 to 2016, animation running on Uber's Kepler.gl.")


## Data

You will need to download several datasets freely available on the [Opendata Sardegna](http://dati.regione.sardegna.it/dataset) portal. See to the notebook `sardinia-fires.ipynb`.


## Installation

Create a conda environment. You can use either [Miniconda](https://conda.io/miniconda.html) or [Anaconda](https://repo.continuum.io/).

```shell
conda create --name sardinia-fires python=3.6 --yes
```

Activate the environment.

```shell
source activate sardinia-fires
```

Install all the dependencies (this might take a while):

```shell
conda install -c conda-forge geopandas jupyter --yes
```

*Note*: there seem to be some issues with fiona (one of geopandas's dependencies). I had to downgrade to `fiona 1.7.9`.

```shell
conda install -c conda-forge fiona=1.7.9
```

When all dependencies have been installed, run the notebook:

```shell
jupyter notebook
```


## Other

You can freeze your environment with:

```shell
conda env export > environment.yml
```

To remove this conda environment, run:

```shell
conda env remove -n sardinia-fires
```
