---
---

Moodle est une plateforme formidable pour la création de cours.
Les activités "Tests" sont très pratiquent mais il est souvent difficile de créer des questions de types mathématiques (mise en forme des questions, traitement de la réponse de l'élève, etc.).
Plusieurs sites proposent des exercices mathématiques interactifs, mais les banques de questions ne sont pas toujours complètes et obligent à jongler entre plusieurs sites. Il est en revanche possible d'intégrer directement dans moodle certains de ces sites. Cette page propose la liste des sites compatibles.

# La liste des sites

{% for site in site.sites %}
  <h2>{{ site.nom }}</h2>
  <a href="{{ site.lien }}"><button>Accéder</button></a> <a href="{{ site.aide }}"><button>Aide</button></a>
  <p>{{ site.content | markdownify }}</p>
{% endfor %}