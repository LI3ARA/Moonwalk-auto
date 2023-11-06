---
layout: post
title: "Projects"
description: 'Innovate, Create, Repeat: My Project Journey'
image: assets/images/pic01.jpg
nav-menu: true
order: 3
---
<!-- Main -->

<div id="main">

<!-- One -->

<!-- <section id="one">
	<div class="inner">
		<header class="major">
			<h2>Sed amet aliquam</h2>
		</header>
		<p>Nullam et orci eu lorem consequat tincidunt vivamus et sagittis magna sed nunc rhoncus condimentum sem. In efficitur ligula tate urna. Maecenas massa vel lacinia pellentesque lorem ipsum dolor. Nullam et orci eu lorem consequat tincidunt. Vivamus et sagittis libero. Nullam et orci eu lorem consequat tincidunt vivamus et sagittis magna sed nunc rhoncus condimentum sem. In efficitur ligula tate urna.</p>
	</div>
</section> -->

<!-- Two -->

<section id="two" class="spotlights">
	<ul class="horizontal-list">
	{% for post in site.posts %}
		{% if post.type == 'projects' %}
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
