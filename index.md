---
title: WELCOME
layout: main
mailTitle: General questions
---

# Welcome to the *AllebiGames* web portal!
We're just a humble indie game developers who tries to bring useful game-templates for you. <br>
Since 2011 we're here for hundreds of customers and hope to become your reliable partner too!<br>
*Help/support customers is always our highest priority, so please don't hesitate to contact us!*

You can check our main assets using theis site menu or directly on [Unity Asset Store](https://assetstore.unity.com/publishers/757)

<br>

## If you need any help:
Please mail us:  <a href="mailto:AllebiGames@gmail.com?subject={{ page.mailTitle }}"> AllebiGames@gmail.com </a>
<br>
**_We'll try to respond as soon as possible, but please note - it can take up to 48h_**
<div align="right">  
Sincerelly  <br> 
<img src="assets/images/allebi_logo_sm.png" alt="drawing" width="100"/>
</div>


* * *
# News feed:

 {% if site.paginate %}
    {% assign posts = paginator.posts %}
  {% else %}
    {% assign posts = site.posts %}
  {% endif %}


  {%- if posts.size > 0 -%}
    {%- if page.list_title -%}
      <h2 class="post-list-heading">{{ page.list_title }}</h2>
    {%- endif -%}
    <ul class="post-list">
      {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
      {%- for post in posts -%}
      <li>
        <span class="post-meta">{{ post.date | date: date_format }}</span>
        <h3>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
        {%- if site.show_excerpts -%}
          {{ post.excerpt }}
        {%- endif -%}
      </li>
      {%- endfor -%}
    </ul>

    {% if site.paginate %}
      <div class="pager">
        <ul class="pagination">
        {%- if paginator.previous_page %}
          <li><a href="{{ paginator.previous_page_path | relative_url }}" class="previous-page">{{ paginator.previous_page }}</a></li>
        {%- else %}
          <li><div class="pager-edge">•</div></li>
        {%- endif %}
          <li><div class="current-page">{{ paginator.page }}</div></li>
        {%- if paginator.next_page %}
          <li><a href="{{ paginator.next_page_path | relative_url }}" class="next-page">{{ paginator.next_page }}</a></li>
        {%- else %}
          <li><div class="pager-edge">•</div></li>
        {%- endif %}
        </ul>
      </div>
    {%- endif %}

  {%- endif -%}
