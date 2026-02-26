# 🇸🇳 XaamSaMoyenne (XSM)

**XaamSaMoyenne** ("Connais ta moyenne" en wolof) est une application web **Mobile-First** conçue pour aider les élèves et étudiants du Sénégal à calculer, simuler et suivre leurs performances académiques. 

Que ce soit pour le système secondaire (Lycée) ou le système universitaire (**LMD**), l'application s'adapte aux coefficients et aux crédits spécifiques de chaque établissement, qu'il soit public ou privé.

---

## 🚀 Fonctionnalités Clés

### 🎓 Pour les Étudiants (Système LMD)
- **Gestion des UE & EC :** Découpage précis par Unité d'Enseignement et Éléments Constitutifs.
- **Crédits Paramétrables :** L'utilisateur peut modifier le nombre de crédits (ECTS) pour chaque module.
- **Logique de Compensation :** Calcul automatique de la validation par compensation semestrielle (si Moyenne Générale ≥ 10).
- **Zéro Stress :** Pas de règle éliminatoire complexe, focus sur l'obtention des 30 ou 60 crédits.

### 🏫 Pour les Lycéens (Séries S, L, G)
- **Coefficients Officiels :** Pré-chargement des coefficients selon la série (S1, S2, L1, L2, G, etc.).
- **Calcul Pondéré :** Gestion des notes de devoirs et compositions.

### 🛠 Fonctions Communes
- **Simulateur d'Examen :** "Combien dois-je avoir à l'examen pour valider mon année ?"
- **Espace Personnel :** Inscription, Connexion sécurisée et option "Se souvenir de moi".
- **Historique :** Suivi de l'évolution des moyennes au fil des semestres.
- **Back-Office Admin :** Interface de gestion pour l'administrateur (statistiques, gestion des utilisateurs et des référentiels).

---

## 🎨 Design & UX/UI
- **Design :** Épuré, professionnel, dominé par le **Blanc**, avec des accents **Vert, Jaune, Rouge** (Couleurs du Sénégal).
- **Mobile-First :** Interface optimisée pour une utilisation à une main.
- **Iconographie :** Utilisation de **Font Awesome 6**.
- **Navigation :** Barre de menu fixe en bas de l'écran (Bottom Nav).

---

## 🛠 Stack Technique
- **Frontend :** HTML5, CSS3 (Flexbox/Grid), JavaScript (ES6+).
- **Backend :** PHP 8.x (Architecture sécurisée).
- **Base de données :** MySQL (via PDO pour la sécurité contre les injections SQL).
- **Sécurité :** `password_hash()` pour les mots de passe, protection contre les failles XSS.

---

## 📂 Structure du Projet
```text
/XaamSaMoyenne
├── /admin             # Back-office (Gestion users, stats, config)
├── /assets            # CSS, JS, Images, Font Awesome
├── /includes          # Fonctions PHP, connexion BDD (PDO), header/footer
├── /auth              # login.php, register.php, reset-password.php
├── dashboard.php      # Page principale utilisateur
├── index.php          # Page d'accueil / Vitrine
└── README.md          # Documentation du projet