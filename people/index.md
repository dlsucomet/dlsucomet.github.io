---
layout: page
permalink: /people/
title: People
---

<h3 class="section-header">Faculty</h3>
<div class="people-wrapper">
    {% for person in site.data.faculty %}
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

<h3 class="section-header">Affiliates</h3>
<div class="people-wrapper">
    {% for person in site.data.affiliates %}
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

<h3 class="section-header">Graduate Students</h3>
<div class="people-wrapper">
    {% for person in site.data.graduates %}
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

<h3 class="section-header">Undergraduate Students</h3>
<div class="people-wrapper">
    {% for person in site.data.undergraduates %}
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

<h3 class="section-header">Service Teams</h3>
<div class="team-wrapper service-teams">
    {% for team in site.data.service %}
    <div>
        <h4 class="section-header">{{ team.name }}</h4>
        <div class="people-wrapper">
            {% for member in team.members %}
                <span style="display:none">{% increment people_count %}</span>
                <div class="person">
                    <img class="person-pic" src="{{ member.pic }}" alt="Photo of {{ member.name }}">
                    <div class="person-details {{ member.type }}" id="{{ people_count }}" onmouseover="show({{ people_count }});" onmouseout="hide({{ people_count }});">
                        <p class="nickname is-visible">{{ member.nickname }}</p>
                        <div class="details">
                            <p class="details-fullname">{{ member.name }}</p>
                            {% if member.role %}<p>{{ member.role }}</p>{% endif %}
                            {% if member.subject %}<p>{{ member.subject }}</p>{% endif %}
                        </div>
                    </div>
                </div>
            {% endfor %}
        </div>
    </div>
    {% endfor %}
</div>

<h3 class="section-header">Alumni</h3>
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