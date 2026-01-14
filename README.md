# 📱 ONF Veille Corse - Application Mobile PWA

## Guide d'Installation et d'Utilisation

---

## 🚀 Installation

### Option 1: Hébergement Gratuit (Recommandé)

1. **GitHub Pages** (100% gratuit)
   - Créer un compte GitHub (gratuit)
   - Créer un repository `onf-veille-corse`
   - Uploader les fichiers (index.html, manifest.json, sw.js, icons/)
   - Aller dans Settings > Pages > Source: main branch
   - L'app sera accessible sur `https://votre-username.github.io/onf-veille-corse/`

2. **Netlify** (gratuit)
   - Créer un compte sur netlify.com
   - Drag & drop le dossier `onf_mobile_app`
   - URL générée automatiquement

3. **Vercel** (gratuit)
   - Créer un compte sur vercel.com
   - Importer depuis GitHub ou upload direct
   - Déploiement instantané

### Option 2: Serveur Local (Test)
```bash
# Avec Python
cd onf_mobile_app
python -m http.server 8000
# Ouvrir http://localhost:8000

# Avec Node.js
npx serve onf_mobile_app
```

---

## 📲 Installer sur iPhone/iPad

1. Ouvrir Safari (obligatoire sur iOS)
2. Aller sur l'URL de l'application
3. Appuyer sur le bouton **Partager** (carré avec flèche)
4. Défiler et appuyer sur **"Sur l'écran d'accueil"**
5. Nommer l'app "ONF Veille" et confirmer
6. L'icône apparaît sur l'écran d'accueil !

---

## 📲 Installer sur Android

1. Ouvrir Chrome
2. Aller sur l'URL de l'application
3. Chrome affiche automatiquement **"Ajouter à l'écran d'accueil"**
4. Ou : Menu (⋮) > "Installer l'application"
5. Confirmer l'installation
6. L'app est maintenant installée !

---

## 🎯 Fonctionnalités

### 🏠 Accueil
- Statistiques globales (alertes, communes, critiques, résolues)
- Liste des 5 dernières alertes
- Accès rapide aux fonctions

### 🗺️ Carte
- Carte interactive de la Corse
- 5 zones pilotes (Bavella, Scandola, Coscione, Piana, Agriates)
- Marqueurs colorés par priorité
- Zoom par zone

### 📊 Statistiques
- Graphique infractions par type (donut)
- Graphique infractions par zone (barres groupées)
- Évolution mensuelle (courbe)
- Répartition par plateforme (pie)

### 📋 Données
- Liste complète des alertes
- Filtres par type d'infraction
- Filtre par commune
- Détails de chaque alerte

### ➕ Nouvelle Alerte
- Sélection type d'infraction
- Choix plateforme et commune
- Lien du contenu
- Capture d'écran (accès caméra)
- Notes complémentaires

### ⚙️ Paramètres
- Notifications on/off
- Mode sombre
- Synchronisation auto
- Génération de rapports (journalier/hebdo/mensuel)
- Informations système

---

## 🔧 Structure des Fichiers

```
onf_mobile_app/
├── index.html      # Application principale
├── manifest.json   # Configuration PWA
├── sw.js           # Service Worker (cache)
├── icons/          # Icônes de l'app
│   ├── icon-72.png
│   ├── icon-96.png
│   ├── icon-128.png
│   ├── icon-144.png
│   ├── icon-152.png
│   ├── icon-192.png
│   ├── icon-384.png
│   └── icon-512.png
└── README.md       # Ce fichier
```

---

## 🎨 Génération des Icônes

Pour générer les icônes, utiliser un outil en ligne gratuit :
- https://realfavicongenerator.net/
- https://www.pwabuilder.com/imageGenerator

Uploader un logo carré (512x512 minimum) et télécharger le pack d'icônes.

---

## 📡 Synchronisation

L'app stocke les données localement (localStorage).
- **Synchronisation manuelle** : bouton 🔄 dans le header
- Les données persistent même sans connexion
- Export possible via les rapports

---

## 🔒 Sécurité

- Pas de données sensibles stockées
- Pas d'authentification requise (usage interne)
- HTTPS obligatoire pour les PWA

---

## 📧 Support

Application développée pour le projet ONF Corse - Veille Digitale Environnementale.

**Contact**: Direction Territoriale ONF Corse

---

## 📝 Changelog

### v1.0.0 (Janvier 2026)
- Version initiale
- Dashboard avec statistiques
- Carte interactive Leaflet
- Graphiques Chart.js
- Formulaire nouvelle alerte
- Filtres et recherche
- Génération de rapports
- PWA installable iOS/Android
