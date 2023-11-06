---
title: Achievements
layout: post
description: 'Achieve, Believe, Succeed: My Success Story'
image: assets/images/pic05.jpg
nav-menu: true
order: 5
---
<!-- Main -->

<div id="main">

<section id="two" class="spotlights">
	<ul class="horizontal-list">
	{% for post in site.posts %}
		{% if post.type == 'archievement' %}
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
