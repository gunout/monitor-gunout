# 🇷🇪 Reunion Monitor — Dashboard des travaux numériques Réunion

> **Monitor temps réel** qui intègre et affiche directement **toutes mes démos en ligne liées à La Réunion** dans une interface type *World Monitor* : iframes intégrées, panneaux d'intelligence, sidebar interactive et détection automatique via l'API GitHub.

[![Site live](https://img.shields.io/badge/site-live-00ff88?logo=github)](https://gunout.github.io/monitor-gunout/)
[![GitHub repo](https://img.shields.io/badge/GitHub-gunout%2Fmonitor--gunout-blue?logo=github)](https://github.com/gunout/monitor-gunout)
[![Version](https://img.shields.io/badge/version-1.0-blue)](https://github.com/gunout/monitor-gunout)
[![Licence](https://img.shields.io/badge/licence-MIT-red)](https://github.com/gunout/monitor-gunout/blob/main/LICENSE)
[![Démos](https://img.shields.io/badge/d%C3%A9mos-64%20en%20ligne-green)](https://gunout.github.io/monitor-gunout/)
[![Responsive](https://img.shields.io/badge/responsive-mobile%20%7C%20tablette%20%7C%204K-informational)](https://gunout.github.io/monitor-gunout/)
[![Theme](https://img.shields.io/badge/theme-dark%20%2F%20cyan-black)](https://gunout.github.io/monitor-gunout/)
[![Statut](https://img.shields.io/badge/statut-production-success)](https://gunout.github.io/monitor-gunout/)

---

## 🔗 Liens rapides

| Ressource | Lien |
|-----------|------|
| 🌐 **Démo en ligne** | [gunout.github.io/monitor-gunout](https://gunout.github.io/monitor-gunout/) |
| 📦 **Dépôt GitHub** | [github.com/gunout/monitor-gunout](https://github.com/gunout/monitor-gunout) |
| 📄 **Code source** | [index.html](https://github.com/gunout/monitor-gunout/blob/main/index.html) |
| 🐛 **Signaler un bug** | [Issues](https://github.com/gunout/monitor-gunout/issues) |
| 💡 **Proposer une idée** | [Discussions](https://github.com/gunout/monitor-gunout/discussions) |
| ⭐ **Mettre une étoile** | [Star le repo](https://github.com/gunout/monitor-gunout) |

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
- [Roadmap](#-roadmap)
- [Contribuer](#-contribuer)
- [Licence](#-licence)
- [Remerciements](#-remerciements)

---

## 🌟 Aperçu

**Reunion Monitor** est un dashboard **sombre et dense** qui :

- **Détecte automatiquement** toutes mes démos en ligne hébergées sur GitHub Pages, Vercel, Netlify ou tout autre hébergeur
- **Affiche chaque démo directement dans une iframe intégrée** — pas de redirection, l'utilisateur reste dans le monitor
- **Organise les travaux par catégories** : Météo, Mer & Sécurité, Immobilier, Formation, Transport, Environnement…
- **Fournit un panneau d'intelligence** : statistiques en direct, top démos, répartition, statut live

### 🌐 Accès direct

👉 **Voir le monitor en direct** : [gunout.github.io/monitor-gunout](https://gunout.github.io/monitor-gunout/)

### 🎨 Interface inspirée de World Monitor

| Élément | Description |
|---------|-------------|
| 🎨 **Thème sombre** | Fond `#050810`, panneaux `#0f1624`, accent cyan `#00e5ff` |
| 📊 **3 colonnes** | Sidebar gauche · Iframe centrale · Intelligence droite |
| 🔴 **Live indicators** | Points pulsants verts pour les démos actives |
| 📡 **Panneaux empilés** | Statistiques, top démos, catégories, système |
| 🖥️ **Iframe plein écran** | Chaque démo s'affiche dans le panneau central |

---

## ✨ Fonctionnalités

### 🎯 Détection automatique des démos
- Récupère **tous les repos publics** de `@gunout` via l'API GitHub REST
- Détecte ceux qui ont un `homepage` ou `has_pages` activé
- Détecte automatiquement ceux liés à La Réunion via mots-clés (reunion, 974, drom, cyclone, requin…)
- **64 démos détectées** automatiquement au démarrage

### 🖥️ Affichage en iframe intégré
- **Mode « Travail actif »** : une démo affichée en plein écran dans l'iframe centrale
- **Mode « Tous les aperçus »** : grille de miniatures live (iframe réduit à 50%)
- Chargement avec spinner animé
- Détection automatique des protections anti-iframe (X-Frame-Options, CSP)
- Fallback : bouton d'ouverture dans un nouvel onglet

### 📚 Sidebar interactive
- Liste complète des démos avec icône, catégorie et statut
- **Recherche instantanée** (nom, description, catégorie)
- **Filtres par catégorie** avec compteurs dynamiques

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
- **Système** : source, user, dernière MAJ, mode actuel

---

## 📦 Démos intégrées

Le monitor intègre actuellement **64 démos en ligne** liées à La Réunion.

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

### 📊 Autres catégories (détection automatique)
Énergie · Politique · Santé · Science · Média · Data · Éducation…

> *Les autres démos sont détectées automatiquement depuis GitHub et catégorisées par mots-clés.*

---

## 🏗️ Architecture

```
monitor-gunout/
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
│   └── Styles CSS (thème sombre World Monitor, responsive)
├── <body>
│   ├── Topbar (navigation onglets + stats live)
│   └── App 3 colonnes
│       ├── Sidebar gauche (liste démos + filtres + recherche)
│       ├── Centre (iframe + contrôles + grille aperçus)
│       └── Panneau droit (intelligence + stats)
└── <script>
    ├── Configuration (GITHUB_USERNAME, DEMOS, ICON_RULES)
    ├── API GitHub (fetch repos avec pagination)
    ├── Détection démos (homepage + has_pages)
    ├── Rendu iframe (chargement + anti-iframe detection + timeout)
    ├── Rendu grille (aperçus live miniatures)
    └── Événements (navigation, filtres, modes)
```

---

## 🚀 Installation

### Prérequis
Aucun — le monitor est **100 % client-side** (HTML + CSS + JavaScript pur).

### Option 1 : Cloner le dépôt

```bash
git clone https://github.com/gunout/monitor-gunout.git
cd monitor-gunout
```

Puis ouvrez `index.html` dans un navigateur moderne.

### Option 2 : Télécharger directement

Téléchargez [index.html](https://github.com/gunout/monitor-gunout/blob/main/index.html) et ouvrez-le dans un navigateur.

### Option 3 : Hébergement local

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

### ⭐ GitHub Pages (déjà configuré)

**Déploiement automatique à chaque `push` sur `main`.**

**URL de production** : [https://gunout.github.io/monitor-gunout/](https://gunout.github.io/monitor-gunout/)

Activation manuelle :
1. **Settings → Pages**
2. Source : **Deploy from a branch**
3. Branch : `main` / `/ (root)`
4. **Save**

### ▲ Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/gunout/monitor-gunout)

```bash
npm i -g vercel
vercel
```

### 🟢 Netlify

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/gunout/monitor-gunout)

```bash
npm i -g netlify-cli
netlify deploy --prod
```

### ☁️ Cloudflare Pages

1. [pages.cloudflare.com](https://pages.cloudflare.com)
2. Connecter GitHub → `gunout/monitor-gunout`
3. Build : *(laisser vide)* · Output : `/`
4. **Save and Deploy**

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
- **🔍 Zoom** → agrandit la vue de l'iframe (115%)
- **🚀 Ouvrir** → ouvre la démo dans un nouvel onglet
- **📦 Code** → accède au repo GitHub

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

### Exclure une démo du monitor

Pour éviter l'auto-référence (le monitor ne doit pas s'afficher lui-même) :

```javascript
const SELF_REPOS = ['monitor-gunout'];
```

### Modifier les couleurs

Dans le `<style>`, modifie les variables CSS :

```css
:root {
  --bg-0: #050810;      /* Fond principal */
  --bg-1: #0a0f1a;      /* Fond secondaire */
  --cyan: #00e5ff;      /* Accent live */
  --green: #00ff88;     /* Statut LIVE */
  --red: #ff3b3b;       /* Alertes */
  --amber: #ffb800;     /* Warnings */
  --purple: #a855f7;    /* Accent secondaire */
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

**GitHub Pages n'ajoute PAS ces en-têtes** → ✅ tes démos s'affichent bien

**Si une démo bloque**, le monitor :
1. Détecte après **15 secondes** (timeout étendu)
2. Affiche un message d'information
3. Propose un lien direct d'ouverture

### Auto-référence

Le monitor **s'exclut automatiquement** de la liste des démos pour éviter une boucle infinie (un site ne peut pas s'afficher lui-même dans son propre iframe).

### Limite API GitHub

- **60 requêtes/heure** sans token
- **5000 requêtes/heure** avec token personnel

Le monitor charge les données **une seule fois au démarrage** (pas de polling), donc cette limite n'est pas un problème en usage normal.

### Pour forcer l'intégration sur tes propres sites

Ajoute dans ton `_headers` ou config Vercel/Netlify :

```
Content-Security-Policy: frame-ancestors *
X-Frame-Options: ALLOWALL
```

---

## 🗺️ Roadmap

### Version 1.1 (prochaine)
- [ ] Exclusion automatique du monitor lui-même
- [ ] Timeout étendu à 15s pour les iframes lentes
- [ ] Détection intelligente des vraies erreurs (pas juste la lenteur)

### Version 1.2
- [ ] Raccourcis clavier (navigation ↑↓, recherche `/`, `Échap`)
- [ ] Mode comparaison (2 iframes côte à côte)
- [ ] Historique de navigation (retour / suivant)
- [ ] Favoris (localStorage)

### Version 2.0
- [ ] Test réel du statut HTTP (200 / 404)
- [ ] Cache local des métadonnées GitHub
- [ ] PWA (installation mobile + service worker)
- [ ] Mode clair
- [ ] Notifications quand une démo tombe

---

## 🤝 Contribuer

Les contributions sont les bienvenues !

1. **Fork** : [github.com/gunout/monitor-gunout/fork](https://github.com/gunout/monitor-gunout/fork)
2. **Créer une branche** : `git checkout -b feature/ma-fonctionnalite`
3. **Commit** : `git commit -m 'Ajout nouvelle fonctionnalité'`
4. **Push** : `git push origin feature/ma-fonctionnalite`
5. **Pull Request**

### Idées d'amélioration

- [ ] Détection automatique du statut HTTP live
- [ ] Système de tags personnalisés
- [ ] Vue timeline (chronologie des déploiements)
- [ ] Recherche avancée avec opérateurs (`cat:meteo lang:js`)
- [ ] Export du catalogue en JSON
- [ ] Widget embarquable pour sites tiers
- [ ] Mode présentation (plein écran sans UI)

---

## 📄 Licence

Ce projet est sous licence **MIT** — voir [LICENSE](https://github.com/gunout/monitor-gunout/blob/main/LICENSE).

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
- **Site** : [gunout.github.io/monitor-gunout](https://gunout.github.io/monitor-gunout/)
- **Issues** : [github.com/gunout/monitor-gunout/issues](https://github.com/gunout/monitor-gunout/issues)
- **Discussions** : [github.com/gunout/monitor-gunout/discussions](https://github.com/gunout/monitor-gunout/discussions)

---

<div align="center">

**🇷🇪 Fait avec ❤️ pour La Réunion 🇷🇪**

[⬆ Retour en haut](#-reunion-monitor--dashboard-des-travaux-numériques-réunion)

### Gunout · 2026

© 2026 **Gunout** — Tous droits réservés.

</div>
