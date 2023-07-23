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
</head><body 
>
<div class="center" 
>
<!--l. 435--><p class="noindent" >
<!--l. 435--><p class="noindent" >

<div><h2>Research Interests</h2><br></div>
<!--l. 438--><p class="noindent" >&#x00A0;&#x00A0;&#x00A0;&#x00A0;&#x00A0;My research focuses on developing statistical methodologies that are theoretically attractive and broadly applicable, often taking
a Bayesian or Generalized Fiducial perspective. I believe a &#8220;sweet spot&#8221; exists where my passion for theoretical statistics research
leads to positive human impacts, and I am looking for complicated and unique applications in pursuit of this intersection.
In my consulting work for the Mayo Clinic, I develop a novel Bayesian changepoint detection system that meets a
real need for the in-process models in its hospitals. This method detects a broad class of changes in longitudinal
data while simultaneously determining a changepoint&#8217;s cause. An additional research interest of mine is Generalized
Fiducial Inference (GFI), which is a modern perspective on Fisher&#8217;s fiducial argument [<a 
href="#Xfisher1935">2</a>,&#x00A0;<a 
href="#Xhannig2016">3</a>]. My theoretical work uses
differential geometry to define a Generalized Fiducial Distribution (GFD) on smooth manifolds. This distribution has
strong inferential capabilities on a large class of constrained parameter spaces and exhibits many useful theoretical
qualities.
    
<ul>
<br>
<h3>Bayesian Changepoint Detection for Mixed Data with Missing Values</h3> <!--l. 442--><p class="noindent" >&#x00A0;&#x00A0;&#x00A0;&#x00A0;&#x00A0;<span 
class="cmbx-10"></span> This project is motivated by monitoring issues
which were observed after the implementation of Murphree et al.&#8217;s [<a 
href="#Xmurphree2021">9</a>] model at the Mayo Clinic in Rochester, MN. Over the past few
years, stark changes in patient hospital data (such as major influxes of missing values due to data pipeline issues) have been
discovered only after model performance has dropped, which has led to a lack of reliability for care providers using the model. The
primary aim of this project is to develop a fast algorithm that can locate and identify the cause of significant changes in the data so
that they can be either addressed and corrected, or the model refit. We do this by classifying the data into homogeneous groupings in
time, called regimes.
<!--l. 444--><p class="noindent" >&#x00A0;&#x00A0;&#x00A0;&#x00A0;&#x00A0;Our design choices were made with ubiquitous real-world data issues in mind, such as high proportions of missingness and
mixed variable types. We further emphasized versatility; our model is able to handle a broad array of different data changes, including
center and spread shifts as well as significant changes to the missingness structure. A vector of regime assignments for a fixed set of
time points, a regime vector, is modeled as a set of sequential observations from a Markov process with unknown
transition probabilities. Given such a regime vector, the data are modeled as a mixture Gaussian Graphical Model
(GGM) with fixed graph structure, using a conjugate Normal-<span 
class="cmmi-10">G</span>-Wishart (NGW) prior, which we introduce as a
generalization of the Normal-Wishart distribution from [<a 
href="#Xbishop2006">1</a>] where the Wishart is replaced by a <span 
class="cmmi-10">G</span>-Wishart. We use
a Double Reversible Jump Metropolis-Hastings algorithm to learn the graph structure <span 
class="cmti-10">alongside </span>other parameter
values and make use of Lenkoski&#8217;s efficient sampling procedure to draw proposal precision matrices from a G-Wishart
distribution [<a 
href="#Xlenkoski2013">4</a>]. For the purpose of calculating acceptance probabilities in our MCMC algorithm, this framework requires
the computation of <span 
class="cmmi-10">G</span>-Wishart normalizing constants. These normalizing terms are notoriously difficult to calculate
in the literature, since they require integrating over a space of positive-definite precision matrices with fixed zero
structure (for instance, see [<a 
href="#Xlenkoski2013">4</a>,&#x00A0;<a 
href="#Xmohammadi2015">6</a>,&#x00A0;<a 
href="#Xmohammadi2021">7</a>,&#x00A0;<a 
href="#Xwang2012">10</a>]). In lieu of calculating these terms directly, we use a Laplace Approximation [<a 
href="#Xlenkoski2011">5</a>].
Our changepoint detection system learns a rich array of models in addition to determining changepoints. We make
use of these models in our development of a fault detection system, which identifies and describes the causes of a
changepoint.
    </p>   
<ul>
<br>
<h3>Generalized Fiducial Inference on Differentiable Manifolds [<a 
href="#Xmurph2022">8</a>]</h3>
<!--l. 442--><p class="noindent" >&#x00A0;&#x00A0;&#x00A0;&#x00A0;&#x00A0;<span 
class="cmbx-10"></span> I am broadly interested in the intersection of statistics
and Riemannian Geometry. In this project, we introduce a novel approach to inference on parameters that take values in a
Riemannian manifold embedded in a Euclidean space. Specifically, on a manifold, embedded in <span 
class="msbm-10">&#x211D;</span><sup><span 
class="cmmi-7">d</span></sup>, that can be determined completely
by the level set of some everywhere differentiable function <span 
class="cmmi-10">g</span>, i.e. <span 
class="cmsy-10"><img 
src="https://sirmurphalot.github.io/assets/cmsy10-4d.png" alt="M" class="10x-x-4d" /> </span>= <span 
class="cmsy-10">{</span><span 
class="cmmi-10">&#x03B8; </span><span 
class="cmsy-10">&#x2208; </span><span 
class="msbm-10">&#x211D;</span><sup><span 
class="cmmi-7">d</span></sup> : <span 
class="cmmi-10">g</span>(<span 
class="cmmi-10">&#x03B8;</span>) = 0<span 
class="cmsy-10">}</span><span 
class="cmmi-10">. </span>Parameter spaces of this form are
ubiquitous across many fields, including chemistry, physics, computer graphics, and geology. A simple example of a manifold of this
form is the unit sphere <span 
class="cmsy-10">{</span><span 
class="cmmi-10">x </span>: <span 
class="cmmi-10">g</span>(<span 
class="cmmi-10">x</span>) := <span 
class="cmsy-10">||</span><span 
class="cmmi-10">x</span><span 
class="cmsy-10">||- </span>1 = 0<span 
class="cmsy-10">}</span>. This new approach uses GFI to obtain a probability distribution on the constrained
parameter space (a posterior-like distribution without defining a prior), without requiring a parameterization that maps the
constrained space to an unconstrained Euclidean space. The proposed methodology, called the constrained generalized fiducial
distribution (CGFD), is obtained by using mathematical tools from Riemannian geometry. A Bernstein-von Mises-type result for the
CGFD is provided, which shows how the desirable asymptotic qualities of the unconstrained GFD are inherited by the
CGFD.
    </p>
<!--l. 442--><p class="noindent" >&#x00A0;&#x00A0;&#x00A0;&#x00A0;&#x00A0;<span 
class="cmbx-10"></span> Similar to the Bayesian posterior, the CGFD must often be estimated using MCMC methods. This introduces the need for
sampling parameter values on a manifold. As part of this project, we extend existing methodology to sample from the CGFD,
including manifold-variants of a random-walk Metropolis-Hastings algorithm and a Hamiltonian Monte Carlo algorithm. In the
experiment in Figure <a 
href="#x1-21">1<!--tex4ht:ref: fig:brain_eigen --></a>, we apply different manifold MCMC algorithms and numerical approximation methods to take
samples from the CGFD when the mean parameters of a multivariate normal distribution are assumed to be on a
sphere. <br>
    </p>
    
<center>
<img 
src="https://sirmurphalot.github.io/assets/FourSpheres-.png" alt="PIC" width="600" 
     height="400"  
>
<br /> 
<!--l. 444--><div class="caption" 
><span class="id">Figure&#x00A0;1:  </span><span  
class="content"><span 
class="cmr-9">Samples  from  the</span>
<span 
class="cmr-9">CGFD</span>
<span 
class="cmr-9">using multiple manifold-sampling</span>
<span 
class="cmr-9">MCMC algorithms.</span></span></div><!--tex4ht:label?: x1-21 -->
</center>
<br>
   
<h3>Future Work</h3>
<!--l. 442--><p class="noindent" >&#x00A0;&#x00A0;&#x00A0;&#x00A0;&#x00A0;<span 
class="cmbx-10"></span> I am interested in developing the <span 
class="cmmi-10">&#x03F5;</span>-admissibility (EAS) methodology of [<a 
href="#Xwilliams2019">11</a>] for model selection with GGMs,
which will introduce a creative new means for graphical selection in GGMs as well as a novel method to predict general precision
matrices. The EAS methodology leverages notions of redundancy to manage the size of the sample space of possible models.
Furthermore, this problem presents an interesting application for the CGFD; the fixed zero structure of a GGM can be expressed as a
differentiable level set. The beauty of this approach is that it realistically expects and addresses the ubiquitous issue of huge numbers of variables <span 
class="cmmi-10">p </span>and sample sets <span 
class="cmmi-10">n</span>, a problem that causes the probability of every possible model
(including the true model <span 
class="cmmi-10">M</span><sub><span 
class="cmr-7">0</span></sub>) to tend towards zero. In numerous cases, the EAS approach gives strong consistency of
the posterior-like probability of the true oracle model <span 
class="cmmi-10">r</span>(<span 
class="cmmi-10">M</span><sub><span 
class="cmr-7">0</span></sub><span 
class="cmsy-10">|</span><span 
class="cmbx-10">Y</span>), in which the probability mass of the true model
approaches 1 as <span 
class="cmmi-10">n,p </span><span 
class="cmsy-10">&#x2192;&#x221E;</span>, or pairwise consistency, in which <span 
class="cmmi-10">r</span>(<span 
class="cmmi-10">M</span><sub><span 
class="cmr-7">0</span></sub><span 
class="cmsy-10">|</span><span 
class="cmbx-10">Y</span>)<span 
class="cmmi-10">&#x2215;r</span>(<span 
class="cmmi-10">M</span><span 
class="cmsy-10">|</span><span 
class="cmbx-10">Y</span>) <span 
class="cmsy-10">&#x2192;&#x221E; </span>for all <span 
class="cmmi-10">M </span><span 
class="cmsy-10">&#x2208;<img 
src="https://sirmurphalot.github.io/assets/cmsy10-4d.png" alt="M" class="10x-x-4d" />\ </span><span 
class="cmmi-10">M</span><sub><span 
class="cmr-7">0</span></sub> as <span 
class="cmmi-10">n,p </span><span 
class="cmsy-10">&#x2192;&#x221E;</span>
[<a 
href="#Xwilliams2022">12</a>].
</p>

<h3 class="likesectionHead"><a 
 id="x1-1000"></a>References</h3>
<!--l. 1--><p class="noindent" >
    <div class="thebibliography">
    <p class="bibitem" ><span class="biblabel">
 <a 
 id="Xbishop2006"></a>[1] <span class="bibsp">&#x00A0;&#x00A0;&#x00A0;</span></span>Christopher&#x00A0;M.  Bishop.     <span 
class="cmti-10">Pattern  Recognition  and  Machine  Learning  (Information  Science  and  Statistics)</span>.
    Springer-Verlag, Berlin, Heidelberg, 2006.
    </p>
    <p class="bibitem" ><span class="biblabel">
 <a 
 id="Xfisher1935"></a>[2] <span class="bibsp">&#x00A0;&#x00A0;&#x00A0;</span></span>R.A. Fisher. The fiducial argument... <span 
class="cmti-10">Annals of Eugenics</span>, 6(4):391&#8211;398, 1935.
    </p>
    <p class="bibitem" ><span class="biblabel">
 <a 
 id="Xhannig2016"></a>[3] <span class="bibsp">&#x00A0;&#x00A0;&#x00A0;</span></span>Jan Hannig, Hari Iyer, Randy C.&#x00A0;S. Lai, and Thomas C.&#x00A0;M. Lee. Generalized fiducial inference: A review and new
    results. <span 
class="cmti-10">Journal of the American Statistical Association</span>, 111(515):1346&#8211;1361, 2016.
    </p>
    <p class="bibitem" ><span class="biblabel">
 <a 
 id="Xlenkoski2013"></a>[4] <span class="bibsp">&#x00A0;&#x00A0;&#x00A0;</span></span>Alex Lenkoski. A direct sampler for g-wishart variates. <span 
class="cmti-10">Stat</span>, 2(1):119&#8211;128, 2013.
    </p>
    <p class="bibitem" ><span class="biblabel">
 <a 
 id="Xlenkoski2011"></a>[5] <span class="bibsp">&#x00A0;&#x00A0;&#x00A0;</span></span>Alex Lenkoski and Adrian Dobra. Computational aspects related to inference in gaussian graphical models with the
    g-wishart prior. <span 
class="cmti-10">Journal of Computational and Graphical Statistics</span>, 20(1):140&#8211;157, 2011.
    </p>
    <p class="bibitem" ><span class="biblabel">
 <a 
 id="Xmohammadi2015"></a>[6] <span class="bibsp">&#x00A0;&#x00A0;&#x00A0;</span></span>A.&#x00A0;Mohammadi and E.&#x00A0;C. Wit.   Bayesian Structure Learning in Sparse Gaussian Graphical Models.   <span 
class="cmti-10">Bayesian</span>
    <span 
class="cmti-10">Analysis</span>, 10(1):109 &#8211; 138, 2015.
    </p>
    <p class="bibitem" ><span class="biblabel">
 <a 
 id="Xmohammadi2021"></a>[7] <span class="bibsp">&#x00A0;&#x00A0;&#x00A0;</span></span>Reza Mohammadi, Helene Massam, and Gerard Letac.  Accelerating bayesian structure learning in sparse gaussian
    graphical models, 2021.
    </p>
    <p class="bibitem" ><span class="biblabel">
 <a 
 id="Xmurph2022"></a>[8] <span class="bibsp">&#x00A0;&#x00A0;&#x00A0;</span></span>Alexander&#x00A0;C  Murph,  Jan  Hannig,  and  Jonathan&#x00A0;P  Williams.   Generalized  fiducial  inference  on  differentiable
    manifolds, 2022.
    </p>
    <p class="bibitem" ><span class="biblabel">
 <a 
 id="Xmurphree2021"></a>[9] <span class="bibsp">&#x00A0;&#x00A0;&#x00A0;</span></span>Dennis&#x00A0;H Murphree, Patrick&#x00A0;M Wilson, Shusaku&#x00A0;W Asai, Daniel&#x00A0;J Quest, Yaxiong Lin, Piyush Mukherjee, Nirmal
    Chhugani, Jacob&#x00A0;J Strand, Gabriel Demuth, David Mead, Brian Wright, Andrew Harrison, Jalal Soleimani, Vitaly
    Herasevich, Brian&#x00A0;W Pickering, and Curtis&#x00A0;B Storlie.   Improving the delivery of palliative care through predictive
    modeling and healthcare informatics.  <span 
class="cmti-10">Journal of the American Medical Informatics Association</span>, 28(6):1065&#8211;1073, 02
    2021.
    </p>
    <p class="bibitem" ><span class="biblabel">
<a 
 id="Xwang2012"></a>[10] <span class="bibsp">&#x00A0;&#x00A0;&#x00A0;</span></span>Hao  Wang  and  Sophia&#x00A0;Zhengzi  Li.   Efficient  Gaussian  graphical  model  determination  under  G-Wishart  prior
    distributions. <span 
class="cmti-10">Electronic Journal of Statistics</span>, 6(none):168 &#8211; 198, 2012.
    </p>
    <p class="bibitem" ><span class="biblabel">
<a 
 id="Xwilliams2019"></a>[11] <span class="bibsp">&#x00A0;&#x00A0;&#x00A0;</span></span>Jonathan&#x00A0;P. Williams and Jan Hannig.  Nonpenalized variable selection in high-dimensional linear model settings
    via generalized fiducial inference. <span 
class="cmti-10">The Annals of Statistics</span>, 47(3):1723 &#8211; 1753, 2019.
                                                                                                       
                                                                                                       
    </p>
    <p class="bibitem" ><span class="biblabel">
<a 
 id="Xwilliams2022"></a>[12] <span class="bibsp">&#x00A0;&#x00A0;&#x00A0;</span></span>Jonathan&#x00A0;P. Williams, Yuying Xie, and Jan Hannig. The eas approach for graphical selection consistency in vector
    autoregression models. <span 
class="cmti-10">Canadian Journal of Statistics</span>, n/a(n/a), 2022.
</p>
    </div>
