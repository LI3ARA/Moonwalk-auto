---
layout: post
title: Publications
description: 'Data Whisperer: My Quest for AI Excellence'
image: assets/images/pic03.jpg
nav-menu: true
order: 2
---
<!-- Main -->

<div id="main">
<!-- Two -->
<section id="two" class="spotlights">
	<ul class="horizontal-list">
	{% for post in site.posts %}
		{% if post.type == 'publication' %}
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
