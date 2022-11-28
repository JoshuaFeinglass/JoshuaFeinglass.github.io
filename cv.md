---
layout: cv
title: CV
permalink: cv/
jsarr:
- js/scripts.js
---

<h1><a style="color: #059; margin-left:0px" href="https://joshuafeinglass.com">Joshua Feinglass</a></h1>


<br/><span class="cv-max-width"> 
		I'm a 4th year PhD student in the <a href="https://yezhouyang.engineering.asu.edu/research-group/" style="color:#005599">ASU APG</a> lab advised by Yezhou Yang and working on <b>generalizable+robust</b> models and evaluations for the deployment of safe and reliable AI systems. More specifically, my thesis will focus on exploring novel representations of vision and language signals in order to improve and characterize <b>model performance in unfamiliar test domains</b> and identify and address <b>gameable aspects of well-established metrics</b>. 
</span>

<span class="cv-max-width">
		I am currently interning at <img class="intro-logo" style="width: 100px;" src="/images/logos/llnl.png">  Lawrence Livermore National Lab, where I am developing and publishing a State-of-the-Art and highly generalizable Zero-Shot Learning architecture with pre-trained vision pipelines, model regularization techniques, and automated external knowledge retrieval from natural language sources. I previously worked full-time as a Senior Digital Signal Processing Engineering at <img class="intro-logo" style="width: 100px;" src="/images/logos/gd.png"> General Dynamics where I primarily designed efficient algorithms for spectral decomposition, detection, characterization, and classification of communication and radar signals.
</span>

<div class="cv-image-links-wrapper" style="font-size: 16px; padding-bottom: 0;">
	<div class="cv-image-links">
		{% for link in site.data.social-links %}
			{% if link.cv-group == 1 %}
				{% include social-link.html link=link %}
			{% endif %}
		{% endfor %}
	</div>
	<div class="cv-image-links">
		{% for link in site.data.social-links %}
			{% if link.cv-group == 2 %}
				{% include social-link.html link=link %}
			{% endif %}
		{% endfor %}
	</div>
</div>


***


<h2><b><a style="color: #059">Education</a></b></h2>

{% for degree in site.data.education %}
{% include degree.html degree=degree %}
{% endfor %}


<h2><b><a style="color: #059">Work and Research Experience</a></b></h2>

{% for experience in site.data.experiences %}
{% if experience.type == 'industry' %}
{% include experience.html experience=experience %}
{% endif %}
{% endfor %}

<h2 id="publications"><b><a style="color: #059">Publications</a></b></h2>

{% for pub in site.data.publications %}
{% include publication.html pub=pub %}
{% endfor %}


<h2><b><a style="color: #059">Talks</a></b></h2>

{% assign talktitles = site.data.talks | group_by:"title" %}
{% for title in talktitles %}
{% include talk.html talk=title %}
{% endfor %}

[cv]: {{ site.url }}/cv.pdf "My CV."
