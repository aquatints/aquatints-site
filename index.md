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
<ul><hr>
	<li>Pat
	<br>
	Pat Heaney is a Junior at the Pennsylvania State University. He is pursuing a B.S. in Security and Risk Analysis at the College of Information Sciences and Technology with a focus in Information & Cybersecurity (ICS).
	<br>
	</li>
<hr>	
	<li>Ryan
	<br>
	Ryan Dougherty is a Junior at the Pennsylvania State University. He is pursuing a B.S. in Information and Science Technology at the College of Information Sciences and Technology with a focus in Design and Development of Applications.
	<br>
	</li>
<hr>
	<li>Wen
	<br>
	Wendy Davis is a Junior at Penn State majoring in Wildlife and Fisheries Science with a focus on wildlife stuides.
	<br>
	</li>
<hr>
	<li>Anthony
	<br>
	Anthony is a Junior at the Pennsylvania State University. He is pursuing a B.S. in Security and Risk Analysis at the College of Information Sciences and Technology with a focus in Information & Cybersecurity (ICS).
	<br>
	</li>
<hr></ul>

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

