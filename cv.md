---
layout: cv
title: CV
permalink: cv/
jsarr:
- js/scripts.js
---

<h1><a style="color: #059; margin-left:0px" href="https://joshuafeinglass.com">Joshua Feinglass</a></h1>


<br/><span class="cv-max-width"> 
		I'm a Founder and Principal Investigator at Green Squirrel Research developing <b>generalizable</b> and <b>robust</b> models for the deployment of safe and reliable AI systems. I received my PhD in Computing Engineering (specialized in Machine Learning) from Arizona State University in December 2024.
</span>

<span class="cv-max-width">
		During my PhD studies, I worked in the <a href="https://yezhouyang.engineering.asu.edu/research-group/" style="color:#005599">ASU APG</a> lab where I was advised by Yezhou Yang. I interned at <img class="intro-logo" style="width: 25px;" src="/images/logos/ms.png">  Microsoft Research, where I developed novel datasets, machine learning models, and benchmarks for forecasting and analyzing cybersecurity incident escalation, and <img class="intro-logo" style="width: 25px;" src="/images/logos/llnl.png">  Lawrence Livermore National Lab, where I developed a novel zero-shot deep learning architecture using image and natural language data sources. Prior to pursuing my Signal Processing/Machine Learning specialized Master's degree in 2016, I also interned for two summers at <img class="intro-logo" style="width: 75px;" src="/images/logos/honeywell.png"> Honeywell where I worked on web development, test automation scripts, electrical component diagrams, and hardware programming.
</span>

<span class="cv-max-width">
		After receiving my Master's degree, I worked full-time as a Senior Digital Signal Processing Engineering at <img class="intro-logo" style="width: 25px;" src="/images/logos/gd.png"> General Dynamics where I designed algorithms for spectral decomposition, detection, characterization, and classification of communication and radar signals before pursing my PhD.
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
