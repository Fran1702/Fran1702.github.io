---
layout: default
title: Projects
permalink: /projects/
---

<style>
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 24px;
    padding: 0;
    list-style: none;
    margin: 0 auto;
    max-width: 1000px;
  }

  .project-item {
    text-align: center;
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 12px;
    transition: box-shadow 0.3s ease;
    background: white;
  }

  .project-item:hover {
    box-shadow: 0 4px 15px rgba(0,0,0,0.15);
  }

  .project-thumb {
    width: 100%;
    height: 150px;
    object-fit: cover;
    border-radius: 6px;
    margin-bottom: 10px;
  }

  .project-title {
    font-weight: 600;
    font-size: 1.1em;
    color: #333;
    margin-bottom: 4px;
  }

  .project-subtitle {
    font-size: 0.9em;
    color: #666;
    margin-top: 0;
  }

  a.project-link {
    color: inherit;
    text-decoration: none;
  }

  a.project-link:hover {
    color: #007acc;
  }
</style>


<h1>My Projects</h1>

<ul class="projects-grid">
  {% for project in site.projects %}
    <li class="project-item">
      <a class="project-link" href="{{ project.url }}">
        <img class="project-thumb" src="{{ project.cover-img[0] }}" alt="{{ project.title }}">
        <div class="project-title">{{ project.title }}</div>
        {% if project.subtitle %}
          <div class="project-subtitle">{{ project.subtitle }}</div>
        {% endif %}
      </a>
    </li>
  {% endfor %}
</ul>
