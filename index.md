---
layout: cv
title: Home
---

<div style="font-size: 40px; font-family: Lato, Arial" class="intro-title"><b>Joshua Feinglass</b></div>
<hr style="margin-left: 0; margin-top:0">

<div class="intro">
	<div class="intro-image">
		<img src="/images/prof_pic.png" style="border-radius: 2px;">

		<div class="intro-image-links" style="margin-left:0px; margin-top:5px">
			{% for link in site.data.social-links %}
			{% if link.on-homepage == true %}
			{% include social-link.html link=link %}
			{% endif %}
			{% endfor %}
		</div>
	</div>



	<div class="intro-text">
	<p markdown="1" style="font-size: 14pt; padding-left:0rem">
		I'm a 5th year PhD student developing <b>generalizable</b> and <b>robust</b> models to ensure the deployment of safe and reliable AI systems.
	</p>
	<p markdown="1" style="font-size: 14pt; padding-left:0rem">
		I work in the <a href="https://yezhouyang.engineering.asu.edu/research-group/" style="color:#005599">ASU APG</a> lab where I'm advised by Yezhou Yang. I recently interned at <img class="intro-logo" style="width: 25px;" src="/images/logos/ms.png">  Microsoft Research, where I developed novel datasets, machine learning models, and benchmarks for forecasting and analyzing cybersecurity incident escalation, and <img class="intro-logo" style="width: 25px;" src="/images/logos/llnl.png">  Lawrence Livermore National Lab, where I developed a novel zero-shot deep learning architecture using image and natural language data sources. Prior to pursuing my Signal Processing/Machine Learning specialized Master's degree in 2016, I also interned for two summers at <img class="intro-logo" style="width: 75px;" src="/images/logos/honeywell.png"> Honeywell where I worked on web development, test automation scripts, electrical component diagrams, and hardware programming.
	</p>
	<p markdown="1" style="font-size: 14pt; padding-left:0rem">
		After recieving my Master's degree, I worked full-time as a Senior Digital Signal Processing Engineering at <img class="intro-logo" style="width: 25px;" src="/images/logos/gd.png"> General Dynamics where I designed algorithms for spectral decomposition, detection, characterization, and classification of communication and radar signals before pursing my PhD.
    </p>
 	</div>

</div>

<div style="padding-top: 30px;font-size: 25px; font-family: Lato, Arial; color: #059;" class="intro-title"><b>News</b></div>
<hr style="margin-left: 0; margin-top:0">

{% for award in site.data.news %}
{% if award.featured == true %}
{% include news.html award=award %}
{% endif %}
{% endfor %}

<div style="padding-top: 50px;font-size: 25px; font-family: Lato, Arial; color: #059;" class="intro-title"><b>Research Highlights</b></div>
<hr style="margin-left: 0; margin-top:0">

<div class="cover-wrapper">
{% assign sortedPublications = site.data.publications | sort: 'feature-order' %}
{% for feature in sortedPublications %}
{% if feature.featured == true %}

{% include feature.html feature=feature %}

{% endif %}
{% endfor %}
</div>

<div style="padding-top: 30px;font-size: 25px; font-family: Lato, Arial; color: #059;" class="intro-title"><b>Education</b></div>
<hr style="margin-left: 0; margin-top:0">

{% for degree in site.data.education %}
{% include degree.html degree=degree %}
{% endfor %}

<div style="padding-top: 30px;font-size: 25px; font-family: Lato, Arial; color: #059;" class="intro-title"><b>Work and Research Experience</b></div>
<hr style="margin-left: 0; margin-top:0">
{% for experience in site.data.experiences %}
{% if experience.type == 'industry' %}
{% include experience.html experience=experience %}
{% endif %}
{% endfor %}



<div style="padding-top: 30px;font-size: 25px; font-family: Lato, Arial; color: #059;" class="intro-title"><b>Publications</b></div>
<hr style="margin-left: 0; margin-top:0">
{% for pub in site.data.publications %}
{% include publication.html pub=pub %}
{% endfor %}
