# 🇷🇪 Reunion Monitor — Dashboard des travaux numériques Réunion

> **Monitor temps réel** qui intègre et affiche directement **toutes mes démos en ligne liées à La Réunion** dans une interface type *World Monitor* : iframe intégrée, panneaux d'intelligence, sidebar interactive et détection automatique via l'API GitHub.

[![GitHub repo](https://img.shields.io/badge/GitHub-gunout%2Freunion--monitor-blue?logo=github)](https://github.com/gunout/reunion-monitor)
[![Version](https://img.shields.io/badge/version-1.0-blue)](https://github.com/gunout/reunion-monitor)
[![Licence](https://img.shields.io/badge/licence-MIT-red)](https://github.com/gunout/reunion-monitor/blob/main/LICENSE)
[![Statut](https://img.shields.io/badge/statut-production-success)](https://gunout.github.io/reunion-monitor/)
[![Démos](https://img.shields.io/badge/d%C3%A9mos-32%20en%20ligne-green)](https://gunout.github.io/reunion-monitor/)
[![Responsive](https://img.shields.io/badge/responsive-mobile%20%7C%20tablette%20%7C%204K-informational)](https://gunout.github.io/reunion-monitor/)
[![Dark Mode](https://img.shields.io/badge/theme-dark-black)](https://gunout.github.io/reunion-monitor/)

---

## 🔗 Liens rapides

| Ressource | Lien |
|-----------|------|
| 📦 **Dépôt GitHub** | [github.com/gunout/reunion-monitor](https://github.com/gunout/reunion-monitor) |
| 🌐 **Démo en ligne** | [gunout.github.io/reunion-monitor](https://gunout.github.io/reunion-monitor/) |
| 📄 **Code source** | [index.html](https://github.com/gunout/reunion-monitor/blob/main/index.html) |
| 🐛 **Signaler un bug** | [Issues](https://github.com/gunout/reunion-monitor/issues) |
| 💡 **Proposer une idée** | [Discussions](https://github.com/gunout/reunion-monitor/discussions) |
| ⭐ **Mettre une étoile** | [Star le repo](https://github.com/gunout/reunion-monitor) |

---

## 📖 Table des matières

- [Aperçu](#-aperçu)
- [Fonctionnalités](#-fonctionnalités)
- [Démos intégrées](#-démos-intégrées)
- [Architecture](#-architecture)
- [Installation](#-installation)
- [Déploiement](#-déploiement)
- [Utilisation](#-utilisation)
- [Personnalisation](#-personnalisation)
- [Compatibilité](#-compatibilité)
- [Limitations](#-limitations)
- [Contribuer](#-contribuer)
- [Licence](#-licence)
- [Remerciements](#-remerciements)

---

## 🌟 Aperçu

**Reunion Monitor** est un dashboard sombre (dark theme) qui :

- **Détecte automatiquement** toutes mes démos en ligne hébergées sur GitHub Pages, Vercel, Netlify ou tout autre hébergeur
- **Affiche chaque démo directement dans une iframe intégrée** — pas de redirection, l'utilisateur reste dans le monitor
- **Organise les travaux par catégories** : Météo, Mer & Sécurité, Immobilier, Formation, Transport, Environnement…
- **Fournit un panneau d'intelligence** : statistiques, top démos, répartition, statut live

### Interface inspirée de World Monitor

| Élément | Description |
|---------|-------------|
| 🎨 **Thème sombre** | Fond `#050810`, panneaux `#0f1624`, accent cyan `#00e5ff` |
| 📊 **3 colonnes** | Sidebar gauche · Iframe centrale · Intelligence droite |
| 🔴 **Live indicators** | Points pulsants verts pour les démos actives |
| 📡 **Panneaux empilés** | Statistiques, top, catégories, système |
| 🖥️ **Iframe plein écran** | Chaque démo s'affiche dans le panneau central |

---

## ✨ Fonctionnalités

### 🎯 Détection automatique des démos
- Récupère **tous les repos publics** de `@gunout` via l'API GitHub REST
- Détecte ceux qui ont un `homepage` ou `has_pages` activé
- Détecte automatiquement ceux liés à La Réunion via mots-clés (reunion, 974, drom, cyclone, requin…)

### 🖥️ Affichage en iframe intégré
- **Mode « Travail actif »** : une démo affichée en plein écran dans l'iframe centrale
- **Mode « Tous les aperçus »** : grille de miniatures live (iframe réduit à 50%)
- Chargement avec spinner animé
- Détection automatique des protections anti-iframe (X-Frame-Options, CSP)
- Fallback : bouton d'ouverture dans un nouvel onglet

### 📚 Sidebar interactive
- Liste complète des démos avec icône, catégorie et statut
- **Recherche instantanée** (nom, description, catégorie)
- **Filtres par catégorie** avec compteurs

### 🎛️ Contrôles du travail actif
- 🔄 **Recharger** l'iframe
- 🔍 **Zoom** (agrandit l'iframe à 115%)
- 🚀 **Ouvrir** dans un onglet
- 📦 **Voir le code** sur GitHub

### 📈 Panneau Intelligence (droite)
- **Travail actif** : nom, catégorie, langage, statut
- **Statistiques globales** : total, catégories, stars, langages
- **Top démos** : classement par étoiles
- **Catégories** : répartition avec barres de progression
- **Système** : source, user, MAJ, mode actuel

---

## 📦 Démos intégrées

Le monitor intègre actuellement **32 démos en ligne** liées à La Réunion :

### 🌴 Météo & Environnement
| # | Démo | Catégorie | Statut |
|---|------|-----------|--------|
| 1 | Météo Réunion | Météo | ✅ LIVE |
| 2 | Assainissement Réunion | Environnement | ✅ LIVE |
| 3 | Vigie Requins | Mer & Sécurité | ✅ LIVE |

### 🏠 Immobilier & Accessibilité
| # | Démo | Catégorie | Statut |
|---|------|-----------|--------|
| 4 | Accessibilité Immobilière Réunion | Immobilier | ✅ LIVE |

### 🎓 Formation & Social
| # | Démo | Catégorie | Statut |
|---|------|-----------|--------|
| 5 | Dashboard CPF Réunion | Formation | ✅ LIVE |

### 🚄 Transport & Mobilité
| # | Démo | Catégorie | Statut |
|---|------|-----------|--------|
| 6 | Reunion Express | Transport | ✅ LIVE |
| 7 | Radar Aérien EU | Transport aérien | ✅ LIVE |

> *(Les 25 autres démos sont détectées automatiquement depuis GitHub)*

---

## 🏗️ Architecture

```
reunion-monitor/
├── index.html              # Dashboard complet (fichier unique)
├── README.md               # Ce fichier
├── LICENSE                 # Licence MIT
└── screenshots/            # Captures d'écran (optionnel)
    ├── single-view.png
    ├── grid-view.png
    └── mobile.png
```

### Structure du code (`index.html`)

```
├── <head>
│   └── Styles CSS (thème sombre, World Monitor style)
├── <body>
│   ├── Topbar (navigation + stats)
│   └── App 3 colonnes
│       ├── Sidebar gauche (liste + filtres + recherche)
│       ├── Centre (iframe + contrôles + grille aperçus)
│       └── Panneau droit (intelligence + stats)
└── <script>
    ├── Configuration (GITHUB_USERNAME, DEMOS, ICON_RULES)
    ├── API GitHub (fetch repos)
    ├── Détection démos (homepage + has_pages)
    ├── Rendu iframe (chargement + anti-iframe detection)
    ├── Rendu grille (aperçus live miniatures)
    └── Événements (navigation, filtres, modes)
```

---

## 🚀 Installation

### Prérequis
Aucun — le monitor est **100 % client-side** (HTML + CSS + JavaScript pur).

### Option 1 : Cloner le dépôt

```bash
git clone https://github.com/gunout/reunion-monitor.git
cd reunion-monitor
```

Puis ouvrez `index.html` dans un navigateur moderne.

### Option 2 : Hébergement local

```bash
# Avec Python
python -m http.server 8000

# Avec Node.js
npx serve

# Puis ouvrir http://localhost:8000
```

---

## 🚢 Déploiement

Le monitor est **100 % statique** (un seul fichier `index.html`).

### ⭐ GitHub Pages (recommandé)

**Déploiement automatique à chaque `push` sur `main`.**

**URL de production** : [https://gunout.github.io/reunion-monitor/](https://gunout.github.io/reunion-monitor/)

Activation manuelle :
1. **Settings → Pages**
2. Source : **Deploy from a branch**
3. Branch : `main` / `/ (root)`
4. **Save**

### ▲ Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/gunout/reunion-monitor)

### 🟢 Netlify

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/gunout/reunion-monitor)

---

## 💡 Utilisation

### Navigation principale

| Onglet | Description |
|--------|-------------|
| 🖥️ **Travail actif** | Affiche une démo en plein écran dans l'iframe |
| 🔲 **Tous les aperçus** | Grille de miniatures live de toutes les démos |

### Interactions

- **Clic sur une démo** dans la sidebar → affichage immédiat dans l'iframe
- **Recherche** → filtre en temps réel
- **Filtres catégorie** → restreint l'affichage
- **🔄 Recharger** → force le rechargement de l'iframe
- **🔍 Zoom** → agrandit la vue de l'iframe
- **🚀 Ouvrir** → ouvre la démo dans un nouvel onglet

### Raccourcis clavier *(à venir)*

| Touche | Action |
|--------|--------|
| `↑` / `↓` | Navigation entre les démos |
| `Entrée` | Ouvrir la démo active |
| `/` | Focus sur la recherche |
| `Échap` | Fermer la recherche |

---

## 🎨 Personnalisation

### Ajouter une démo manuellement

Modifie le tableau `DEMOS` dans `index.html` :

```javascript
const DEMOS = [
  {
    id: 1,
    name: 'Météo Réunion',
    repo: 'meteo-reunion',
    url: 'https://gunout.github.io/meteo-reunion/',
    icon: '🌴',
    color: '#00ff88',
    category: 'Météo',
    description: 'Dashboard météo temps réel des 24 communes.'
  },
  // ... ajoute ici
];
```

### Modifier les couleurs

Dans le `<style>`, modifie les variables CSS :

```css
:root {
  --bg-0: #050810;      /* Fond principal */
  --cyan: #00e5ff;      /* Accent live */
  --green: #00ff88;     /* Statut LIVE */
  --red: #ff3b3b;       /* Alertes */
  --amber: #ffb800;     /* Warnings */
}
```

### Ajouter un token GitHub

Pour passer de 60 à 5000 requêtes/heure :

1. GitHub → Settings → Developer settings → Tokens → **Generate new token**
2. Scope : `public_repo` uniquement
3. Colle-le dans :

```javascript
const GITHUB_TOKEN = 'ghp_xxxxxxxxxxxxxxxxxxxx';
```

---

## 📱 Compatibilité

### Navigateurs

| Navigateur | Version min |
|------------|-------------|
| Chrome / Edge | 90+ |
| Firefox | 88+ |
| Safari | 14+ |
| Opera | 76+ |

### Écrans

| Type | Largeur | Comportement |
|------|---------|--------------|
| 📱 Mobile | 320 – 639 px | 1 colonne, sidebar en haut |
| 💻 Tablette | 640 – 1023 px | 2 colonnes |
| 🖥️ Desktop | 1024 – 1599 px | 3 colonnes |
| 🖥️ 4K | 1920 px+ | 3 colonnes élargies |

---

## ⚠️ Limitations

### Iframes bloquées

Certains sites déploient des protections anti-iframe :

- **X-Frame-Options: DENY** ou **SAMEORIGIN**
- **Content-Security-Policy** avec `frame-ancestors`
- **Cookies SameSite** stricts

**GitHub Pages n'ajoute PAS ces en-têtes** → ✅ tes démos s'afficheront bien

**Si une démo bloque**, le monitor :
1. Détecte après 8 secondes
2. Affiche un message d'information
3. Propose un lien direct d'ouverture

### Pour forcer l'intégration sur tes propres sites

Ajoute dans ton `_headers` ou config Vercel/Netlify :

```
Content-Security-Policy: frame-ancestors *
X-Frame-Options: ALLOWALL
```

### Limite API GitHub

- **60 requêtes/heure** sans token
- **5000 requêtes/heure** avec token personnel

Le monitor charge les données **une seule fois au démarrage** (pas de polling), donc cette limite n'est pas un problème en usage normal.

---

## 🤝 Contribuer

Les contributions sont les bienvenues !

1. **Fork** : [github.com/gunout/reunion-monitor/fork](https://github.com/gunout/reunion-monitor/fork)
2. **Créer une branche** : `git checkout -b feature/ma-fonctionnalite`
3. **Commit** : `git commit -m 'Ajout nouvelle fonctionnalité'`
4. **Push** : `git push origin feature/ma-fonctionnalite`
5. **Pull Request**

### Idées d'amélioration

- [ ] Raccourcis clavier (navigation ↑↓, recherche `/`)
- [ ] Mode comparaison (2 iframes côte à côte)
- [ ] Historique de navigation
- [ ] Favoris (localStorage)
- [ ] Export JSON du catalogue
- [ ] Notifications quand une démo tombe
- [ ] Détection automatique du statut HTTP (200/404)
- [ ] Cache local des métadonnées GitHub
- [ ] PWA (installation mobile)
- [ ] Mode clair

---

## 📄 Licence

Ce projet est sous licence **MIT** — voir [LICENSE](https://github.com/gunout/reunion-monitor/blob/main/LICENSE).

```
MIT License

Copyright (c) 2025-2026 Gunout

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🙏 Remerciements

- **[GitHub REST API](https://docs.github.com/en/rest)** — Récupération des repos et métadonnées
- **[World Monitor](https://github.com/koala73/worldmonitor)** — Inspiration pour le design et l'organisation
- **La Réunion** 🌴 et son écosystème numérique
- **Tous les projets open-source** qui ont inspiré ce monitor

---

## 📞 Contact

- **GitHub** : [@gunout](https://github.com/gunout)
- **Issues** : [github.com/gunout/reunion-monitor/issues](https://github.com/gunout/reunion-monitor/issues)
- **Discussions** : [github.com/gunout/reunion-monitor/discussions](https://github.com/gunout/reunion-monitor/discussions)

---

<div align="center">

**🇷🇪 Fait pour La Réunion 🇷🇪**

[⬆ Retour en haut](#-reunion-monitor--dashboard-des-travaux-numériques-réunion)

### Gunout · 2026

© 2026 **Gunout** — Tous droits réservés.

</div>
