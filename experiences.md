---
title: Experience
layout: post
description: 'From Intern to Expert: My Professional Evolution'
image: assets/images/pic04.jpg
nav-menu: true
order: 4
---
<!-- Main -->

<div id="main">

<!-- Two -->

<section id="two" class="spotlights">
	<ul class="horizontal-list">
	{% for post in site.posts %}
		{% if post.type == 'experience' %}
			<li class="card">
				<a href="{{ site.baseurl }}{{ post.url }}" class="image">
				<span class="header">
					{{ post.title }}
					{% if post.highlight %}
						<mark>{{ post.highlight }}</mark>
					{% endif %}
				</span>		
				<hr />
				<p class="body">
					{{ post.description }}
				</p>
				</a>
			</li>
		{% endif %}
	{% endfor %}
	</ul>
</section>

</div>
