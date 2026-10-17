---
layout: page
title: Publications
permalink: /publications/
cover-image: gla-ucl-sketch.png
--- 
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

  <!-- 2. Clean up trailing ", no" if the split cut off at "no." -->
{% if venue_year contains ', no' %}
{% assign venue_year = venue_year | remove: ', no' | strip %}
{% endif %}

  <!-- 3. Extract External Link Safely -->
{% assign ext_link = "" %}
{% if post.content contains 'https://' %}
{% assign link_parts = post.content | split: 'https://' %}
{% assign candidate = link_parts[1] | split: ')' | first | split: ' ' | first | split: '"' | first | split: '<' | first %}
{% assign ext_link = candidate | prepend: 'https://' | strip %}
{% elsif post.content contains 'http://' %}
{% assign link_parts = post.content | split: 'http://' %}
{% assign candidate = link_parts[1] | split: ')' | first | split: ' ' | first | split: '"' | first | split: '<' | first %}
{% assign ext_link = candidate | prepend: 'http://' | strip %}
{% endif %}

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


