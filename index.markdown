---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: Home
---

<div class="container">
	<div>
		<h2>About Me</h2>
		I am a PostDoc in the <a href="https://manao.inria.fr/" target="_blank">Manao</a> team at <a href="https://www.inria.fr/fr/centre-inria-universite-bordeaux" target="_blank">Inria Bordeaux</a>, working in Computer Graphics and Animation with <a href="https://www.labri.fr/perso/pbenard/index.html" target="_blank">Pierre Benard</a> in the <a href="https://mostyle.github.io/" target="_blank">MoStyle</a> project.
		I previously obtained my Ph.D. from the <a href="https://edmstii.univ-grenoble-alpes.fr/" target="_blank">MSTII</a> doctoral school in june 2022, under the supervision of <a href="https://swuhrer.gitlabpages.inria.fr/website/" target="_blank">Stefanie Wuhrer</a>, <a href="https://morpheo.inrialpes.fr/people/Boyer/" target="_blank">Edmond Boyer</a> and <a href="https://perso.univ-rennes2.fr/franck.multon" target="_blank">Franck Multon</a>, within Inria teams <a href="https://team.inria.fr/morpheo/" target="_blank">Morpheo</a> (Grenoble) and <a href="https://team.inria.fr/mimetic/#" target="_blank">Mimetic</a> (Rennes).
	</div>
	<div>
		<img class="profileimg" src="assets/profile.jpg">
	</div>

</div>

## Research Interests

I am currently working on 3D animation stylization. My focus is on stylization of the geometry and motion of 3D animations in order to recreate traditional 2D animation effects. I am also interested in perception of animations by observers. During my Ph.D. thesis, I worked on transfer of animations between characters, focusing on morphologically and perceptually plausible deformations. In earlier projects, I worked on human computer interaction in virtual and mixed reality environments.

## News

<ul>
{% for post in site.posts %}
{% if post.news and post.recent%}
<li>
{{ post.excerpt }}
</li>
{% endif %}
{% endfor %}
</ul>