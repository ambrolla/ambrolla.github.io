---
layout: post
comments: true
title: "Neuroglancer"
tags:
  - Tech Challenges
  - Work Stuff
---

One of the coolest things I've seen in my life (the most other impressive thing, in my opinion that I did, was to look at the bacteria phages through electronic microscope back in University) is to work with Neuroglancer. I was very impressed with what technology is able to do nowdays (and realized how much I have to constantly learn and read in order to keep up).

Neuroglancer is high-performance, flexible WebGL-based viewer and visualization framework for volumetric data. It supports a wide variety of data sources and can display arbitrary (non axis-aligned) cross-sectional views of volumetric data and 3-D meshes and line-segment-based models (skeletons). Neuroglancer is a powerful tool for large-scale neuroscience datasets, which can be impractical to visualize with other traditional image viewer applications.

The part I've worked with is to install and run Neuroglancer locally. And later, using Jupyter Notebook (in my local environment) create a Navigation Panel where you can manipulate different display settings. This, I did using Python.

This [link](https://connectomics.readthedocs.io/en/latest/external/neuroglancer.html) helped me with the Neuroglancer installation. This [link](https://github.com/google/neuroglancer/blob/master/python/examples/jupyter-notebook-demo.ipynb) where you can see the Neuroglancer Example in Jupyter Notebook, that I've used to create a Nav Panel. This [link](https://neuroglancer-demo.appspot.com/#!%7B%22dimensions%22:%7B%22x%22:%5B8e-9%2C%22m%22%5D%2C%22y%22:%5B8e-9%2C%22m%22%5D%2C%22z%22:%5B8e-9%2C%22m%22%5D%7D%2C%22position%22:%5B3004.24853515625%2C3322.9228515625%2C4205.5%5D%2C%22crossSectionScale%22:0.7749164979610815%2C%22projectionOrientation%22:%5B0.31435418128967285%2C0.8142172694206238%2C0.4843378961086273%2C-0.06040274351835251%5D%2C%22projectionScale%22:4593.980956070107%2C%22layers%22:%5B%7B%22type%22:%22image%22%2C%22source%22:%22precomputed://gs://neuroglancer-public-data/flyem_fib-25/image%22%2C%22tab%22:%22source%22%2C%22name%22:%22image%22%7D%2C%7B%22type%22:%22segmentation%22%2C%22source%22:%22precomputed://gs://neuroglancer-public-data/flyem_fib-25/ground_truth%22%2C%22tab%22:%22source%22%2C%22segments%22:%5B%22158571%22%2C%2221894%22%2C%2222060%22%2C%2224436%22%2C%222515%22%5D%2C%22name%22:%22ground-truth%22%7D%5D%2C%22showSlices%22:false%2C%22selectedLayer%22:%7B%22visible%22:true%2C%22layer%22:%22image%22%7D%2C%22layout%22:%224panel%22%7D) where you can play with Neuroglancer, with the default Nav Bar. And [here](https://github.com/ambrolla/examples/blob/Neuroglancer/Neuroglancer.ipynb) is my code.

Below is the image of my Navigation Panel (that I've made) with the output.

![Neuroglancer](/images/Neuroglancer.png)

And this is the code that I wrote, to implement changes to the viewer. Also, I made it possible to use Neuroglancer methods to do changes in viewer state on Neuroglancer server side directly considering pretty limited Neuroglancer documentation.

![Neuroglancer work](/images/Neuroglancer_work.png)
