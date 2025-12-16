## A) Photo dans le header : lien cliquable correct (nouvel onglet + sécurité)
- Votre lien de photo pointe vers `#` (cela ne fait rien)
- Le clic doit ouvrir l’image dans un nouvel onglet
- Exemple :
```
<a href="./img/Bron_Thomas_resultat.jpg" target="_blank" rel="noopener noreferrer">
  <img src="./img/Bron_Thomas_resultat.jpg" alt="Photo de Thomas Bron">
</a>
```
## B) Corriger le HTML invalide (listes et balises mal fermées)
- Vous avez des `<ul>` imbriqués sans fermeture correcte
- Vous avez des titres (`h2`) placés dans des listes
- Veuillez corriger la structure :
  - une liste `<ul>` contient uniquement des `<li>`
  - on ferme `</ul>` avant de passer à un autre titre/section

## C) Ne pas utiliser `<nav>` pour du contenu (qualités / défauts)
- La balise `<nav>` sert uniquement aux menus de navigation
- Veuillez remplacer ce bloc par une `<section>`

## D) Footer : ajouter `&copy;2025` + e-mail cliquable
- Le footer est vide
- Veuillez ajouter `&copy;2025` + votre e-mail en `mailto:`
- Exemple :
```
<footer>
  &copy;2025 Thomas Bron —
  <a href="mailto:prenom.nom@email.com">prenom.nom@email.com</a>
</footer>
```

## Autres
- Attention à l'indentation et à la lisibilité du code
- utilisez `<strong>` plutôt que `<b>`
- ajouter des favicons à la racine du projet
  
