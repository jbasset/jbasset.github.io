---
layout: page
title: Publications
---

{% for year in (2018...2023) reversed %}

<h1> {{year}} </h1>

{% for pub in site.data.publications %}
{% if pub.year == year %}

<div class="container">
	<a href="{{pub.site}}" target="_blank" class="imglink">
		<img src="assets/thumbnails/{{pub.thumbnail}}" alt="{{pub.thumbnail}}" width=200 class="thumbnail"/>
	</a>
	<div>
		<p class="pubtext"><a href="{{pub.site}}" target="_blank"><strong>{{pub.title}}</strong></a></p>
		<p class="pubtext">{{pub.authors}}</p>
		<p class="pubtext"><em>{{pub.journal}}</em></p>
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

{% endif %}
{% endfor %}
{% endfor %}