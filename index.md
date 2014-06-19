---
layout: page
title: RC Zone - a worldwide funny rc model zone
tagline: fly your dream
---
{% include JB/setup %}
# Fly Your Dream, Overlooks The World.
---


{% for post in site.posts %}
<div class = "card">
	<div class = "clearfix">
		<div  class = "date_label">
			<div class="day_month">
      			{{ post.date | date:"%m/%d" }}
      			</div>
      			<div class="year">
      			{{ post.date | date:"%Y" }}
      			</div>
      		</div> 
	</div>
		{{ post.content  | | split:'<!--break-->' | first }}
	<div class = "read_more">
		<a href="{{ BASE_PATH }}{{ post.url }}">&hellip;More</a>
	</div>
	
</div>
<hr>
{% endfor %}

