---
layout: cv
title: Home
---

<div style="font-size: 40px; font-family: Lato, Arial" class="intro-title"><b>Joshua Feinglass</b></div>
<hr style="margin-left: 0; margin-top:0">

<div class="intro">
	<div class="intro-image">
		<img src="/images/prof_pic.jpg" style="border-radius: 2px;">

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
		I'm a 4th year PhD student in the <a href="https://yezhouyang.engineering.asu.edu/research-group/" style="color:#005599">ASU APG</a> lab advised by Yezhou Yang and working on <b>generalizable+robust</b> models and evaluations for the deployment of safe and reliable AI systems. More specifically, my thesis will focus on exploring novel representations of vision and language signals in order to improve and characterize <b>model performance in unfamiliar test domains</b> and identify and address <b>gameable aspects of well-established metrics</b>. 
	</p>
	<p markdown="1" style="font-size: 14pt; padding-left:0rem">
		I am currently interning at <img class="intro-logo" style="width: 100px;" src="/images/logos/llnl.png">  Lawrence Livermore National Lab, where I am developing and publishing a State-of-the-Art and highly generalizable Zero-Shot Learning architecture with pre-trained vision pipelines, model regularization techniques, and automated external knowledge retrieval from natural language sources. I previously worked full-time as a Senior Digital Signal Processing Engineering at <img class="intro-logo" style="width: 100px;" src="/images/logos/gd.png"> General Dynamics where I primarily designed efficient algorithms for spectral decomposition, detection, characterization, and classification of communication and radar signals.
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
