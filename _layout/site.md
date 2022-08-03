---
---
<h2>{{ s.nom }}</h2>
<a href="{{ s.lien }}"><button>Accéder</button></a> <a href="{{ s.aide }}"><button>Aide</button></a>
<p>{{ s.content | markdownify }}</p>