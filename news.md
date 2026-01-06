---
title: News & Media
---

<div class="container section">
  <h1>News &amp; Media</h1>
  <p>Edit <code>_data/news.yml</code> to keep this feed current. Each item accepts <code>description</code> and <code>link</code> (YouTube URLs supported).</p>
  <ul class="list">
    {% for item in site.data.news %}
    <li>
      <p>{{ item.description }}</p>
      {% if item.link %}<a href="{{ item.link }}" target="_blank" rel="noopener">Watch video</a>{% endif %}
    </li>
    {% endfor %}
  </ul>
</div>
