---
layout: main
---

<div class="abstract">
    <p class="abstract-overview">
        The Center for Complexity and Emerging Technologies (COMET) is an interdisciplinary research laboratory under the Advanced Research Institute for Informatics, Computing, and Networking (AdRIC) at <a href="https://www.dlsu.edu.ph" target="_blank">De La Salle University</a>. Our mission is to enhance our understanding of <span class="about-highlight">emergent phenomena in real-life systems (i.e. cities, mobility), sociotechnical systems (i.e. social networking sites, Wikipedia), and human-computer interactions</span>. We develop computational models which are then used in the design of interactive tools, information systems, and interaction techniques.
    </p>
    <div class="recent-pubs-header">
        <h4>Recent Publications</h4>
        <a href="/papers/"><span>View all</span><i class="fas fa-angle-double-right"></i></a>
    </div>
    <div class="recent-pubs">
    {% for conf in site.data.feature %}
        <p class="conf-name">{{ conf.conf }}</p>
        {% assign researches = site.data.publications | where:"name", conf.year | first %}
        <div class="projects">
        {% for paper in conf.papers %}
            {% assign research = researches.papers | where:"id", paper.id | first %}
            <div class="project">
                <img class="project-img" src="{{ research.figure }}" alt="{{ research.alt }}">
                <div class="project-desc">
                    <p class="project-desc-main">
                    {% if research.page %}
                        <a href="{{ research.page }}">
                    {% endif %}
                        {{ research.title }}
                    {% if research.page %}
                        </a>
                    {% endif %}
                    </p>
                    <p>{{ research.authors }}</p>
                    <p class="pub-misc">
                        {% if research.link %}
                            <a class="pub-link" href="{{ research.link }}"><i class="fas fa-external-link-square-alt"></i>&nbsp;Publisher's Copy</a>
                        {% endif %}
                        {% if research.acm %}
                            <a class="pub-link" href="{{ research.acm }}"><i class="ai ai-acm ai-lg"></i>&nbsp;Open Access ACM</a>
                        {% endif %}
                        {% if research.file %}
                            <a class="pub-link" href="{{ research.file }}"><i class="ai ai-open-access ai-lg"></i>PDF</a>
                        {% endif %}
                        {% if research.arxiv %}
                            <a class="pub-link" href="{{ research.arxiv }}"><i class="ai ai-arxiv ai-lg"></i>&nbsp;arXiv Preprint</a>
                        {% endif %}
                        {% if research.doi %}
                            <a class="pub-link" href="https://doi.org/{{ research.doi }}"><i class="fas fa-globe"></i>&nbsp;DOI</a>
                        {% endif %}
                        {% if research.cite %}
                            <a class="pub-link" href="{{ research.cite }}"><i class="fas fa-quote-left"></i>&nbsp;Cite</a>
                        {% endif %}
                        {% if research.bibtex %}
                            <a class="pub-link" href="{{ research.bibtex }}"><i class="fas fa-book"></i>&nbsp;BibTeX</a>
                        {% endif %}
                        {% if research.award %}
                            <span class="pub-award"><i class="fas fa-trophy"></i> {{ research.award }}</span>
                        {% endif %}
                    </p>
                </div>
            </div>
        {% endfor %}
        </div>
    {% endfor %}
    </div>
    <div class="recent-pubs-header">
        <h4>Projects</h4>
        <!-- <a href="/projects/"><span>View all</span><i class="fas fa-angle-double-right"></i></a> -->
    </div>
    <div class="projects">
        {% for project in site.data.projects %}
        <div class="project">
            <img class="project-img" src="{{ project.img }}" alt="{{ project.alt }}">
            <div class="project-desc">
                <p class="project-desc-main"><a href="{{ project.link }}" target="_blank">{{ project.name }}</a></p>
                <p>{{ project.desc }}</p>
            </div>
        </div>
        {% endfor %}
    </div>
</div>

<div class="news-sidebar">
    <div class="externals">
        {% for item in site.data.external %}
        <a href="{{ item.link }}" target="_blank">
            <span>{{ item.icon }}</span>
            <span class="external-desc">{{ item.name }}</span>
            <span class="external-desc-short">{{ item.shortname }}</span>
        </a>
        {% endfor %}
    </div>
    <h4>Updates</h4>
    <ul class="sidebar-items">
        {% for item in site.data.news %}
            <li>
                <p class="news-date">{{ item.date }}</p>
                <p class="news-text">{{ item.text }}</p>
            </li>
        {% endfor %}
    </ul>
</div>