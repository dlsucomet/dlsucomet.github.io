---
layout: page
permalink: /people/
title: People
---

<div class="people-wrapper">
    {% for person in site.data.people %}
        <div class="person">
            {% if person.website %}
                <a href="{{ person.website }}">
            {% endif %}
                    <img class="person-pic" src="{{ person.pic }}">
            {% if person.website %}
                </a>
            {% endif %}
            <p>{{ person.nickname }}</p>
        </div>
    {% endfor %}
</div>

<h4 class="section-header">Alumni</h4>
<div class="alumni-wrapper">
    {% for alum in site.data.alumni %}
        <p>{{ alum.first }} {{ alum.last }}</p>
    {% endfor %}
</div>