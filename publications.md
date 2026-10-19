---
layout: page
title: Publications
permalink: /publications/
cover-image: gla-ucl-sketch.png
--- 

### Selected publications
<div class="selectedPub">
<ul class="grid-list" style="grid-template-columns: repeat(auto-fill, minmax(330px, 1fr));">
{% for post in site.categories.selected limit:10 %}
  {% assign clean_text = post.content | strip_html | strip %}

{% assign pub_title = nil %}
{% assign venue_year = nil %}

  <!-- 1. Extract Title -->
{% if clean_text contains '"' %}
{% assign parts = clean_text | split: '"' %}
{% assign pub_title = parts[1] %}
{% assign remainder = parts[2] | split: '.' %}
{% assign venue_year = remainder[0] | strip %}
{% elsif clean_text contains '“' %}
{% assign parts = clean_text | split: '“' %}
{% assign sub_parts = parts[1] | split: '”' %}
{% assign pub_title = sub_parts[0] %}
{% assign remainder = sub_parts[1] | split: '.' %}
{% assign venue_year = remainder[0] | strip %}
{% endif %}

{% unless pub_title %}
{% assign pub_title = post.title %}
{% endunless %}

  <!-- 2. Clean up trailing ", no" -->
{% if venue_year contains ', no' %}
{% assign venue_year = venue_year | remove: ', no' | strip %}
{% endif %}

  <!-- 3. Robust External Link Extraction -->
{% assign ext_link = "" %}
{% if post.content contains 'https://' %}
{% assign link_chunks = post.content | split: 'https://' %}
{% for chunk in link_chunks %}
{% if forloop.first %}{% continue %}{% endif %}
<!-- Clean up common trailing markdown/HTML symbols -->
{% assign raw_candidate = chunk | split: '"' | first | split: "'" | first | split: '>' | first | split: ']' | first | strip %}
<!-- If it's a valid URL chunk, capture it and break -->
{% if ext_link == "" and raw_candidate != "" %}
{% assign ext_link = raw_candidate | prepend: 'https://' %}
{% endif %}
{% endfor %}
{% elsif post.content contains 'http://' %}
{% assign link_chunks = post.content | split: 'http://' %}
{% for chunk in link_chunks %}
{% if forloop.first %}{% continue %}{% endif %}
{% assign raw_candidate = chunk | split: '"' | first | split: "'" | first | split: '>' | first | split: ']' | first | strip %}
{% if ext_link == "" and raw_candidate != "" %}
{% assign ext_link = raw_candidate | prepend: 'http://' %}
{% endif %}
{% endfor %}
{% endif %}

  <!-- Fallback only if absolutely no link was found -->
{% if ext_link == "" %}
{% assign ext_link = post.url %}
{% endif %}

  <li>
    <h3>
      <a href="{{ ext_link }}" target="_blank" rel="noopener noreferrer">{{ pub_title }}</a>
    </h3>
    {% if venue_year %}
      <p class="pub-venue">{{ venue_year }}</p>
    {% endif %}
  </li>
{% endfor %}
</ul>
</div>

### recent publications (2017 ~)
{% for post in site.categories.paper %}

{% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}

{% assign prev = post %}
{% for p in site.categories.paper %}
   {% if p.title == post.title %}
    {% break %}
   {% endif %}   
   {% assign prev = p %}
{% endfor %}
{% capture next_year %}{{ prev.date | date: "%Y" }}{% endcapture %}

{% if forloop.first %}
### {{this_year}} 
{% endif %}

{% if forloop.last %}

{% else %}
   {% if this_year != next_year %}
### {{this_year}}
   {% endif %}
{% endif %}
- {{post.content}}
{% endfor %}


