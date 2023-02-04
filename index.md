---
---

<!-- Ce site permet de générer des questions provenant d'exerciseurs (Labomep, Mathalea, Geogebra, etc.) à importer dans des tests (quiz) moodle. Les scores obtenus dans l'exerciseurs sont récupéré afin d'être utilisé comme score de la question.

----
-->

Vous trouverez sur cette page une solution permettant d'intégrer de nombreux exerciseurs (Labomep, Mathalea, Geogebra, etc.) directement dans Moodle sans nécessiter aucun plugin. Ces exerciseurs sont intégrés dans l'activité "Test (Quiz)" de Moodle sous forme de questions (à importer). Les scores obtenus dans l'exerciseurs sont récupéré afin d'être utilisé comme score de la question.

Il est ainsi possible de créer des quiz avec des exercices provenant de différents exerciseurs, sans que les élèves n'aient à jongler avec des comptes ou interfaces différentes.

<!--

--------------------

Moodle est une plateforme formidable pour la création de cours.
Les activités "Tests" sont très pratiques mais il est souvent difficile de créer des questions de types mathématiques (mise en forme des questions, traitement de la réponse de l'élève, etc.).
Plusieurs sites proposent des exercices mathématiques interactifs, mais les banques de questions ne sont pas toujours complètes et obligent à jongler entre plusieurs sites. Il est en revanche possible d'intégrer directement dans moodle certains de ces sites. Les scores obtenus aux exercices sont alors directement remontés dans moodle. Cette page propose une liste de sites compatibles. A noter que cela ne nécessite aucun plugin.

-->

# La liste des sites

{% for s in site.sites %}
<div {% if s.wip %} style="opacity:0.25;" {% endif %}>
  <h2 id="site-{{ s.slug }}">{{ s.nom }}</h2>
  <a href="{{ s.lien }}"><button>Accéder</button></a>
  <a href="{{ s.aide }}"><button>Aide</button></a>
  {% if s.demo %}<a href="#démonstration"><button>Démo</button></a>{% endif %}
  {% if s.image %}<center><a href="./sites/images/{{s.slug}}.png"><img src="./sites/images/{{s.slug}}.png" style="max-height:300px;max-width:500px;" /></a></center>{% endif %}
  <p>{{ s.content | markdownify }}</p>
</div>
{% endfor %}

# Carte des intégrations

{% include carte.html %}

# Démonstration

{% include demonstration.md %}

# Fonctionnement

{% include fonctionnement.md %}