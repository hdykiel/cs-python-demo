# Displaying python matplotlib graph inside of a shiny app
Process: write matplotlib.py script in RStudio. Executing program line by line in RStudio's python repl works, however running:

> reticulate::source_python('~/CS Python Demo/Shiny-Python/matplotlib.py')

Returns the following error message: 

> /opt/python/3.7.3/bin/python3:17: UserWarning: Matplotlib is currently using agg, which is a non-GUI backend, so cannot show the figure.

Naturally, using `source_python(maplotlib.py)` returns the same error. The solution here is to first export the python plot as an image (see [Communities post](https://community.rstudio.com/t/is-it-possible-to-plot-matplotlib-in-r-shiny-using-reticulate/28828/2))

# Reference a python function from Shiny 
Process: create a new python script, such as python_function.py using your favorite editor. If you have RStudio Server Pro w/ job launcher, you can use RStudio, Jupyter Notebook, or JupyterLab (and VS Code one day soon).

Use `reticulate::source_python()` to source your python functions and make them available in your R environment.