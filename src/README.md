# Composant de Carte de Profil en HTML & CSS

![License](https://img.shields.io/badge/license-MIT-blue.svg) ![Version](https://img.shields.io/badge/version-1.0.0-green.svg)

> Un composant de carte de profil moderne et responsive, construit avec une approche "mobile-first" en HTML5 sémantique et CSS3.

Ce projet est une implémentation frontend pure d'une maquette de carte de profil utilisateur. L'accent a été mis sur la création d'un code propre, maintenable et scalable, en utilisant des techniques CSS modernes comme Flexbox, les Custom Properties (variables CSS) et une architecture de nommage BEM.

![Aperçu du Composant de Carte de Profil](https://i.imgur.com/GNWaB46.png)

---

## 📋 Table des Matières

1.  [Aperçu du Projet](#-aperçu-du-projet)
2.  [Fonctionnalités](#-fonctionnalités)
3.  [Technologies Utilisées](#-technologies-utilisées)
4.  [Installation et Lancement](#-installation-et-lancement)
5.  [Utilisation](#-utilisation)
6.  [Défis et Apprentissages](#-défis-et-apprentissages)
7.  [Améliorations Possibles](#-améliorations-possibles)
8.  [Auteur](#-auteur)
9.  [Licence](#-licence)

---

## 🚀 Aperçu du Projet

L'objectif de ce projet était de traduire fidèlement une conception UI en un composant web fonctionnel et robuste. Plus qu'un simple exercice de style, ce fut une étude de cas sur l'importance de l'architecture CSS et de la structuration HTML pour garantir la longévité et la facilité de maintenance d'un composant.

---

## ✨ Fonctionnalités

*   **HTML Sémantique :** Utilisation de balises appropriées (`<article>`, `<header>`, `<footer>`) pour améliorer l'accessibilité et le SEO.
*   **CSS Moderne :** Layout entièrement géré avec Flexbox pour un alignement et une distribution flexibles des éléments.
*   **Architecture CSS Scalable :** Nommage des classes inspiré de la méthodologie BEM (`profile-card__header`) pour éviter les conflits de style et rendre le code plus lisible.
*   **Variables CSS (Custom Properties) :** Centralisation des valeurs de design (couleurs, espacements) pour un theming et des ajustements facilités.
*   **Design Responsive :** Le composant s'adapte élégamment aux différentes tailles d'écran grâce à des media queries.
*   **Code Commenté :** Le code est documenté pour expliquer les décisions architecturales et les parties les plus complexes.

---

## 🛠️ Technologies Utilisées

Ce projet a été construit sans aucun framework, en utilisant uniquement les technologies web de base.

*   **Frontend**
    *   HTML5
    *   CSS3 (Flexbox, Custom Properties, Media Queries)
*   **Outils de développement**
    *   Git & GitHub pour le versioning

---

## ⚙️ Installation et Lancement

Le projet est entièrement statique et ne nécessite aucune installation de dépendances.

1.  **Clonez le dépôt :**
    ```bash
    git clone https://github.com/djilanrene/foc-defi-1-djilanrene.git
    ```

2.  **Accédez au dossier du projet :**
    ```bash
    cd foc-defi-1-djilanrene
    ```

3.  **Ouvrez le fichier `index.html` :**
    Ouvrez simplement le fichier `index.html` dans votre navigateur web. Le composant est prêt à être visualisé.

---

## 📖 Utilisation

Ce composant est autonome. Vous pouvez :
*   Visualiser le rendu final en ouvrant le fichier `index.html`.
*   Intégrer le code HTML et CSS dans un projet plus large.
*   Modifier les variables CSS dans `styles.css` pour personnaliser rapidement l'apparence de la carte (couleurs, espacements, etc.).

---

## 🧠 Défis et Apprentissages

**Défi : Le positionnement de l'avatar**

Le principal défi technique a été de positionner l'avatar pour qu'il chevauche parfaitement la section supérieure (header) et la section inférieure (footer) de la carte, tout en restant centré.

**Solution :**
Une technique de positionnement absolu combinée à une transformation CSS a été utilisée.
1.  Le conteneur du header (`.profile-card__header`) a été défini comme `position: relative` pour servir de référentiel.
2.  L'avatar (ou son conteneur) a été placé en `position: absolute` à l'intérieur du header.
3.  En le positionnant à `bottom: 0`, on le colle au bas de la section du header.
4.  La magie opère avec `transform: translateY(50%)`, qui le décale vers le bas de 50% de *sa propre hauteur*, créant ainsi l'effet de chevauchement désiré. Cette méthode est robuste et s'adapte à différentes tailles d'avatar.

**Apprentissages :**
*   **Maîtrise du positionnement CSS :** Renforcement des concepts de flux, de position relative/absolue et de l'impact des transformations.
*   **Architecture de composant :** Comprendre comment décomposer une interface en blocs logiques (`header`, `footer`, `stats`) rend le développement beaucoup plus gérable.
*   **Puissance des variables CSS :** Réaliser à quel point l'utilisation de `var(--ma-couleur)` au lieu de codes hexadécimaux partout simplifie la maintenance et ouvre la porte à des fonctionnalités comme le theming.

---

## 🔮 Améliorations Possibles

- [ ] **Transitions & Micro-interactions :** Ajouter des transitions CSS subtiles sur les boutons et les statistiques au survol (`:hover`) pour une expérience plus dynamique.
- [ ] **Transformation en Composant Web :** Encapsuler le HTML, CSS et (futur) JS dans un Web Component pour une réutilisabilité maximale.
- [ ] **Accessibilité (a11y) :** Améliorer davantage l'accessibilité en ajoutant des attributs ARIA pour les utilisateurs de lecteurs d'écran.
- [ ] **Intégration Framework :** Montrer comment ce composant peut être porté vers un framework comme React, Vue ou Svelte en le rendant dynamique via des `props`.

---

## 👤 Auteur

*   **René DJILAN**
*   GitHub: [@djilanrene](https://github.com/djilanrene/)
*   Portfolio: [bento.me/foc-togo](https://bento.me/foc-togo)

---

## 📜 Licence

Ce projet est distribué sous la licence MIT.