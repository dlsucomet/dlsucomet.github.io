---
layout: page
permalink: /people/
title: People
---

<div class="people-wrapper">
    {% for person in site.data.people %}
    <span style="display:none">{% increment people_count %}</span>
        <div class="person">
            <img class="person-pic" src="{{ person.pic }}" alt="Photo of {{ person.nickname }}">
            {% if person.website %}
            <a href="{{ person.website }}" target="_blank">
            {% endif %}
                <div class="person-details {{ person.type }}" id="{{ people_count }}" onmouseover="show({{ people_count }});" onmouseout="hide({{ people_count }});">
                    <p class="nickname is-visible">{{ person.nickname }}</p>
                    <div class="details">
                        <p class="details-fullname">{{ person.first }}&nbsp;{{ person.last }}</p>
                        {% if person.type == "Faculty" %}<p>{{ person.role }}</p>{% endif %}
                        <p>{{ person.program }}</p>
                    </div>
                </div>
            {% if person.website %}
            </a>
            {% endif %}
        </div>
    {% endfor %}
</div>

<h4 class="section-header">Alumni</h4>
<div class="alumni-wrapper">
    {% for alum in site.data.alumni %}
        <p>{{ alum.first }} {{ alum.last }}</p>
    {% endfor %}
</div>

<script>
    function show(element) {
        console.log(element);
        var person = document.getElementById(element);
        var details = person.getElementsByClassName("details");
        var nickname = person.getElementsByClassName("nickname");
 
        person.classList.add("is-visible");
        details[0].classList.add("is-visible");
        nickname[0].classList.remove("is-visible");
    }
    
    function hide(element) {
        var person = document.getElementById(element);
        var details = person.getElementsByClassName("details");
        var nickname = person.getElementsByClassName("nickname");
 
        person.classList.remove("is-visible");
        details[0].classList.remove("is-visible");
        nickname[0].classList.add("is-visible");
    }
</script>