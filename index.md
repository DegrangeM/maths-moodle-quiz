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

# Test

<script src="./neo4jd3/d3.min.js"></script>
<script src="./neo4jd3/neo4jd3.js"></script>
<link href="./neo4jd3/neo4jd3.min.css" rel="stylesheet" />
<div id="map">
</div>
<script>
  new Neo4jd3('#map', {}).updateWithD3Data({
    "nodes": [
        {
            "id": "1",
            "labels": ["User"],
            "properties": {
                "userId": "eisman"
            }
        },
        {
            "id": "8",
            "labels": ["Project"],
            "properties": {
                "name": "neo4jd3",
                "title": "neo4jd3.js",
                "description": "Neo4j graph visualization using D3.js.",
                "url": "https://eisman.github.io/neo4jd3"
            }
        }
    ],
    "relationships": [
        {
            "id": "7",
            "type": "DEVELOPES",
            "startNode": "1",
            "endNode": "8",
            "properties": {
                "from": 1470002400000
            },
            "source": "1",
            "target": "8",
            "linknum": 1
        }
    ]
});
</script>