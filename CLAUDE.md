# CLAUDE.md

Site vitrine de la paroisse Saint-Germain-l’Auxerrois de Romainville (93).

## Nature du projet
- Site statique pur : `index.html` + `styles.css`. **Aucun build, aucune dépendance** — garder ainsi, il doit pouvoir être déposé tel quel sur Netlify Drop ou GitHub Pages.
- Prévisualisation locale : `npm run dev` → http://localhost:8080 (`serve` récupéré à la volée par npx, rien d’installé).
- `package.json` ne sert qu’au serveur de dev.

## Conventions
- Tout est en français : noms de classes CSS, commentaires, contenus (`.photo`, `.chapeau`, `.corps`, `.frise`, `.cartes`, `.pratique`, `.a-completer`…).
- Typographie française : apostrophe typographique `’`, « guillemets », exposants `<sup>e</sup>`.
- Couleurs et espacements en variables dans `:root` de `styles.css`, redéfinies dans le bloc `prefers-color-scheme: dark`.
- Police unique : Archivo (Google Fonts).
- Points de rupture : `56rem` (menu mobile, colonnes empilées) et `40rem` (mot-symbole sur deux lignes).

## Structure de `index.html`
- En-tête posé sur la photo d’ouverture ; menu mobile en `<details>` stylé par le `<style>` inline du `<head>`.
- Sections d’information `#messes`, `#histoire`, `#sacrements`, `#venir`, intercalées de panneaux `.photo` plein écran.
- Chaque panneau `.photo` prend son image dans `style="--photo:url(...)"` ; une classe `.s-*` (`.s-facade`, `.s-vitraux`…) fournit le dégradé de secours.
- Le petit script en bas de page ajuste la taille du mot-symbole `.mot` à la largeur disponible.
- Données structurées schema.org (`Church`) dans le `<head>` : à tenir à jour avec l’adresse.

## Contenus
- `.a-completer` (surligné jaune) = information manquante à faire valider par la paroisse. **Ne jamais inventer** d’horaires, téléphone ou e-mail.
- Photos chargées depuis Wikimedia Commons : si une photo change, mettre à jour les crédits et licences dans le pied de page.
- La liste « avant mise en ligne » est dans le `README.md`.
