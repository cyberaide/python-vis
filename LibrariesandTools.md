# Libraries and Tools

TODO: AS WE WILL REPLACE FOOTNOTES WITH PROPER CITATIOPNS FOOTNOTS CAN NOT
BE BEHIND A DO THE MUST BEE BEFORE THE DOT.

TODO: any citation that is not listed as citation in the main text
will be deleted automatically. so make sure they are used if you add them

TODO: A CITATION CAN NOT BE BEHIND A cod, it must be before and used
in a proper centence

We will be using the pip command in gitbash on Windows to install the
libraries/tools below. This will work if you are using an ENV3 based
installation of Python. Please refer to this documentation if you are
not familiar with ENV3 based installation:
<https://cybertraining-dsc.github.io/docs/tutorial/reu/python/>

## GraphViz

graphviz is an open source python mod that is used to create graph
visualizations as a way of representing structural information as
graphs and networks [^1].


### Installation

```bash
$ sudo apt install graphviz -y
$ pip install graphviz
```

### Gallery

* <https://graphviz.org/gallery/>

## matplotlib

Matplotlib is a library in Python for creating static (still figures),
animated (moving pictures), and interactive vizualizations such as
charts, graphs and scatter plots. It is one of the oldest and most
popular plotting libraries in Python.

### Installation

#### From official release (Python)

[^2] CITATION NOT NEEDED

```bash
python -m pip install -U pip
python - m pip install -U matplotlib
```

### Gallery

* https://matplotlib.org/stable/gallery/index.html

### Matplotlib Stacked Bar Chart Example

[^7] PLEASE INVENT YOUR OWN

```bash
import matplotlib.pyplot as plt


labels = ['G1', 'G2', 'G3', 'G4', 'G5']
men_means = [20, 35, 30, 35, 27]
women_means = [25, 32, 34, 20, 25]
men_std = [2, 3, 4, 1, 2]
women_std = [3, 5, 2, 3, 3]
width = 0.35       # the width of the bars: can also be len(x) sequence

fig, ax = plt.subplots()

ax.bar(labels, men_means, width, yerr=men_std, label='Men')
ax.bar(labels, women_means, width, yerr=women_std, bottom=men_means,
       label='Women')

ax.set_ylabel('Scores')
ax.set_title('Scores by group and gender')
ax.legend()

plt.show()
```



## seaborn

Seaborn is a data vizualization tool in Python based on
matplotlib. Seaborn is used for making statistical graphics, Helping
you to explore and understand your data with a visual
representation. It allows you to focus on the meaning of your plots
rather than on the details of drawing them.

### Installation

```bash
$ pip install seaborn
```

### Gallery

 * <https://seaborn.pydata.org/examples/index.html>


### Seaborn Scatterplot Example

PLEASE INVENT YOUR OWN [^6] 

```bash
import seaborn as sns
import matplotlib.pyplot as plt
sns.set_theme(style="whitegrid")

# Load the example diamonds dataset
diamonds = sns.load_dataset("diamonds")

# Draw a scatter plot while assigning point colors and sizes to different
# variables in the dataset
f, ax = plt.subplots(figsize=(6.5, 6.5))
sns.despine(f, left=True, bottom=True)
clarity_ranking = ["I1", "SI2", "SI1", "VS2", "VS1", "VVS2", "VVS1", "IF"]
sns.scatterplot(x="carat", y="price",
                hue="clarity", size="depth",
                palette="ch:r=-.2,d=.3_r",
                hue_order=clarity_ranking,
                sizes=(1, 8), linewidth=0,
                data=diamonds, ax=ax)
```


## ggplot

ggplot is run in plotnine, a grammar of graphics package in Python. It
is based on the library written in R.

### Installation

```bash
$ pip install plotnine
```

### GGplot bar chart

PLEASE INVENT YOUR OWN [^11] 

```python
from plotnine.data import mpg
from plotnine import ggplot, aes, geom_bar

ggplot(mpg) + aes(x="class") + geom_bar()
```


## bokeh

bokeh is a Python library used mostly for creating interactive
vizualization sets. vizualizations created in bakeh are powered by
JavaScript without the user having to write any JavaScript
themselves. Vizualizations created in bokeh can range from simple line
plots to large and complex dashboards containing multiple datasets.

### Installation

```bash
$ pip install bokeh
```

### Gallery

* <https://docs.bokeh.org/en/latest/docs/gallery.html#gallery>

### Bokeh Stacked Bar Chart Example

DID YOU INVENT THIS OR IS CITATION MISSING

```bash
from bokeh.plotting import figure, show

labels = ['G1', 'G2', 'G3', 'G4', 'G5']
genders = ["Men", "Women"]
colors = ["#c9d9d3", "#718dbf"]

data = {'labels' : labels,
        'Men'   : [20, 35, 30, 35, 27],
        'Women'   : [25, 32, 34, 20, 25]}

p = figure(x_range=labels, height=250, title="Scores by group and gender",
           toolbar_location=None, tools="hover", tooltips="$name @labels: @$name")

p.vbar_stack(genders, x='labels', width=0.9, color=colors, source=data,
             legend_label=genders)

p.y_range.start = 0
p.x_range.range_padding = 0.1
p.xgrid.grid_line_color = None
p.axis.minor_tick_line_color = None
p.outline_line_color = None
p.legend.location = "top_left"
p.legend.orientation = "horizontal"

show(p)
```

## altair

Altair is a declarative statistical vizualization library for Python [^3].


### Installation

```bash
$ pip install altair vega_datasets
```

The above line of code only installs a partial version of altair. You
can find instructions on how to install the master version of Altair
here:

* https://altair-viz.github.io/getting_started/installation.html

### Gallery

* https://altair-viz.github.io/gallery/index.html


### Altair Bar Chart Example

This example uses pandas in conjunction with altair, pandas
installation is referred to later on this page.

PLEASE INVENT YOUR OWN [^8]

```bash
import altair as alt
import pandas as pd

source = pd.DataFrame({
    'a': ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I'],
    'b': [28, 55, 43, 91, 81, 53, 19, 87, 52]
})

alt.Chart(source).mark_bar().encode(
    x='a',
    y='b'
)
```




## pygal

pygal is a dynamic Scalable Vector Graphics (SVG) library in Python. 

### Installation

```bash
pip install pygal
```

### Gallery

* <http://www.pygal.org/en/latest/index.html>

## plotly

plotly is a graphing library in Python that is used to make
interactive, publication quality graphs. It is built on top of
plotly's Javascript library and supports over 40 chart types.

### Installation

```bash
$ pip install plotly==5.3.1
```

### Gallery (basic charts)

* <https://plotly.com/python/basic-charts/>

### Plotly Stacked Bar Chart Example

IS THIS INVENTED BY YOU?

```bash
import plotly.graph_objects as go
labels = ['G1', 'G2', 'G3', 'G4', 'G5']

fig = go.Figure(data=[
    go.Bar(name='Women', x=labels, y=[25, 32, 34, 20, 25]),
    go.Bar(name='Men', x=labels, y=[20, 35, 30, 35, 27])
])
# Change the bar mode
fig.update_layout(barmode='stack')
fig.show()
```


## geoplotlib

geoplotlib is a Python toolkit for creating vizualization of
geographical data. It can be used to make maps, spatial graphs, etc.

### Installation

#### Required packages for geoplotlib:
* pip
* numpy
* pyglet

```bash
pip3 install geoplotlib
```

### Examples (dot density and spatial graph)

* <https://www.pluralsight.com/guides/building-geoplots-with-geoplotlib> 


### geoplotlib Dot Density Map Example


## gleam

Gleam allows a user to make interactive web interface versions of
plots and graphs. A user can control a specified number of inputs and
you can use any sort of Python graphing library to plot those
inputs. Gleam provides the web interface that allows anyone to control
the data in real time.

### Installation

```bash
$ pip install gleam
```

### Gleam Interactive Scatter Plot Example

PLEASE INVET YOUR OWN [^9]

```bash
from wtforms import fields
from ggplot import *
from gleam import Page, panels

class ScatterInput(panels.Inputs):
    title = fields.StringField(label="Title of plot:")
    yvar = fields.SelectField(label="Y axis",
                              choices=[("beef", "Beef"),
                                       ("pork", "Pork")])
    smoother = fields.BooleanField(label="Smoothing Curve")

class ScatterPlot(panels.Plot):
    name = "Scatter"

    def plot(self, inputs):
        p = ggplot(meat, aes(x='date', y=inputs.yvar))
        if inputs.smoother:
            p = p + stat_smooth(color="blue")
        p = p + geom_point() + ggtitle(inputs.title)
        return p

class ScatterPage(Page):
    input = ScatterInput()
    output = ScatterPlot()

ScatterPage.run()
```



## missingno

missingno provides a series of visualizations to help users understand
the presence and distribution of missing data within the pandas
datafram, which we will discuss later [^4]. From the plots created
using missingno, users can identify where missing values occur, if
they are correlated, etc.

### Installation

```bash 
pip install missingno
```

### missingno Bar Example

This example uses data from the NYPD Motor Vehicle Collisions Dataset [^15].

```bash
import pandas as pd
import missingno as msno
%matplotlib inline

# importing the dataset from 
collisions = pd.read_csv("https://raw.githubusercontent.com/ResidentMario/missingno-data/master/nyc_collision_factors.csv")

msno.bar(collisions.sample(1000))
```

[^16]


## leather

TODO: unimportant. Remove

leather is a Python library that outputs simple data
visualizations. Leather allows you to graph your data without having
to worry about anything fancy.

### Installation

```bash
pip install leather
```

### Gallery 

* <https://leather.readthedocs.io/en/0.3.3/examples.html>

### Leather Bar Chart Example

```bash
import leather

data = [
    (0, 3),
    (4, 5),
    (7, 9),
    (8, 4)
]

chart = leather.Chart('Dots')
chart.add_dots(data)
chart.to_svg('examples/charts/dots.svg')
```

[^12]

## bqplot

bqplot is a 2-D interactive visualization library in the Jupyter
Notebook. In bqplot, all components are interactive, allowing the user
to integrate visualization s with other Jupyter interactive widgets to
create integrated GUIs with a few lines of Python code [^5].

### Installation

```bash
$ pip install bqplot
```

### Gallery

* <https://bqplot.readthedocs.io/en/latest/usage.html#examples>

### Bqplot Line Chart Example

```bash
import numpy as np
from bqplot import pyplot as plt

plt.figure(1, title='Line Chart')
np.random.seed(0)
n = 200
x = np.linspace(0.0, 10.0, n)
y = np.cumsum(np.random.randn(n))
plt.plot(x, y)
plt.show()
```

[^10]

## pandas 

pandas is an open source data analysis and manipulation tool. It is
build on top of the Python language.

### Installation/using pandas

```bash
import pandas
```

### Pandas Bar Chart Example using Altair

PLEASE INVENT YOUR OWN [^8]

```bash
import altair as alt
import pandas as pd

source = pd.DataFrame({
    'a': ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I'],
    'b': [28, 55, 43, 91, 81, 53, 19, 87, 52]
})

alt.Chart(source).mark_bar().encode(
    x='a',
    y='b'
)
```



## ipywidgets

ipywidgets are HTML-interactive widgets used for Jupyter notebooks to
help users visualize changes in data.

### Installation

```bash
pip install ipywidgets
```

## jupyter

Jupyter consists of two web-based interfaces: JupyterLab and Jupyter
Notebook. JupyterLab is a development environment for various jupyter
notebooks code and data. Jupyter Notebook is an open-source
application that allows users to create and share documents that
contain live code, equations, vizualization and narrative text
[^13].

### Installation of JupyterLab 

```bash
$ pip install jupyterlab
```

### Running JupyterLab

```bash
$ jupyter-lab
```

### Installation of Jupyter Notebook

```bash
$ pip install notebook
```

### Running Jupyter Notebook

```bash
$ jupyter notebook
```

## tqdm

tqdm is a Python library that is used for creating progress meters/bars

### Installation

```bash
$ pip install tqdm
```

### tqdm simple example

```bash
import tqdm
for i in tqdm.trange(int(1e8)):
    pass
```
	
[^14]

## image manipulation

# Resources

[^1]: * <https://graphviz.org/>

[^2]: * <https://matplotlib.org/stable/users/installing.html>

[^3]: * <https://altair-viz.github.io/>

[^4]: * <https://towardsdatascience.com/using-the-missingno-python-library-to-identify-and-visualise-missing-data-prior-to-machine-learning-34c8c5b5f009>

[^5]: * <https://github.com/bqplot/bqplot>

[^6]: * <https://seaborn.pydata.org/examples/different_scatter_variables.html>

[^7]: * <https://matplotlib.org/stable/gallery/lines_bars_and_markers/bar_stacked.html#sphx-glr-gallery-lines-bars-and-markers-bar-stacked-py>

[^8]: * <https://altair-viz.github.io/gallery/simple_bar_chart.html>

[^9]: * <https://github.com/dgrtwo/gleam>

[^10]: * <https://bqplot.readthedocs.io/en/latest/usage.html#examples>

[^11]: * <https://realpython.com/ggplot-python/#plotting-data-using-python-and-ggplot>

[^12]: * <https://leather.readthedocs.io/en/0.3.3/examples.html>

[^13]: * <https://jupyter.org/>

[^14]: * <https://github.com/tqdm/tqdm/blob/master/examples/simple_examples.py>

[^15]: * <https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95>

[^16]: * <https://github.com/ResidentMario/missingno>
