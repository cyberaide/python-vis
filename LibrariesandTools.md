## Libraries and Tools

Most of the libraries/tools below use pip to install. If you do not already have pip installed, here is the code to do so:

#### Linux & MacOS

```bash 
$ python -m ensurepip --upgrade
```

#### Windows

```bash
C:> py -m ensurepip --upgrade
```


### GraphViz

graphviz is an open source python mod that is used to create graph visualizations as a way of representing structural information as graphs and networks. [^5]

[^5]: * <https://graphviz.org/>


#### Installation

##### Ubuntu

```bash
$ sudo apt install graphviz -y
$ pip install graphviz
```

#### Gallery

* <https://graphviz.org/gallery/>

### matplotlib

Matplotlib is a library in Python for creating static (still figures), animated (moving pictures), and interactive vizualizations such as charts, graphs and scatter plots. It is one of the oldest and most popular plotting libraries in Python. 

#### Installation

##### From official release (Python)

```bash
python -m pip install -U pip
python - m pip install -U matplotlib
```
[^1]

##### Ubuntu

```bash
$ sudo apt-get install python3-matplotlib
```
[^1]
[^1]: * <https://matplotlib.org/stable/users/installing.html>

#### Gallery

* https://matplotlib.org/stable/gallery/index.html

### seaborn
Seaborn is a data vizualization tool in Python based on matplotlib. Seaborn is used for making statistical graphics, Helping you to explore and understand your data with a visual representation. It allows you to focus on the meaning of your plots rather than on the details of drawing them. 

#### Installation

```bash
$ pip install seaborn
```

#### Gallery

 * <https://seaborn.pydata.org/examples/index.html>

### ggplot

ggplot is run in plotnine, a grammar of graphics package in Python. It is based on the library written in R. 


### bokeh

bokeh is a Python library used mostly for creating interactive vizualization sets. vizualizations created in bakeh are powered by JavaScript without the user having to write any JavaScript themselves. Vizualizations created in bokeh can range from simple line plots to large and complex dashboards containing multiple datasets. 

#### Installation

```bash
$ pip install bokeh
```

#### Gallery

* <https://docs.bokeh.org/en/latest/docs/gallery.html#gallery>

### altair

Altair is a declarative statistical vizualization library for Python. [^2]

[^2]: * <https://altair-viz.github.io/>

#### Installation

```bash
$ pip install altair vega_datasets
```
The above line of code only installs a partial version of altair. You can find instructions on how to install the master version of Altair here: * https://altair-viz.github.io/getting_started/installation.html

#### Gallery

* https://altair-viz.github.io/gallery/index.html

### pygal

pygal is a dynamic Scalable Vector Graphics (SVG)library in Python. 

#### Installation

```bash
pip install pygal
```

#### Gallery

* <http://www.pygal.org/en/latest/index.html>

### plotly

plotly is a graphing library in Python that is used to make interactive, publication quality graphs. It is built on top of plotly's Javascript library and supports over 40 chart types. 

#### Installation

##### Using pip

```bash
$ pip install plotly==5.3.1
```

##### Using conda

```bash
$ conda install -c plotly plotly=5.3.1
```

#### Gallery (basic charts)

* <https://plotly.com/python/basic-charts/>


### geoplotlib

geoplotlib is a Python toolkit for creating vizualization of geographical data. It can be used to make maps, spatial graphs, etc. 

#### Installation

##### Required packages for geoplotlib:
* pip
* numpy
* pyglet

```bash
pip3 install geoplotlib
```

#### Examples (dot density and spatial graph)

* <https://www.pluralsight.com/guides/building-geoplots-with-geoplotlib> 

### gleam

Gleam allows a user to make interactive web interface versions of plots and graphs. A user can control a specified number of inputs and you can use any sort of Python graphing library to plot those inputs. Gleam provides the web interface that allows anyone to control the data in real time. 


### missingno

missingno provides a series of visualizations to help users understand the presence and distribution of missing data within the pandas datafram, which we will discuss later. [^4] From the plots created using missingno, users can identify where missing values occur, if they are correlated, etc. 

[^4]: * <https://towardsdatascience.com/using-the-missingno-python-library-to-identify-and-visualise-missing-data-prior-to-machine-learning-34c8c5b5f009>

#### Installation

```bash 
pip install missingno
```

### leather

leather is a Python library that outputs simple data visualizations. Leather allows you to graph your data without having to worry about anything fancy. 

#### Installation

```bash
pip install leather
```

#### Examples 

* <https://leather.readthedocs.io/en/0.3.3/examples.html>

### bqplot

bqplot is a 2-D interactive visualization library in the Jupyter Notebook. In bqplot, all components are interactive, allowing the user to integrate visualization s with other Jupyter interactive widgets to create integrated GUIs with a few lines of Python code. [^3]

[^3]: * <https://github.com/bqplot/bqplot>

#### Installation

##### With pip:
```bash
$ pip install bqplot
```

##### With conda:
```bash
$ conda install -c conda-forge bqplot
```

#### Examples

* <https://bqplot.readthedocs.io/en/latest/usage.html#examples>

### pandas 

pandas is an open source data analysis and manipulation tool. It is build on top of the Python language.

#### Installation/using pandas

```bash
import pandas
```

