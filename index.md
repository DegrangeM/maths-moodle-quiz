---
---

Moodle est une plateforme formidable pour la création de cours.
Les activités "Tests" sont très pratiques mais il est souvent difficile de créer des questions de types mathématiques (mise en forme des questions, traitement de la réponse de l'élève, etc.).
Plusieurs sites proposent des exercices mathématiques interactifs, mais les banques de questions ne sont pas toujours complètes et obligent à jongler entre plusieurs sites. Il est en revanche possible d'intégrer directement dans moodle certains de ces sites. Les scores obtenus aux exercices sont alors directement remontés dans moodle. Cette page propose une liste de sites compatibles. A noter que cela ne nécessite aucun plugin.

# La liste des sites

{% for s in site.sites %}
<div {% if s.wip %} style="opacity:0.25;" {% endif %}>
  <h2 id="site-{{ s.slug }}">{{ s.nom }}</h2>
  <a href="{{ s.lien }}"><button>Accéder</button></a> <a href="{{ s.aide }}"><button>Aide</button></a>
  {% if s.image %}<center><a href="./sites/images/{{s.slug}}.png"><img src="./sites/images/{{s.slug}}.png" style="max-height:300px;max-width:500px;" /></a></center>{% endif %}
  <p>{{ s.content | markdownify }}</p>
</div>
{% endfor %}

# Carte des intégrations

{% include carte.html %}

# Fonctionnement

{% include fonctionnement.md %}

# Démonstration

{% include demonstration.md %}
