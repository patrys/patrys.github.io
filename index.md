---
layout: splash
title: Room 303
tagline: Bug to the Feature
---
{% include JB/setup %}

<h2>Ostatnio opublikowane</h2>

<div class="row">
	<div class="col-sm-12">
		{% assign post = site.posts | first %}
		<h3><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h3>
		<p><span class="label label-default">{{ post.date | date_to_string }}</span></p>
		{{ post.excerpt }}
	</div>
</div>

<div class="row">
{% for post in site.posts limit:20 offset:1 %}
<div class="col-sm-6">
	<h3><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h3>
	<p><span class="label label-default">{{ post.date | date_to_string }}</span></p>
</div>
{% endfor %}
</div>