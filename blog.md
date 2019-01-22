
<ul>
  {% for post in site.posts %}
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <small style="color: hotpink;">{{ post.author }} on {{ post.date | date_to_string }}</small>
    <p>
      {{ post.excerpt }}
    </p>
  {% endfor %}
</ul>

