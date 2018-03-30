---
layout: default
---

# $ cat about.txt
{:id="about"}

We're a couple of friends who like to do hackathons.  [Our Github](https://github.com/aquatints).

# $ cat contact.txt
{:id="contact"}

Contact Pat: [s3cpat](https://s3c.ninja).

# $ cat team.txt
{:id="team"}
<ul>
	<li>Pat</li>
	<li>Ryan</li>
	<li>Wen</li>
</ul>

<ul>
{% for member in site.categories.team reversed %}
<li id="{{ member.title }}">{{ member.title }}
<ul>
<li>{{ member.mail }}</li>
<li><a href="https://github.com/{{ member.github }}">https://github.com/{{ member.github }}</a></li>
<li><a href="{{ member.site }}">{{ member.site }}</a></li>
</ul>
</li>
{% endfor %}
</ul>

# $ cat projects.txt
{:id="projects"}

<ul>
{% for project in site.categories.projects %}
<li><a href="{{ project.link }}">{{ project.title }}</a> - {{ project.description }}</li>
{% endfor %}
</ul>

# $ cat posts.txt
{:id="posts"}

<ul>
{% for post in site.categories.posts %}

{% if post.en %}
<li>{{ post.title }} :: <a href="{{ post.url }}" title="{{ post.description }}">en</a></li>
{% endif %}

{% endfor %}
</ul>

