---
layout: default
title: "Publications"
permalink: /publication
---

{%- assign alldocs = site.publications -%}
   {% for post in alldocs %} 
<div class="col-12 mb-2">
<div class="card chulapa-border-card-index">
	<div class="row g-0">
		<a {% if post.doi %} href="{{- post.doi -}}"{% endif %} class="col-sm-1 chulapa-min-h-10 chulapa-card-img chulapa-overlay-img chulapa-gradient {% if post.header_img == nil or post.og_image -%} d-none d-sm-flex {% endif %} ">
		</a>
		<div class="col-sm">
			<article class="card-body chulapa-links-hover-only">
				<a href="{{- post.url | absolute_url -}}"><h5 class="card-title">{{- post.title  | default: "---" -}}</h5></a>
			  <h6 class="card-subtitle mb-2 text-muted">{{- post.authors -}}</h6>
				
{%- assign fallbackdesc = post.abstract | 
              markdownify |  newline_to_br | 
              replace:"<br />", ",.," | 
              replace:"{{", ",.," | 
              replace:"{%", ",.," | 
              split: ",.," | first -%}
				<div class="card-text">{{- post.excerpt | default: fallbackdesc | strip_html | 
              escape_once -}}
				</div>
			</article>
			{% if post.date %}
			<div class="border-top-0 card-footer border-primary chulapa-bg-transparent">
				{% if post.date -%}<p class="small text-right font-italic mb-1">
<time datetime="{{- post.date | date_to_xmlschema -}}">{{- post.date | date: "%d/%m/%Y"  -}}</time></p>{%- endif %}
				</div>
			{% endif %}
		</div>
	</div>
</div>
</div>
{% endfor %}