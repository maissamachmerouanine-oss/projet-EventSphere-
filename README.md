# EventSphere - Plateforme d'événements responsive

## Contexte pédagogique
Cette plateforme web permet aux utilisateurs de découvrir et consulter des événements (conférences, ateliers, concerts, formations). Le site est entièrement responsive et s'adapte à tous les types d'écrans.

## Technologies utilisées
- HTML5
- CSS3 (Flexbox, Grid, Media Queries)
- JavaScript (menu burger)

## Structure du projet
```
eventsphere/
├── index.html                    # Page d'accueil
├── events.html                   # Liste des événements
├── event-details.html            # Détail d'un événement
├── contact.html                  # Formulaire de contact
├── css/
│   ├── style.css                 # Styles de base et variables
│   ├── layout.css                # Layouts avec Grid et Flexbox
│   ├── components.css            # Composants (header, cartes, boutons)
│   └── responsive.css            # Media Queries
├── images/
│   ├── hero.jpg                  # Image de la section hero
│   ├── event1.jpg                # Image événement 1
│   └── event2.jpg                # Image événement 2
└── js/
    └── script.js                 # Script pour le menu burger
```

## Viewport
Le viewport est configuré dans toutes les pages HTML :
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

**Importance du viewport :**
- Sans viewport, le navigateur mobile affiche le site comme sur desktop, rendant le contenu illisible
- Avec viewport, le site s'adapte correctement à la largeur de l'écran mobile
- `width=device-width` définit la largeur du viewport à la largeur de l'écran
- `initial-scale=1.0` définit le niveau de zoom initial

## Flexbox (obligatoire)
Flexbox est utilisé pour :
- **Header** : Alignement du logo, navigation et bouton burger
- **Navigation** : Disposition horizontale des liens de menu
- **Filtres** : Organisation des sélecteurs et champ de recherche
- **Boutons** : Centrage du contenu dans les boutons

Propriétés utilisées :
- `display: flex`
- `justify-content: space-between/center`
- `align-items: center`
- `flex-wrap: wrap` (pour les filtres)
- `gap` pour l'espacement

## CSS Grid (obligatoire)
Grid est utilisé pour :
- **Grille d'événements** : Affichage des cartes en colonnes adaptatives
- **Section hero détails** : Mise en page image + informations
- **Contact** : Formulaire et informations côte à côte

Propriétés utilisées :
- `display: grid`
- `grid-template-columns: repeat(3, 1fr)` (desktop), `repeat(2, 1fr)` (tablette), `1fr` (mobile)
- `gap` pour l'espacement

## Media Queries (obligatoire)
Breakpoints utilisés :
- **Mobile** : `@media (max-width: 767px)`
- **Tablette** : `@media (min-width: 768px) and (max-width: 1023px)`
- **Desktop** : `@media (min-width: 1024px)`

Adaptations :
- Grille événements : 1 colonne (mobile) → 2 colonnes (tablette) → 3 colonnes (desktop)
- Menu burger : visible sur mobile, navigation cachée par défaut
- Header : padding réduit sur mobile
- Contact : grille 1 colonne sur mobile
- Détails événement : grille 1 colonne sur mobile

## Fonctionnalités implémentées
- ✅ Design responsive complet
- ✅ Menu burger fonctionnel (JavaScript)
- ✅ 4 pages : accueil, événements, détails, contact
- ✅ Formulaire de contact
- ✅ Filtres sur la page événements
- ✅ Animations CSS (hover sur cartes)
- ✅ Structure sémantique HTML5

## Bonus implémentés
- Menu burger mobile avec JavaScript
- Animations CSS (transform sur hover)
- Optimisation des images (object-fit: cover)

## Comment lancer le projet
1. Ouvrir `index.html` dans un navigateur
2. Le site est entièrement statique, pas de serveur requis
3. Tester le responsive en redimensionnant la fenêtre ou sur mobile

## Navigateur supportés
- Chrome/Chromium
- Firefox
- Safari
- Edge