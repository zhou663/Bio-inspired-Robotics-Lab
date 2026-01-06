---
title: Publications
---

<div class="container section">
  <h1>Publications</h1>
  <p>Update <code>_data/publications.yml</code> with your latest papers. Each entry shows the title, authors, venue, and tags.</p>
  <ul class="list">
    {% for pub in site.data.publications %}
    <li>
      <h3><a href="{{ pub.link }}" target="_blank" rel="noopener">{{ pub.title }}</a></h3>
      <p>{{ pub.authors }}</p>
      <p>{{ pub.venue }}</p>
      <div class="tag-list">
        {% for tag in pub.tags %}
        <span class="tag">{{ tag }}</span>
        {% endfor %}
      </div>
      <p>{{ pub.summary }}</p>
    </li>
    {% endfor %}
  </ul>
</div>
