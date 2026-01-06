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
      {% if item.link %}
      {% assign embed_url = item.link
        | replace: 'https://youtu.be/', 'https://www.youtube.com/embed/'
        | replace: 'http://youtu.be/', 'https://www.youtube.com/embed/'
        | replace: 'https://youtube.com/shorts/', 'https://www.youtube.com/embed/'
        | replace: 'https://www.youtube.com/shorts/', 'https://www.youtube.com/embed/'
        | replace: 'watch?v=', 'embed/'
        | replace: '&', '?' %}
      <div class="news-video">
        <iframe src="{{ embed_url }}" title="{{ item.description }}" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>
      {% endif %}
    </li>
    {% endfor %}
  </ul>
</div>
