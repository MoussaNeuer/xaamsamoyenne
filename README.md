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
/xaamsamoyenne/
│
├── 📁 admin/                          # Espace administrateur
│   ├── 📁 includes/
│   │   ├── admin_auth.php             # Authentification admin
│   │   └── admin_header.php           # Header commun admin
│   │
│   ├── index.php                      # Dashboard admin
│   ├── login.php                      # Connexion admin
│   ├── users.php                      # Gestion des utilisateurs (CRUD)
│   ├── series.php                     # Gestion des séries (CRUD)
│   ├── matieres.php                   # Gestion des matières (CRUD)
│   ├── coefficients.php               # Gestion des coefficients
│   ├── stats.php                      # Statistiques globales
│   └── settings.php                   # Paramètres du site
│
├── 📁 assets/                          # Ressources statiques
│   ├── 📁 css/
│   │   ├── style.css                   # Styles principaux
│   │   └── style.min.css               # Version minifiée
│   │
│   ├── 📁 js/
│   │   ├── main.js                     # JavaScript principal (animations, toasts)
│   │   └── main.min.js                 # Version minifiée
│   │
│   └── 📁 images/                      # Images du site
│       ├── logo.png
│       └── favicon.ico
│
├── 📁 auth/                             # Authentification publique
│   ├── login.php                        # Connexion utilisateur
│   ├── register.php                     # Inscription
│   ├── logout.php                       # Déconnexion
│   └── reset-password.php                # Réinitialisation mot de passe
│
├── 📁 includes/                          # Fonctions communes
│   ├── config.php                        # Configuration globale
│   ├── database.php                      # Connexion PDO
│   └── auth_functions.php                 # Fonctions d'authentification
│
├── 📁 lycee/                             # Espace Lycéens
│   ├── 📁 includes/
│   │   └── lyceen_functions.php          # Fonctions spécifiques lycée
│   │
│   ├── index.php                          # Dashboard lycéen
│   ├── notes.php                          # Liste des notes
│   ├── ajouter-note.php                   # Ajout de note avec coefficient
│   ├── simulateur.php                      # Simulateur objectif examen
│   ├── historique.php                      # Historique des notes
│   └── profil.php                          # Profil lycéen
│
├── 📁 universite/                         # Espace Étudiants LMD
│   ├── 📁 includes/
│   │   └── etudiant_functions.php          # Fonctions spécifiques LMD
│   │
│   ├── index.php                            # Dashboard étudiant
│   ├── ues.php                              # Gestion des UE (Création/Liste)
│   ├── ue-details.php                        # Détail d'une UE
│   ├── ecs.php                               # Gestion des EC par UE
│   ├── ajouter-ec.php                         # Ajout d'EC (modal)
│   ├── notes.php                              # Liste des notes LMD
│   ├── ajouter-note.php                        # Ajout de note (EC)
│   ├── simulateur.php                          # Simulateur LMD
│   ├── historique.php                          # Historique semestriel
│   └── profil.php                              # Profil étudiant
│
├── index.php                                # Page d'accueil publique
├── dashboard.php                            # Redirection vers espace selon rôle
├── .htaccess                                # Configuration Apache (cache, compression)
└── README.md                                # Documentation du projet
