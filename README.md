# 🎯 DRAFT RADAR

**Outil pour créer des équipes de manière aléatoire** - Interface style terminal rétro avec effets visuels

![Version](https://img.shields.io/badge/version-5.0-green)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

---

## 📖 Description

Draft Radar est une application web interactive qui permet de créer des équipes aléatoires à partir d'une liste de joueurs (appelés "matelots"). Avec son interface style terminal des années 80 et ses effets visuels (scanlines, explosions), l'outil transforme la création d'équipes en une expérience ludique et immersive.

### ✨ Fonctionnalités Principales

- 🎲 **Attribution aléatoire** des joueurs aux navires (équipes)
- 👥 **4 à 20 matelots** configurables
- 🚢 **2 à 10 navires** (équipes) selon le nombre de joueurs
- ⌨️ **Interface clavier** - Ajout de joueurs avec la touche Entrée
- 📱 **100% Responsive** - Fonctionne sur desktop, tablette et mobile
- 💾 **Sauvegarde automatique** dans le navigateur (localStorage)
- 💥 **Effets visuels** - Explosions de particules lors des clics
- 🎨 **Thème rétro** - Police VT323, couleur vert terminal, scanlines

---

## 🚀 Démarrage Rapide

### Ouvrir l'application

1. **En ligne :**  
   Ouvrez directement : [Draft Radar sur GitHub Pages](https://martineisf.github.io/Draft-Radar/)

2. **En local :**  
   - Téléchargez le fichier `index.html`
   - Double-cliquez dessus ou ouvrez-le dans votre navigateur
   - Aucune installation requise !

### Première utilisation

1. Cliquez sur **"ACCÉDER AU RADAR"**
2. Cliquez sur **"CONFIG"** en haut à droite
3. Ajoutez vos joueurs (voir section suivante)
4. Choisissez le nombre de navires (équipes)
5. Cliquez sur **"GÉNÉRER LA GRILLE"**
6. Chaque joueur clique sur une case pour révéler son équipe ! 🎉

---

## 👥 Gestion des Matelots (Joueurs)

### Ajouter un joueur

**Méthode 1 - Avec l'input (recommandé) :**
1. Tapez le nom dans le champ de saisie
2. Appuyez sur **ENTRÉE** ⏎
3. Le joueur est ajouté instantanément

**Méthode 2 - Avec le bouton :**
1. Tapez le nom dans le champ
2. Cliquez sur **"+ AJOUTER UN MATELOT"**

💡 **Astuces :**
- Si vous laissez le champ vide, un nom par défaut sera généré ("Matelot 1", "Matelot 2"...)
- Les **noms doublons** sont détectés et refusés
- Les **noms vides** sont automatiquement rejetés
- Maximum **20 matelots**

### Modifier un nom

Cliquez directement dans le nom dans la liste et modifiez-le en ligne.

### Supprimer un joueur

Cliquez sur le **X** à droite du nom (minimum 4 joueurs requis).

---

## 🚢 Configuration des Navires (Équipes)

### Règles automatiques

- **Minimum 2 navires** (équipes)
- **Maximum 10 navires**
- Chaque navire doit avoir **au moins 2 matelots**
- Le slider s'adapte automatiquement selon le nombre de joueurs

### Exemples de configurations

| Matelots | Navires possibles | Exemple de répartition |
|----------|-------------------|------------------------|
| 4        | 2                 | 2 joueurs par équipe   |
| 9        | 2-4               | 3-2-2-2 ou 5-4         |
| 20       | 2-10              | 2 joueurs par équipe   |

---

## 🎮 Mode Jeu

### Comment jouer

1. **Grille générée** - Chaque case représente un matelot
2. **Tour par tour** - Le nom du joueur actif s'affiche en haut
3. **Cliquer sur une case** - Révèle le navire assigné
4. **Effet visuel** - Explosion de particules vertes 💥
5. **Progression** - Barre de progression globale
6. **Sidebar** - État en temps réel de chaque navire

### Interface de jeu

```
┌─────────────────────────────────────────┐
│  >> ORDRE DE TIR : Alice (1/9)         │
│  ████████░░░░░░░░░░░░░░░  40%          │
├─────────────────────────┬───────────────┤
│                         │  État Flotte  │
│    A   B   C            │               │
│  1 [A1][A2][A3]        │ ▸ PORTE-AVIONS│
│  2 [B1][B2][B3]        │   Alice  2/3  │
│  3 [C1][C2][C3]        │               │
│                         │ ▸ CROISEUR    │
│                         │   Bob    1/3  │
└─────────────────────────┴───────────────┘
```

### Fin de partie

Lorsque tous les matelots ont cliqué, un **DEBRIEFING** s'affiche avec la composition finale de chaque navire.

---

## 📱 Responsive Design

### Desktop (1920×1080, 1366×768)
- Grille spacieuse avec cellules de **150px**
- Sidebar à droite
- Gap de **8px** entre cellules

### Tablette (768×1024)
- Grille adaptée
- Sidebar en dessous de la grille
- Navigation optimisée

### Mobile (375×667, 414×896)
- Grille avec cellules de **100px**
- **Maximum 3 colonnes** sur mobile
- Gap de **3px** entre cellules
- **Scroll vertical** activé pour voir toute la grille
- Textes adaptés pour la lisibilité

---

## 🧪 Tests et Validation

### Tests automatiques

Ouvrez la **Console du navigateur** (F12) pour voir les tests automatiques :

```
🧪 DRAFT RADAR - TESTS DE VALIDATION
=====================================
✓ Test 1 - Ratio grille : 58.3% (objectif: ~60%)
✓ Test 2 - Alignement axes : OK ✅ (delta: 0.0px)
✓ Test 3 - Input présent : OK ✅
✓ Test 4 - Mode : DESKTOP 🖥️ (largeur: 1920px)
=====================================
🎯 VALIDATION TERMINÉE
```

### Tests manuels

Consultez les instructions en haut du fichier HTML (lignes 1-37) pour les tests manuels détaillés.

---

## 🛠️ Technologies Utilisées

- **HTML5** - Structure sémantique
- **CSS3** - Styles avec variables CSS, flexbox, grid
- **JavaScript Vanilla** - Logique sans framework
- **LocalStorage API** - Sauvegarde persistante
- **Canvas API** - Effets de particules

### Dépendances

- **Google Fonts** - Police VT323 (terminal rétro)
- Aucune autre dépendance externe !

---

## 🎨 Personnalisation

### Modifier les couleurs

Dans le fichier `index.html`, ligne ~10 :

```css
:root {
    --p: #00FF00;     /* Couleur principale (vert) */
    --d: #003300;     /* Couleur sombre */
    --bg: #000000;    /* Fond */
    --error: #FF0000; /* Erreurs */
}
```

### Modifier les noms de navires

Ligne ~981 dans `index.html` :

```javascript
const SHIPS = [
    "PORTE-AVIONS", "SOUS-MARIN", "CROISEUR", 
    "DESTROYER", "FRÉGATE", "CUIRASSÉ",
    "CORVETTE", "ESCORTEUR", "PATROUILLEUR", "TORPILLEUR"
];
```

### Modifier les limites

```javascript
const MAX_NAMES = 20;              // Maximum de joueurs
const MIN_MATELOTS_PER_SHIP = 2;   // Minimum par équipe
```

---

## 📂 Structure du Projet

```
Draft-Radar/
├── index.html          # Application complète (HTML + CSS + JS)
├── .gitignore         # Fichiers à ignorer par Git
└── README.md          # Cette documentation
```

**Note :** L'application est un **fichier HTML unique** autonome !

---

## 🐛 Résolution de Problèmes

### La grille ne s'affiche pas
- Vérifiez que vous avez au moins 4 matelots
- Vérifiez le nombre de navires requis (min 2 matelots par navire)

### Les noms ne se sauvegardent pas
- Vérifiez que les cookies/localStorage sont autorisés dans votre navigateur
- En mode privé, les données sont perdues à la fermeture

### L'input ne fonctionne pas
- Assurez-vous d'utiliser un navigateur moderne (Chrome, Firefox, Edge, Safari)
- Vérifiez la console (F12) pour d'éventuelles erreurs

### Sur mobile, la grille est coupée
- Utilisez le **scroll vertical** pour voir toute la grille
- La grille s'adapte automatiquement à la taille d'écran

---

## 🔄 Réinitialisation

### Abandonner la mission actuelle
1. Cliquez sur **"CONFIG"**
2. Cliquez sur **"ABANDONNER MISSION"**
3. Les noms sont conservés, seule la grille est réinitialisée

### Réinitialisation totale
1. Cliquez sur **"CONFIG"**
2. Cliquez sur **"RÉINITIALISATION TOTALE"** (bouton rouge)
3. ⚠️ **TOUTES les données sont effacées définitivement**

---

## 📝 Historique des Versions

### Version 5.0 (31 Janvier 2026)
- ✨ Input avec touche Entrée pour ajouter des joueurs
- ✨ Validation des noms (pas de doublons, pas de noms vides)
- ✨ Grille responsive avec scroll mobile
- ✨ Taille de cellules fixe (150px desktop, 100px mobile)
- ✨ Grille mobile optimisée (max 3 colonnes)
- ✨ Alignement pixel-perfect des axes
- ✨ Tests automatiques intégrés
- 🐛 Correction du scroll sur mobile
- 📖 Documentation complète

### Version 4.0
- Format de grille optimisé (ratio 60% hauteur)
- Amélioration du responsive design
- Interface utilisateur améliorée

---

## 👨‍💻 Auteur

**MARTOCHE** - [GitHub](https://github.com/MartineEisf)

---

## 📜 Licence

Ce projet est sous licence MIT - vous êtes libre de l'utiliser, le modifier et le distribuer.

---

## 🙏 Remerciements

- Police **VT323** par Google Fonts
- Inspiration design : terminaux des années 80
- Communauté open-source

---

## 📞 Support

Des questions ? Des suggestions ?
- Ouvrez une [issue sur GitHub](https://github.com/MartineEisf/Draft-Radar/issues)
- Contactez-moi via GitHub

---

**Bon draft ! 🚀⚓**
