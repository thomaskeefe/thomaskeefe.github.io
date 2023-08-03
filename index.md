---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: default
title: Thomas H. Keefe
permalink: 
---
<div class="banner">
    <div class="photo">
        <img src="{{site.url}}/assets/tom_china.jpg" width="207px" height="200px"> 
    </div>
    <div class="contact">
        <font size="+2">Thomas H. Keefe</font> <br>
        PhD Candidate, Statistics & Operations Research<br>
        UNC-Chapel Hill<br>
        <a href="mailto:{{site.email}}"> <img src="{{site.url}}/css/icons/gmail.jpg"  class="icon"> </a>
        <a href="https://www.linkedin.com/in/thomas-keefe-52b80073/"><img src="{{site.url}}/css/icons/linkedin.jpg"  class="icon"> </a>
        <a href="https://github.com/thomaskeefe"><img src="{{site.url}}/css/icons/github.png" class="icon"></a>
    </div>
</div>
<div class="homecontent">
    <br>
    <br>
    <p>
        <h3>About Me</h3>
        I am finishing my PhD in Statistics and Operations Research at UNC-Chapel Hill, where I work with 
        <a href="https://marron.web.unc.edu/">J. S. Marron</a>, 
        <a href="https://hannig.cloudapps.unc.edu/">Jan Hannig</a>, and 
        <a href="https://www.med.unc.edu/medicine/rheumatology-allergy-immunology/people/amanda-e-nelson-md-mscr/">Amanda Nelson</a>. I plan to defend in December 2023, and I am currently exploring opportunities to continue statistical and machine learning research in a governmental/industrial lab or postdoc environment.
        <br>
        Prior to starting my PhD, I was a data scientist in Cambridge, MA.
        Outside of my work, I love skiing, board games, cooking, and Crossfit.
    </p>
    <p>
        <h3>Research Interests</h3>
        I work on methods to help scientists understand the structure in high-dimensional and complex datasets, often motivated by the <a href="https://doi.org/10.1002/bimj.201300072">object-oriented data analysis</a> framework. This research includes statistics, machine learning, clustering, Bayesian methods, multivariate analysis, and data integration. 
    </p>
    <p>
        <h3>Teaching</h3>
        I've taught several courses at UNC and served as instructional assistant for others; please see <a href="{{ site.url }}/teaching">Teaching</a> for more.
    </p>
    <p>
        <h3>Recent News</h3>
        <table class="news">
        {% assign news = (site.data.news | sort: 'date') | reverse %} {% for n in news limit:5 %}
            <tr>
                <td class="date">{{ n.date | date_to_string }} </td> 
                <td class="description"> {{ n.description | markdownify }} </td>
            </tr>
        {% endfor %}
        </table>
        <a href="{{site.url}}/news.html">View All</a> <br>
    </p>
</div>
