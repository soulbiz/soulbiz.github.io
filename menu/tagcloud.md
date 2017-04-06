---
layout: page
title: TagCloud
---

<div>
  {% include tag-cloud.html %}
  
  {% assign sorted-tags = site.tags | sort %}
  
  <div class="tags-postlist">
    {% for tag in sorted-tags %}
    <h2 id="{{ tag[0] | slugify }}">{{ tag[0] }}</h2>
    
    <ul>
      {% for post in tag[1] %}
        <a class="tag-post" href="{{ site.baseurl }}{{ post.url }}">
		  <li>
			{{ post.title }}
		  <small class="post-date">{{ post.date | date_to_string }}</small>
		  </li>
        </a>
      {% endfor %}
    </ul>
    
    {% endfor %}
  </div>
</div>
