---
layout: page
title: offical blogs
tagline: fly your dream
---
{% include JB/setup %}
# fly your dreams here
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
		<a href="{{ BASE_PATH }}{{ post.url }}">&hellip;MORE DETAILS</a>
	</div>
	
</div>
<hr>
{% endfor %}

