---
layout: default
---
<h2>{{ page.nom }}</h2>
<a href="{{ page.lien }}"><button>Accéder</button></a> <a href="{{ page.aide }}"><button>Aide</button></a>
<p>{{ page.content | markdownify }}</p>