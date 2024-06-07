---
layout: page
title: Publications
---

{% for year in (2018...2024) reversed %}

{% assign pub_year = site.data.publications | where: "year", year %}

{% if pub_year.size > 0 %}


<h2>{{year}} </h2>

{% assign types = "Journal Articles, Conference Articles, Thesis, Conference Talks" | split: ", " %}
{% for type in types %}
{% assign pub_type = pub_year | where: "type", type %}

{% if pub_type.size > 0 %}

<h3>{{type}}</h3>

{% for pub in pub_type %}

<div class="container">
	<a href="{{pub.site}}" target="_blank" class="imglink">
		<img src="assets/thumbnails/{{pub.thumbnail}}" alt="{{pub.thumbnail}}" class="thumbnail"/>
	</a>
	<div>
		<p class="pubtext"><a href="{{pub.site}}" target="_blank"><strong>{{pub.title}}</strong></a></p>
		<p class="pubtext">{{pub.authors}}</p>
		<p class="pubtext"><em>{{pub.journal}}</em></p>
		{% if pub.distinction != "none" %}
			<p class="pubtext"><b>{{pub.distinction}}</b></p>
		{% endif %}
		<div class="pubtext, container">
			{% for link in pub.links %}
			<a class="button" href="{{link.link}}" target="_blank">
				<span>
					{{link.name}}
				</span>
			</a>
			{% endfor %}
		</div>
	</div>
</div>

<br/>

{% endfor %}


{% endif %}
{% endfor %}
{% endif %}
{% endfor %}