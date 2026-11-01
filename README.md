## Site vitrine — Saint-Germain-l’Auxerrois de Romainville

Site statique : `index.html` + `styles.css`, aucune dépendance ni build.
Police chargée depuis Google Fonts (Archivo), plan via OpenStreetMap.

## Développement
Prévisualiser en local : `npm run dev`, puis ouvrir http://localhost:8080.
Aucune installation : le serveur `serve` est récupéré à la volée par npx.

## Photos
Les photos actuelles viennent de Wikimedia Commons (catégorie « Église Saint-Germain-l'Auxerrois de Romainville »)
et sont chargées directement depuis upload.wikimedia.org. Crédits obligatoires (déjà dans le pied de page) :
façade : Chabe01, CC BY-SA 4.0 · intérieur aux vitraux : Parisette, CC BY-SA 3.0 · chapelle et nef : Rc1959, CC0 · carte postale : domaine public.
Pour ne plus dépendre de Wikimedia, télécharger les fichiers dans `images/` et remplacer les URL dans `index.html`.

## Photos maison (optionnel)
Créer un dossier `images/` et y déposer : `facade.jpg`, `vitraux.jpg`, `vierge.jpg`, `nef.jpg` (2400 px de large, JPEG ~300 Ko),
puis remplacer l’URL du `--photo:url(...)` correspondant dans `index.html`.
Tant qu'une photo manque, un dégradé de secours s'affiche.

## Avant mise en ligne : à faire valider par la paroisse
Les éléments surlignés en jaune (classe `.a-completer`) sont à remplir :
- messes de semaine
- jours et heures de l’accueil paroissial
- téléphone et e-mail

À confirmer aussi :
- messe du dimanche à 11h15 (trouvée sur un agrégateur, à vérifier sur messes.info)
- délais indiqués pour baptême, mariage, catéchisme (pratiques courantes, pas propres à la paroisse)
- mentions légales / directeur de publication (obligatoire pour un site en ligne)

Une fois complété, supprimer la classe `.a-completer` des éléments.

## Hébergement
GitHub Pages, déployé par GitHub Actions (`.github/workflows/deploy.yml`) à chaque push sur `main`.
Seuls `index.html`, `styles.css` et `images/` (s’il existe) sont publiés.
Prérequis côté dépôt : Settings → Pages → Source : « GitHub Actions ».
Alternative sans GitHub : glisser `index.html` et `styles.css` dans Netlify Drop.

## Statistiques de visites
Compteur GoatCounter, tableau de bord : https://sgaromainville.goatcounter.com.
Aucun cookie, donc pas de bandeau de consentement.
Les visiteurs équipés d’un bloqueur (Brave, uBlock…) ne sont pas comptés : les chiffres sont un minimum.

## Sources
Histoire : fiche de Seine-Saint-Denis Tourisme et dossier de l’Inventaire du patrimoine d’Île-de-France.
Horaires : messes.info.
