Generating data for the plots
=============================

The files `name_neurons.txt` and `NeuronConnect.txt` both come from [wormweb.org](http://wormweb.org/). Links to both files and more information can be found in their [details page](http://wormweb.org/details.html).

The file `CElegansNeuronTables-connectome.csv` was originally found in the [CElegansNeuroML](https://github.com/openworm/CElegansNeuroML) repository. The original file there has been updated since then and is now called `CElegansNeuronTables.xls`.

The Jupyter notebook in this repository called `compare-and-compute-statistics.ipynb` goes through a detailed analysis of the data in the three files and contains detailed comments on each step. It also generates some useful output files:

* `non-pharyngeal-edges.csv` contains an edge-list representation of the non-pharyngeal portion of the connectome as an undirected graph. It was used to create the plot in the Gephi file `c-elegans-undirected.gephi`. It lists 2290 edges. 
* `non-pharyngeal-directed-edges.csv` contains a directed edge list for the non-pharyngeal portion of the connectome. It was used to create the plot in the Gephi file `c-elegans-new-directed.gephi` and contains 2997 edges.
* `in-degree-dist.csv` and `out-degree-dist.csv` contain the in-degree and out-degree frequencies for the directed non-pharyngeal graph. These files are used in the notebook `c-elegans-degree-dists.ipynb` to plot the distributions.

## Requirements

These Jupyter notebooks were created with Jupyter Lab for Python 3.8. The following additional packages are required in order to run them:

```
matplotlib>=3.5.1
numpy>=1.22.3
python-igraph>=0.9.10
pandas>=1.5.3
```
