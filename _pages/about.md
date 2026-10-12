---
permalink: /
title: "About me"
excerpt: "Xin Xiong, postdoctoral researcher at HKBU, develops computational methods to study cellular heterogeneity and tumor-immune interactions."
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi, I'm Xin Xiong.

I am a Postdoctoral Research Fellow at [Hong Kong Baptist University](https://www.hkbu.edu.hk/).
I develop machine learning and statistical methods to study cellular
heterogeneity and tumor-immune interactions from transcriptomic and other omics data.

## Research Focus

My research addresses a central challenge in cancer biology: bulk tumor RNA
sequencing combines signals from different cell types into a single expression
profile, obscuring cellular heterogeneity. Computational deconvolution provides
a way to infer cellular composition from these mixed signals.

Building on my doctoral work on DeSide, I am developing a generative model based
on a variational autoencoder (VAE) to jointly infer cell-type proportions and
reconstruct cell-type-specific gene-expression profiles from bulk solid-tumor
transcriptomic data, using single-cell RNA-seq data as a reference.

My broader interests include biological foundation models, dynamical systems,
and spatial transcriptomics. I am interested in how these approaches, together
with multi-omics integration, can help us understand gene regulation,
tumor-immune interactions, and the spatial and temporal organization of tissues.
Across these directions, I emphasize interpretable models and systems-level understanding.

## News

{% assign news_posts = site.posts | where_exp: "post", "post.tags contains 'news'" %}
{% if news_posts.size > 0 %}
<ul>
{% for post in news_posts limit: 3 %}
  <li><strong>{{ post.date | date: "%b %d, %Y" }}</strong> - <strong>{{ post.title }}</strong>: {{ post.excerpt | markdownify | remove: '<p>' | remove: '</p>' }}</li>
{% endfor %}
</ul>
{% else %}
No news yet. Please check back later.
{% endif %}

## Selected Work

- **DeSide**: A unified deep learning framework for cellular deconvolution in the tumor microenvironment, designed to improve the interpretation of bulk transcriptomic data in cancer studies. [Article](https://www.pnas.org/doi/10.1073/pnas.2407096121), [GitHub](https://github.com/OnlyBelter/DeSide)
- **Ion mobility collision cross-section atlas**: Contributed to a large-scale resource for known and unknown metabolite annotation in untargeted metabolomics, expanding computational support for molecular identification. [Article](https://doi.org/10.1038/s41467-020-18171-8)
- **MetCCS predictor**: Developed a web server for predicting collision cross-section values of metabolites, helping support ion mobility-mass spectrometry based metabolomics analysis. [Article](https://doi.org/10.1093/bioinformatics/btx140)

## Brief Background

I completed my PhD in the Department of Physics at HKBU in September 2025 under
the mentorship of [Prof. Liang Tian](https://physics.hkbu.edu.hk/people/tian-liang).
My doctoral research led to DeSide, a deep learning framework for cellular deconvolution of the tumor microenvironment.

Earlier, I worked as a research assistant at the Shenzhen Institute of Synthetic Biology
under the guidance of [Prof. Xuefei Li](https://isynbio.siat.ac.cn/Li(x)lab/view.php?id=48),
where I began studying the tumor microenvironment and cellular deconvolution.
Before that, I worked at [ZhuLab](http://www.zhulab.cn) within the Interdisciplinary
Research Center on Biology and Chemistry in Shanghai, contributing to
computational tools for metabolomics and mass spectrometry data analysis.
I received my bachelor's degree (BEng) in Bioengineering from [Xi’an Polytechnic University](https://www.xpu.edu.cn/) and my master's degree (MEng) in Computer Science from [Shanghai Jiao Tong University](https://www.sjtu.edu.cn/) under the supervision of [Prof. Hai Zhao](https://bcmi.sjtu.edu.cn/home/zhaohai/).

Outside of research, I enjoy reading, watching movies, playing badminton, and practicing [photography](https://www.flickr.com/photos/200188531@N06/albums).


[//]: # ()
[//]: # (| <img width="200" alt="Xi'an" src="/images/myself/Just Graduated_2010.jpg">  @Xi'an )

[//]: # ()
[//]: # (| <img width="200" alt="Mount Tai" src="/images/myself/Mount Tai_2012Oct.jpg"> @Mount Tai    )

[//]: # ()
[//]: # (| <img width="200" alt="Guilin" src="/images/myself/Guilin_2013.jpg"> @Guilin      |)
