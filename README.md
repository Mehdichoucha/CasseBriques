# 🎮 Break-Briks (Breakout Game)

Un jeu de casse-briques moderne et dynamique développé en C++ avec SFML 3.0.2.

## 🎯 Description

Break-Briks est un jeu de casse-briques complet avec une interface utilisateur moderne et des effets visuels dynamiques :
- **Page d'accueil animée** avec titre arc-en-ciel et particules
- **Deux modes de jeu** : Raquette (disponible) et Canon (à venir)
- Raquette contrôlable avec physique réaliste
- Balle avec rebonds dynamiques
- Grille de 50 briques colorées (5 rangées × 10 colonnes)
- **Système de vies** (3 vies par partie)
- **Écrans de victoire et défaite** avec animations
- **Options de fin de partie** (Rejouer, Menu, Quitter)
- Système de score avec affichage en temps réel

## 🎮 Contrôles

### Menu Principal
- **↑/↓** ou **W/S** : Naviguer entre les options
- **Entrée** ou **Espace** : Sélectionner
- **Échap** : Quitter
- **Souris** : Navigation et clic

### En Jeu
- **A** ou **Flèche Gauche** : Déplacer la raquette à gauche
- **D** ou **Flèche Droite** : Déplacer la raquette à droite

### Écrans de Fin
- **↑/↓** ou **W/S** : Naviguer entre les options
- **Entrée** : Sélectionner
- **R** : Rejouer rapidement
- **M** : Retour au menu
- **Échap** : Quitter

## 🛠️ Technologies utilisées

- **C++17**
- **SFML 3.0.2** (Simple and Fast Multimedia Library)
- **Clang++** (Compilateur)

## 🚀 Installation et compilation

### Prérequis
- SFML 3.0.2 installé sur votre système
- Compilateur C++17 compatible

### Sur macOS avec Homebrew
```bash
# Installer SFML
brew install sfml

# Cloner le repository
git clone 
cd CasseBriques

# Compiler le projet
clang++ -std=c++17 *.cpp -o main -I/opt/homebrew/include -L/opt/homebrew/lib -lsfml-graphics -lsfml-window -lsfml-system

# Lancer le jeu
./main
```

## 🎨 Fonctionnalités implémentées

### ✅ Interface utilisateur moderne
- [x] **Page d'accueil dynamique** avec titre animé "BREAK-BRIKS"
- [x] **Animations arc-en-ciel** sur le titre avec effets de rebond
- [x] **Particules animées** en arrière-plan
- [x] **Dégradés de couleur** dynamiques
- [x] **Boutons stylisés** : "Raquette" et "Canon" (à venir)
- [x] **Navigation clavier et souris**

### ✅ Gameplay complet
- [x] **Mode Raquette** entièrement fonctionnel
- [x] **Système de vies** (3 vies par partie)
- [x] **Raquette contrôlable** avec physique réaliste
- [x] **Balle dynamique** avec angles de rebond variables
- [x] **50 briques colorées** (5 rangées × 10 colonnes)
- [x] **Système de score** (10 points par brique)
- [x] **Collision detection avancée**
- [x] **Conditions de fin** (victoire/défaite)

### ✅ Écrans de fin de partie
- [x] **Écran de victoire** avec animations dorées
- [x] **Écran de défaite** avec thème rouge
- [x] **Affichage du score final**
- [x] **Options de fin** : Rejouer, Menu, Quitter
- [x] **Animations des boutons** et sélection visuelle

### 🎨 Design et effets visuels
- **Page d'accueil** : Fond dégradé animé, particules flottantes
- **Titre dynamique** : Couleurs arc-en-ciel, rotations et rebonds
- **Boutons interactifs** : Effets de survol et sélection
- **Écrans de fin** : Fonds colorés thématiques (or/rouge)
- **Animations fluides** : 60 FPS avec deltaTime

## 🏗️ Architecture du code

### Structure modulaire (fichiers séparés)
- **`GameStates.h`** : Énumération des états (MENU, PLAYING, VICTORY, DEFEAT)
- **`GameData.h/.cpp`** : Structure des données de jeu
- **`Menu.h/.cpp`** : Gestionnaire du menu principal avec animations
- **`Game.h/.cpp`** : Logique de gameplay et physique
- **`EndScreen.h/.cpp`** : Gestionnaire des écrans de fin
- **`main.cpp`** : Boucle principale et gestion des états

### Gestion des états
Le jeu utilise une machine à états pour gérer :
- **Menu principal** → Navigation et sélection du mode
- **Jeu en cours** → Physique et gameplay
- **Écran de victoire** → Animation de réussite
- **Écran de défaite** → Options de continuation

### Concepts techniques utilisés
- Vecteurs 2D pour positions et vitesses
- Gestion du temps avec `deltaTime`
- Détection de collision AABB (Axis-Aligned Bounding Box)
- Conteneurs STL (`std::vector`) pour les briques
- Gestion d'événements SFML 3.0

---

**Score maximum possible : 500 points** (50 briques × 10 points)
