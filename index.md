---
layout: default
home: true
---

{% include_relative info.md %}

<div class="h_title">Latest news | <a href="/updates/">all updates</a></div>

<img src="img/announcement.png" width="30" style="float:left">&nbsp;&nbsp;**We are hiring a postdocral researcher on Clinical AI and Health Equity. Check [job advert](https://www.ucl.ac.uk/work-at-ucl/search-ucl-jobs/details?nPostingId=14329&nPostingTargetId=35063&id=Q1KFK026203F3VBQBLO8M8M07&LG=UK&languageSelect=UK&mask=ext).**

{% for post in site.categories.news limit:5%}

{% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
{% capture next_year %}{{ post.previous.date | date: "%Y" }}{% endcapture %}

{% if forloop.first %}
### {{this_year}}
{% endif %}

- ({{ post.date | date: "%-d %B %Y"}}) {% if post.related_image %}
  <img src="{{post.related_image}}" width="700px" style="filter: drop-shadow(0.35rem 0.35rem 0.4rem rgba(0, 0, 0, 0.3)); margin-bottom:20px"/>
  {% endif %}  {{ post.title }} {% if post.categories contains 'events'%}
  <a href="{{ post.url }}">Event Details</a>
  {% endif %} 
 <hr style="text-align: center"/>
{% if forloop.last %}

{% else %}
    {% if this_year != next_year %}
### {{next_year}}
    {% endif %}
{% endif %}
{% endfor %}


<div style="color: #999999;margin:60px 0 20px 0;font-style: italic;text-align: center;font-size: 90%">Acknowledgement: Logo designed by Yuchen Wu</div>
