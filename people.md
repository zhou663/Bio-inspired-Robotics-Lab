---
title: People
---

<div class="container section">
  <h1>People</h1>
  <p>Update the <code>_data/people.yml</code> file to add or edit lab members.</p>
  <div class="people-grid">
    {% for person in site.data.people %}
    <div class="person">
      <img src="{{ person.photo }}" alt="{{ person.name }} photo" style="width:100%;border-radius:10px;border:1px solid var(--border);">
      <h3>{{ person.name }}</h3>
      <p class="role">{{ person.role }}</p>
      <p>{{ person.bio }}</p>
    </div>
    {% endfor %}
  </div>
</div>
