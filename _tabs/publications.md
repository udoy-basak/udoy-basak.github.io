---
title: Publications
icon: fas fa-book
order: 5
---
# Publications v1

{% assign publication_posts = site.posts | where_exp: "post", "post.categories contains 'Publications'" %}

{% assign publication_years = publication_posts | map: "date" | map: "year" | uniq | sort | reverse %}

{% for year in publication_years %}

## {{ year }}

{% for post in publication_posts %}
  {% if post.date | date: "%Y" == year %}

### [{{ post.title }}]({{ post.url | relative_url }})

{% if post.authors %}
**Authors:** {{ post.authors }}

{% endif %}
{% if post.journal %}
**Journal:** *{{ post.journal }}*

{% endif %}
{% if post.description %}
{{ post.description }}

{% endif %}

{% endif %}
{% endfor %}

{% endfor %}



# Publications v2

{% assign publication_posts = site.posts | where_exp: "post", "post.categories contains 'Publications'" %}

{% assign publication_years = "" | split: "" %}

{% for post in publication_posts %}
  {% assign year = post.date | date: "%Y" %}
  {% unless publication_years contains year %}
    {% assign publication_years = publication_years | push: year %}
  {% endunless %}
{% endfor %}

{% assign publication_years = publication_years | sort | reverse %}

{% for year in publication_years %}

## {{ year }}

{% for post in publication_posts %}
  {% assign post_year = post.date | date: "%Y" %}
  {% if post_year == year %}

### [{{ post.title }}]({{ post.url | relative_url }})

{% if post.authors %}
**Authors:** {{ post.authors }}  
{% endif %}

{% if post.journal %}
**Journal:** *{{ post.journal }}*  
{% endif %}

{% if post.volume %}
**Volume:** {{ post.volume }}  
{% endif %}

{% if post.pages %}
**Pages:** {{ post.pages }}  
{% endif %}

{% if post.description %}
{{ post.description }}
{% endif %}

{% endif %}
{% endfor %}

{% endfor %}











--------------------------------------------------------------
# Publications

My research publications are listed below.

# Publications and Presentations by Year




# Journal Publications by Year

## 2023

1. **SM Rayhanul Islam, U. S. Basak.** On traveling wave solutions with bifurcation analysis for the nonlinear potential Kadomtsev–Petviashvili and Calogero–Degasperis equations. *Partial Differential Equations in Applied Mathematics*, **8**, 100561 (2023).

2. **U. S. Basak, S. Sattari, Md. Motaleb Hossain, Kazuki Horikawa, Mikito Toda, T. Komatsuzaki.** Comparison of particle image velocimetry and the underlying agents dynamics in collectively moving self-propelled particles. *Scientific Reports*, **13**, 12566 (2023).

3. **Md. Ekramul Islam, M. M. Hossain, K. M. Helal, U. S. Basak, R. C. Bhowmik, M. A. Akbar.** Solitary wave analysis of the Kadomtsev–Petviashvili model in mathematical physics. *Arab Journal of Basic and Applied Sciences*, **30**(1), 329–340 (2023).

4. **U. S. Basak, Md. Ekramul Islam, S. Sattari.** Inferring interaction domains of collectively moving agents with varying radius of influence. *AIP Advances*, **13**, 035312 (2023).

## 2022

1. **S. Sattari, U. S. Basak, J. P. Crutchfield, T. Komatsuzaki.** Modes of information flow in collective cohesion. *Science Advances*, **8**(6), eabj1720 (2022).

## 2021

1. **U. S. Basak, S. Sattari, H. M. Motaleb, K. Horikawa, T. Komatsuzaki.** An information-theoretic approach to infer the underlying interaction domain among elements from finite length trajectories in a noisy environment. *The Journal of Chemical Physics*, **154**, 034901 (2021).

2. **U. S. Basak, S. Sattari, H. M. Motaleb, K. Horikawa, T. Komatsuzaki.** Transfer entropy dependent on distance among agents in quantifying leader-follower relationships. *Biophysics and Physicobiology*, **18**, 131–144 (2021).

## 2020

1. **U. S. Basak, S. Sattari, K. Horikawa, T. Komatsuzaki.** Inferring domain of interactions among particles from ensemble of trajectories. *Physical Review E*, **102**(1), 012404 (2020).


# Presentations

## Selected Contributed Talks by Year

### 2021

1. **Basak, U. S., Sattari, S., Hossain, M. M., Komatsuzaki, T.** Inferring domain of interactions among *Dictyostelium discoideum* colony from the ensembles of trajectories of cells. *Hokkaido-Tohoku Joint Meeting of Biophysics*, March 8, 2021 (Online).

### 2019

1. **Basak, U. S., Sattari, S., Komatsuzaki, T.** Identification of interaction distance of a group of collectively moving animals. *5th Hokkaido University Departmental Cross-Symposium*, November 6, 2019, Hokkaido University, Japan.

### 2018

1. **Basak, U. S., Sattari, S., Hossain, M. M., Komatsuzaki, T.** Identification of leader(s) in a *Dictyostelium discoideum* colony: An information-theoretic approach. *The Biophysics Hokkaido Branch Meeting*, organized by the Biophysical Society of Japan, Hokkaido University, Japan, 2018.

2. **Basak, U. S., Sattari, S., Hossain, M. M., Komatsuzaki, T.** Information-theoretic approach to identify the leader(s) in a *Dictyostelium discoideum* colony. *6th International LIFE-SCIENCE Symposium for Young Scientists*, Hokkaido University, Sapporo, Japan, November 19, 2018.


## Selected Poster Presentations by Year

### 2021

1. **U. S. Basak, S. Sattari, T. Komatsuzaki.** Information-theoretic approach to identify the leader(s) in a *Dictyostelium discoideum* colony. *4th Area Conference Poster Presentation Flash Talk*, March 4–5, 2021 (Online).

### 2020

1. **U. S. Basak, S. Sattari, M. M. Hossain, K. Horikawa, T. Komatsuzaki.** Quantifying the length- and time-scales of influence of cells in collective motion. *6th Annual Hokkaido University Cross-Departmental Symposium*, Hokkaido University, Sapporo, Japan, October 19, 2020.

2. **U. S. Basak, S. Sattari, M. M. Hossain, K. Horikawa, T. Komatsuzaki.** Quantifying the length- and time-scales of influence of cells in collective motion. *58th Annual Meeting of the Biophysical Society of Japan*, Online, September 18, 2020.

### 2019

1. **U. S. Basak, S. Sattari, S. Nicholson, J. Green, M. Toda, T. Komatsuzaki.** A sandbox model system for understanding leadership in collective motion. *20th RIES-HOKUDAI International Symposium*, Hokkaido University Conference Hall, Sapporo, Japan, December 2, 2019.

2. **U. S. Basak, S. Sattari, M. M. Hossain, T. Komatsuzaki.** An information-theoretic approach toward identifying the leader(s) and aggregation place in *Dictyostelium discoideum* colony. *57th Annual Meeting of the Biophysical Society of Japan (BSJ2019)*, Miyazaki, Japan.

3. **U. S. Basak, S. Sattari, S. Nicholson, M. Toda, J. Green, T. Komatsuzaki.** A leadership-based phase transition in a flocking model with activated and un-activated agents. *57th Annual Meeting of the Biophysical Society of Japan*, Seagaia Convention Center, Miyazaki, Japan, September 25, 2019.

### 2018

1. **U. S. Basak, S. Sattari, S. Nicholson, J. Green, M. Toda, T. Komatsuzaki.** A sandbox model system for understanding leadership in collective motion. *Study Group, Theory and Experiment, 19th RIES-HOKUDAI International Symposium*, Jozankei View Hotel, Sapporo, Japan, December 11, 2018.
