---
author: Garry Shi
pubDatetime: 2024-03-18T14:05:00Z
title: Collaboration Patterns with Jupyter Notebooks
slug: jupyter
featured: true
draft: false
tags:
  - software
  - learning
  - jupyter

description: Collaboration patterns with Jupyter notebooks
---

# Introduction

Jupyter notebooks are notebook applications that are built and maintained by the [Project Jupyter](https://docs.jupyter.org/en/latest/), open source. A notebook, specifically refers to the .ipynb file format, for which code inputs, outputs and metadata are stored into a singular file format, commonly used for Python, but have uses in Julia and R as well. There are multiple ways to interact with an edit Jupyter notebooks, which include a web based IDE which utilizes a Python kernel named Jupyterlab, to type and run code.

Jupyter notebooks have long history of use, from rapid prototyping for data scientist/machine learning engineers to get a trained Machine Learning model running; adjust hyper-parameters and train models, or simply to visualize data quick.

Most companies that make use of and regularly interact with data in large amounts will generally utilize Jupyter notebooks in some way. For example, Meta utilizes an internal Jupyter notebook sharing and management platform named [Bento](https://engineering.fb.com/2023/08/29/security/scheduling-jupyter-notebooks-meta/) to schedule and run notebooks, while [Netflix](https://netflixtechblog.com/scheduling-notebooks-348e6c14cfd6) has their own platform and system in which they run notebooks integrated into their workflow. Interestingly, its arguable that Jupyter notebooks are similar to Python scripts, but less on scripts and with a larger focus on data-based applications.

![Bento's System Architecture](@assets/images/jupyter/bento.webp)
_Bento's system architecture, found at [this link](https://engineering.fb.com/2023/08/29/security/scheduling-jupyter-notebooks-meta/)_

# Collaboration Patterns

Collaboration patterns in Jupyter notebooks are interesting due to the nature of Jupyter notebooks, but I'd argue that the nature of collaboration is dependent on the nature of the use of notebooks. As mentioned above, notebooks can be used for a number of purposes: from prototyping to production data transformation, etc. In my opinion, your choice of collaborative pattern should be dependent on the purpose of your notebook.

## Git

Git and its associated platforms (Gitlab/Github/etc.) are one of the most common ways for software developers to collaborate and manage version control. For most newer versions of Gitlab and Github, it is possible to view diffs between versions of Jupyter notebooks in a repository, but I have encountered issues with older Git-platforms not supporting viewing Jupyter notebook diffs on the platform or not being able to translate notebook metadata to proper formatted text. (ultimately, it depends on the environment)

## Live Collaboration with Jupyterlab / Extensions

![Jupyterlab RTC](@assets/images/jupyter/rtc.webp)
_Jupyterlab real-time collaboration at work, found at [this link](https://jupyterlab-realtime-collaboration.readthedocs.io/en/latest/)_

Jupyterlab provides an extension named (jupyter_collaboration)[https://jupyterlab-realtime-collaboration.readthedocs.io/en/latest/], which allows for real-time collaboration. This requires a shared link to a Jupyter notebook, which I personally haven't tried, but could lead to potential security issues (imo).

## Real-time Collaboration with Jupyterhub

Jupyterhub is a multi-user hub that provides individual Jupyterlab environments to users in a single Kubernetes cluster. You can find the details [here](https://jupyterhub.readthedocs.io/), but Jupyterhub provides support for real-time collaboration (RTC). This is similar to live collaboration with Jupyterlab, but in a corporate environment, it is probably more ideal to rely on a self-managed and maintained Kubernetes cluster for security in collaboration.

## Third-party platforms

Google collab allows for (not real time) collaboration in a notebook through a shared link. But this form of collaboration isn't in real-time, which might not necessarily be great for someone's specific usecase. Regardless, alternatives such as codecollab.io exist which allow for real-time platforms to collaborate and interact on a Jupyter notebook, though they might not be suitable in a corporate environment.

## Individual Prototyping

If one of your main goals in using a Jupyter notebook is to prototype on an individual level and maybe get a single person to code review your notebook, it could be ideal to rely on Git and its associated platforms, reducing the overhead needed to boot up a collaboration platform or set up a Jupyterlab environment with extensions.

However, for corporate and IT security, having full control over an IDE is necessary for security and management of collaborative tools to reduce possible avenues of compromise. Thus, depending on your company's protocols or partnerships with possible IDEs / available infrastructure, it might be more ideal to set up environments for individuals working on large amounts of data to prototype and create notebooks more efficiently.
