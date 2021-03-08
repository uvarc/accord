---
layout: default
---

# Environments

Environments consist of web-based, containerized interfaces launched on-demand by researchers. Approved environemnts 
and details about them are below. ACCORD strives to use rich, well-supported, usable container images with quality
documentation  and healthy user communities supporting them.


## Theia Python

A rich IDE that allows researchers to manage their files and data, write code with an intelligent editor, and execute 
code within a terminal session.

![Theia](accord/docs/assets/img/theia-screenshot.jpg)

Learn more about the `Theia Python IDE <https://theia-ide.org/>`_

## Jupyter Lab

Allows for interactive, notebook-based analysis of data. A good choice for pulling quick results or refining your code in 
numerous languages including Python, R, Julia, bash, etc.

.. image:: ../_static/images/jupyter_sample.png
   :alt: Jupyter Lab
   :align: center
   :width: 80%

Learn more about `Jupyter Lab <https://jupyter.org/>`_


## RStudio

The standard IDE for research using the R programming language. This environment is useful for generating plots and 
other R-based analysis.

.. image:: ../_static/images/rstudio_example.png
   :alt: Jupyter Notebook
   :align: center
   :width: 80%

Learn more about `RStudio <https://rstudio.com/>`_


## Runtimes & Limitations


- Computing environments can be used for short-lived, interactive, computing and analysis.
- Environments may also be used for longer, more intensive job runs that may last for hours. 
- For extended runs, you may close your browser tab and return later, if so desired.
- While environments cannot be "paused" their configuration can easily be repeated.
- Environments are bound to 16 cores / 48GB of memory / 1TB of cluster storage.
- Outbound access to the Internet is restricted to package and library mirrors such as pip, PyPi, CPAN, CRAN, etc.
- ACCORD is not a BYOC (Bring Your Own Container) environment, but we welcome your suggestions for additional containers to be considered in the future.
