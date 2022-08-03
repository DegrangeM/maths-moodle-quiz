---
---

Description du site ...

{% for site in site.sites %}
  <h1>{{ site.nom }}</h1>
  <a href="{{ site.lien }}"><button>Accéder</button></a> <a href="{{ site.aide }}"><button>Aide</button></a>
  <p>{{ site.content | markdownify }}</p>
{% endfor %}