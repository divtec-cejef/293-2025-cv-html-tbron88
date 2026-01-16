## A) HTML — Listes mal fermées / structure cassée

Dans `Ma formation`, vous ouvrez un `<ul>` puis vous **ré-ouvrez un autre `<ul>` sans fermer le premier**, et ensuite vous enchaînez des `<h2>` au milieu.

> 💬 « Un `<ul>` ne doit contenir que des `<li>`. Les titres (`<h2>`) doivent être en dehors. »

✅ À corriger :

* Fermer chaque liste avant de passer à une autre section.
* Chaque section = un titre (`h2`) puis son contenu (souvent un `ul`).

---

## B) HTML — Lien du menu “Mes compétences” ne fonctionne pas

Dans le menu, vous avez :

* lien : `href="#competences"`
* mais dans la page : **il n’existe aucun élément** avec `id="competences"`

Donc le clic ne peut pas scroller au bon endroit.

> 💬 « Une ancre fonctionne seulement si le `href="#..."` correspond exactement à un `id="..."`. »

✅ À corriger :

* Ajouter une section “compétences” avec `id="competences"`
  OU
* Changer le lien du menu pour pointer vers un `id` existant.

---

## C) CSS — `a:hover { text-decoration: italic; }` ne marche pas

`text-decoration` ne peut pas prendre la valeur `italic`.

> 💬 « Italic = `font-style: italic;` ; `text-decoration` sert à underline/line-through/etc. »

✅ À corriger :

* Remplacer par `font-style: italic;` si vous voulez de l’italique au survol.

---

## E) CSS — Classe `.avatar` définie mais jamais utilisée

Vous avez une règle :

* `.avatar { ... box-shadow ... }`

Mais dans le HTML, l’image n’a **pas** `class="avatar"`.

Donc l’ombre ne s’applique pas.

> 💬 « Une règle CSS ne sert que si elle cible vraiment un élément (classe/id utilisés). »

✅ À corriger (au choix) :

* Ajouter `class="avatar"` sur l’image
  OU
* Mettre l’ombre directement sur `img` (moins précis).

---

## F) CSS — Image responsive : `width: auto` inutile ici

Dans `img` :

* `max-width: 100%`
* `height: auto`
* `width: auto`

`width: auto` est la valeur par défaut, donc elle n’apporte rien.

> 💬 « Gardez seulement les règles utiles : `max-width: 100%` + `height: auto` suffisent. »

✅ À simplifier :

* enlever `width: auto;`

---

## G) Étape 2 — Éléments manquants pour valider complètement

Il vous manque encore plusieurs critères demandés :

* tailles en `px` et `em`
* `background-image`
* `@font-face`
* `header { padding: ... }`
* `footer { margin: ... }`

✅ Exemple d’idée simple :

* `h1 { font-size: 40px; }` (px)
* `h2 { font-size: 1.5em; }` (em)
* `body { background-image: url("..."); }`
* ajouter un `@font-face` (police locale)
