---
layout: default
title: Thomas H. Keefe | Research
permalink: research 
---

<html > 
<head><title></title> 
<meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1"> 
<meta name="generator" content="TeX4ht (http://www.tug.org/tex4ht/)"> 
<meta name="originator" content="TeX4ht (http://www.tug.org/tex4ht/)"> 
<!-- html --> 
<meta name="src" content="main.tex"> 
<link rel="stylesheet" type="text/css" href="main.css"> 
</head>
<body >
<div class="center" 
>
<!--l. 435--><p class="noindent" >
<!--l. 435--><p class="noindent" >

<div><h2>Research</h2><br></div>

    
<h3>Full Bayes SVD in Stan</h3>
This work develops the singular value composition in the Bayesian modeling language <a href="https://mc-stan.org/">Stan</a>. 
The Bayesian approach allows us to model the uncertainty in singular values and singular vectors from an observed dataset. 
Because the matrices of left and right singular vectors are orthonormal, this model requires sampling from the <i>Stiefel manifold</i> of orthonormal matrices. 
It is a "full Bayes" approach in that every parameter in the model has a prior; none are plug-in estimates. 
<a href="{{site.url}}/assets/BayesSVDPoster.pdf">Poster presented at Bayes, Fiducial, and Frequentist Conference</a> in May 2023; a manuscript is under preparation.
<br><br>

<h3>Powerful significance testing for unbalanced clusters</h3>
Clustering is a large topic within machine learning, with many algorithms available and applications in diverse scientific areas. However, there are few methods for statistically determining if the clusters are "really there" or if they represent a noise aspect in the sample at hand. 
The <a href="https://www.tandfonline.com/doi/abs/10.1198/016214508000000454">SigClust</a> methodology is one approach that has been useful in validating clusters, but it fails in the important case when the clusters of interest are of very unbalanced sizes, such as in the case of rare subtypes of disease.
We develop a method that is statistically powerful in both the balanced and unbalanced regimes, using a novel measure of cluster quality that accounts for cluster size. 
The preprint is available <a href="https://arxiv.org/abs/2308.13079">here</a>.
<br><br>

<h3>Patterns of variation among baseline femoral and tibial cartilage thickness and clinical features</h3>
Using a novel dataset of knee cartilage thickness maps estimated from MRI, we use the data-integration methodology <a href="https://doi.org/10.1016/j.jmva.2018.03.008">Angle-based Joint and Individual Variation Explained</a> (AJIVE) to find modes of variation expressed simultaneously across femoral cartilage, tibial cartilage, and clinical/demographic features.
We found three significant and interpretable modes of variation: the first corresponding to overall size; the second to extent of arthritic cartilage thinning in weight bearing regions of the knee; and the third to medial/lateral predominance of cartilage thinning.
Our <a href="https://doi.org/10.1016/j.ocarto.2023.100334">manuscript</a> was published in <i>Osteoarthritis and Cartilage Open</i> in February 2023, and I presented a <a href="{{site.url}}//assets/CartilageOarsi20200420Final.pdf">poster</a> at OARSI Connect 2021 (online).
<br><br>

<h3>Biclustering reveals potential knee OA phenotypes in exploratory analyses</h3>
This work uses biclustering, a family of methods that cluster both the rows and columns of a dataset, to identify candidate phenotypes of knee osteoarthritis from a large dataset of clinical and demographic measurements from the <i>Osteoarthritis Initiative</i>.
Our <a href="https://doi.org/10.1371/journal.pone.0266964">manuscript</a> was published in <i>PLOS ONE</i> in May 2022.

<ul>


