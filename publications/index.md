---
layout: publications
permalink: /publications/
title: Publications
---

<!-- Override column widths because of changes in content. -->
<style>
    .twocol-content {
        margin-bottom: 40px;
    }

    .twocol-section {
        margin-bottom: 10px;
    }

    .twocol-left-col {
        width: 10%;
    }

    .twocol-entry {
        width: 88%;
    }
</style>

<div>
    {% for item in site.data.publications %}
        <div class="twocol-content twocol-section">
            <p class="twocol-left-col"></p>
            <p class="twocol-entry">{{ item.name }}</p>
        </div>

        {% if item.papers %}
            {% for paper in item.papers %}
                <div class="twocol-content">
                    <div class="twocol-left-col">
                        {% if paper.figure %}
                            <img class="pub-thumbnail" src="{{ paper.figure }}" alt="{{ paper.alt }}">
                        {% endif %}
                    </div>
                    <div class="twocol-entry">
                        <p class="pub-twocol-entry-main">
                            {% if paper.page %}
                                <a href="{{ paper.page }}">
                            {% endif %}
                            {{ paper.title }}
                            {% if paper.page %}
                                </a>
                            {% endif %}
                        </p>
                        <p>{{ paper.authors }}</p>
                        <p><em>{{ paper.venue }}</em>, {{ paper.year }}</p>
                        <p class="pub-misc">
                            {% if paper.file %}
                                <a class="pub-link" href="{{ paper.file }}"><i class="ai ai-open-access ai-lg"></i>PDF</a>
                            {% endif %}
                            {% if paper.arxiv %}
                                <a class="pub-link" href="{{ paper.arxiv }}"><i class="ai ai-arxiv ai-lg"></i>&nbsp;arXiv Preprint</a>
                            {% endif %}
                            {% if paper.link %}
                                <a class="pub-link" href="{{ paper.link }}"><i class="fas fa-external-link-square-alt"></i>&nbsp;Publisher's Copy</a>
                            {% endif %}
                            {% if paper.doi %}
                                <a class="pub-link" href="https://doi.org/{{ paper.doi }}"><i class="fas fa-globe"></i>&nbsp;DOI</a>
                            {% endif %}
                            {% if paper.cite %}
                                <a class="pub-link" href="{{ paper.cite }}"><i class="fas fa-quote-left"></i>&nbsp;Cite</a>
                            {% endif %}
                            {% if paper.bibtex %}
                                <a class="pub-link" href="{{ paper.bibtex }}"><i class="fas fa-book"></i>&nbsp;BibTeX</a>
                            {% endif %}
                            {% if paper.accept-rate %}
                                <span class="pub-accept-rate">Acceptance Rate: {{ paper.accept-rate }}%</span>
                            {% endif %}
                            {% if paper.award %}
                                <span class="pub-award"><i class="fas fa-trophy"></i> {{ paper.award }}</span>
                            {% endif %}
                        </p>
                    </div>
                </div>
            {% endfor %}
        {% endif %}
    {% endfor %}
</div>

<br>
#### Access
If you cannot access any of my publications from the publisher's websites, you may request from me thru email or my [ResearchGate profile](https://www.researchgate.net/profile/Briane_Paul_Samson).