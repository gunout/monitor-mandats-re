# 🇷🇪 Monitor Mandats Réunion — Dashboard Maires 974

**Visualisation interactive des mandats municipaux des 24 communes de La Réunion depuis 1950.**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=for-the-badge&logo=chart.js&logoColor=white)
![Leaflet](https://img.shields.io/badge/Leaflet-199900?style=for-the-badge&logo=leaflet&logoColor=white)
![PapaParse](https://img.shields.io/badge/PapaParse-FF6B35?style=for-the-badge&logo=databricks&logoColor=white)

![License MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)
![Data CC0](https://img.shields.io/badge/Data-CC--Zero-lightgrey.svg?style=for-the-badge)
![Data.gouv.fr](https://img.shields.io/badge/Source-data.gouv.fr-000091?style=for-the-badge)
![Made in Réunion](https://img.shields.io/badge/Made%20in-La%20Réunion%20974-0066CC?style=for-the-badge)

![GitHub last commit](https://img.shields.io/github/last-commit/gunout/monitor-mandats-re?style=for-the-badge)
![GitHub repo size](https://img.shields.io/github/repo-size/gunout/monitor-mandats-re?style=for-the-badge)
![GitHub stars](https://img.shields.io/github/stars/gunout/monitor-mandats-re?style=for-the-badge)

---

## 📖 À propos

Ce dashboard interactif permet d'explorer et d'analyser **l'histoire politique des 24 communes de La Réunion** à travers les mandats de leurs maires, depuis 1950 (voire 1900 pour certaines mairies).

Les données proviennent du jeu de données ouvert **"Mandats des maires de La Réunion"** publié sur [data.gouv.fr](https://www.data.gouv.fr/fr/datasets/mandats-des-maires-de-la-reunion/) sous licence **CC-Zero**.

### 🎯 Objectifs

- 🗺️ **Cartographier** la répartition géographique des mandats
- 📊 **Analyser** l'évolution temporelle (décennies, timeline)
- ⚖️ **Mesurer** la parité hommes/femmes dans le temps
- 🏛️ **Comparer** les communes et intercommunalités
- 👤 **Retracer** la carrière des maires les plus marquants

---

## 🚀 Démo

Le dashboard se lance localement dans le navigateur. Aucun backend n'est requis : tout se passe côté client grâce à PapaParse pour lire les CSV et Chart.js / Leaflet pour les visualisations.

### Aperçu des vues

| Vue | Description |
|-----|-------------|
| 📋 Mandats | Liste paginée et filtrable de tous les mandats |
| 🗺️ Carte | Carte interactive Leaflet avec cercles proportionnels |
| 📊 Graphiques | 7 visualisations (décennies, parité, timeline, heatmap…) |
| 👤 Maires | Classement des maires par nombre de mandats |
| 📄 JSON brut | Aperçu des données filtrées |

---

## ✨ Fonctionnalités

### 🎛️ Filtres interactifs

- 🔍 **Recherche libre** (maire, commune, intercommunalité)
- 🏘️ **Filtre par commune** (24 disponibles)
- 🏛️ **Filtre par intercommunalité** (CIVIS, CASUD, CIREST, TO, CINOR)
- ⚖️ **Filtre par genre** (Hommes / Femmes)
- 📅 **Filtre par période** (année min / max)
- 🔄 **Tri** (récents, anciens, alphabétique)

### 📊 Visualisations

| Graphique | Type | Description |
|-----------|------|-------------|
| Mandats par décennie | Barres | Répartition temporelle |
| Évolution de la parité H/F | Aires empilées | Progression femmes/hommes |
| Timeline des mandats | Ligne | Mandats débutés par an |
| Mandats par intercommunalité | Barres horizontales | Répartition par EPCI |
| Répartition H/F globale | Doughnut | Ratio global |
| Top 10 des communes | Barres horizontales | Classement |
| Distribution des durées | Histogramme | Analyse des mandats |
| Heatmap communes × décennies | Table custom | Densité temporelle |

### 🗺️ Carte interactive

- Tuiles **OpenStreetMap** (aucune clé API requise)
- **Cercles proportionnels** au nombre de mandats
- **Dégradé de couleurs** (bleu → orange → rouge)
- **Popups** détaillés au clic

### 🧠 Colonne Intelligence

- 💚 État du monitor en temps réel
- 📊 Statistiques filtrées
- 🏆 Top 5 communes et maires
- ⚙️ Configuration

### 🪟 Modal profil maire

- 👤 Identité complète
- 🏛️ Communes administrées
- 📅 Chronologie de tous les mandats

### 📥 Exports

- **JSON** filtré
- **CSV** filtré (compatible Excel / LibreOffice)

---

## 📦 Installation

### Prérequis

- Un navigateur moderne (Chrome, Firefox, Edge, Safari)
- **Python 3** ou **Node.js** (pour le serveur local)

### 📁 Structure du projet

| Chemin | Type | Description |
|--------|------|-------------|
| `index.html` | Fichier | Dashboard complet (HTML + CSS + JS intégrés) |
| `README.md` | Fichier | Documentation du projet |
| `LICENSE` | Fichier | Licence MIT |
| `data/` | Dossier | Contient les 4 fichiers CSV sources |
| `data/communes.csv` | Fichier | 24 communes (code INSEE, nom, interco) |
| `data/intercommunalites.csv` | Fichier | 5 EPCI (SIREN, nom, nom_court) |
| `data/maires.csv` | Fichier | Liste des maires (nom, prénom, genre…) |
| `data/mandats.csv` | Fichier | Mandats (code INSEE, maire, dates) |

### 🚀 Lancement

**Option 1 — Python (recommandé)**

```bash
git clone https://github.com/gunout/monitor-mandats-re.git
cd monitor-mandats-re
python -m http.server 8000
```

Puis ouvrez : **http://localhost:8000**

**Option 2 — Node.js**

```bash
npx serve
```

**Option 3 — VS Code**

Installez l'extension **Live Server**, puis clic droit sur `index.html` → **Open with Live Server**.

> ⚠️ Ne pas ouvrir `index.html` en double-cliquant dessus ! Le protocole `file://` bloque le chargement des CSV.

---

## 📊 Source des données

### 🏛️ Producteur

- **Producteur** : [SysDevRun](https://www.sys-dev-run.fr/)
- **Contact** : contact@sys-dev-run.fr
- **Site de navigation** : [maires.sys-dev-run.re](https://maires.sys-dev-run.re/)

### 📄 Fichiers

| Fichier | Lignes | Colonnes principales | Taille |
|---------|--------|----------------------|--------|
| communes.csv | 24 | code_insee, nom, interco | 605 o |
| intercommunalites.csv | 5 | siren, nom, nom_court | 295 o |
| maires.csv | ~200 | nom, prenom, date_naissance, genre | 5 Ko |
| mandats.csv | ~300 | code_insee, nom_commune, nom_maire, date_debut, date_fin | 27 Ko |

### 📅 Couverture

- **Temporelle** : 1900 → aujourd'hui
- **Spatiale** : Département de La Réunion (974)
- **Licence** : [CC-Zero](https://creativecommons.org/publicdomain/zero/1.0/)

### 🔗 Accès API

**API Tabulaire (JSON)**

```
https://tabular-api.data.gouv.fr/api/resources/{RESOURCE_ID}/data/json/
```

| Ressource | Resource ID |
|-----------|-------------|
| Communes | ad481c6f-a54f-4016-858a-c573168bc364 |
| Intercommunalités | 6a9f0f30-5c18-417a-a093-eb833cfdc608 |
| Maires | b7a25167-be52-4d9f-bb23-7214729ed01b |
| Mandats | b72e2765-6414-41e4-a521-a21b6de2775e |

**CSV direct**

```
https://maires.sys-dev-run.re/data/{fichier}.csv
```

---

## 🛠️ Stack technique

| Technologie | Usage | Version |
|-------------|-------|---------|
| HTML5 | Structure | 5 |
| CSS3 | Design (DSFR-inspired) | 3 |
| JavaScript | Logique applicative | ES2020+ |
| Chart.js | Graphiques | 4.4.0 |
| Leaflet | Cartographie | 1.9.4 |
| PapaParse | Parsing CSV | 5.4.1 |

### 🎨 Design system

Inspiré du **Système de Design de l'État (DSFR)** :

- 🎨 Palette officielle (bleu France, rouge Marianne, or)
- 🇫🇷 Bandeau tricolore en en-tête
- 🔤 Typographie Marianne
- 📐 Composants accessibles

---

## 📱 Responsive

| Breakpoint | Comportement |
|------------|--------------|
| 🖥️ > 1200px | Layout 3 colonnes complet |
| 💻 900–1200px | Colonnes réduites |
| 📱 < 900px | Empilement vertical |

---

## 📂 Organisation du code

| Section | Rôle |
|---------|------|
| `CONFIG` | Fichiers CSV + coordonnées des communes |
| `Utils` | escapeHtml, normalize, formatUptime… |
| `loadData()` | Chargement CSV via PapaParse |
| `prepareData()` | Enrichissement / jointures entre fichiers |
| `applyFilters()` | Filtrage multicritère |
| `renderKPIs()` | 6 indicateurs clés |
| `renderResults()` | Liste paginée des mandats |
| `renderMapView()` | Carte Leaflet |
| `renderChartsView()` | 6 graphiques Chart.js |
| `renderCustomHeatmap()` | Heatmap HTML/CSS |
| `renderMairesView()` | Agrégat par maire |
| `showMaireModal()` | Modal profil maire |
| `exportJson()` / `exportCsv()` | Exports filtrés |

---

## 🐛 Résolution de problèmes

### ❌ Impossible de charger data/xxx.csv

**Cause** : ouverture du fichier en `file://`.

**Solution** : lancer un serveur local.

```bash
python -m http.server 8000
```

### ❌ La carte ne s'affiche pas

**Cause** : tuiles bloquées ou cache navigateur.

**Solution** :

1. Vérifier la connexion Internet
2. Forcer le rechargement : `Ctrl + Shift + R` (Windows) / `Cmd + Shift + R` (Mac)
3. Les tuiles OSM ne nécessitent aucune clé API

### ❌ Les graphiques sont vides

**Cause** : les noms de colonnes CSV ne correspondent pas.

**Solution** :

1. Ouvrir la console (F12)
2. Chercher les logs `✅ data/xxx.csv : N lignes`
3. Si `0 lignes`, vérifier le séparateur CSV (`,` vs `;`)
4. Ajuster le code si les colonnes diffèrent

### ❌ Heatmap absente

**Cause** : ancienne version Chart.js buggée.

**Solution** : la heatmap est en HTML/CSS pur (fiable sur tous les navigateurs). Rechargez avec `Ctrl + Shift + R`.

---

## 🎯 Feuille de route

- [x] Dashboard fonctionnel
- [x] Carte interactive sans clé API
- [x] Heatmap custom
- [x] Exports JSON / CSV
- [x] Modal profil maire
- [ ] Comparateur de 2 communes côte à côte
- [ ] Mode clair / sombre
- [ ] Export PDF
- [ ] Autocomplétion maire
- [ ] PWA (hors-ligne)
- [ ] Internationalisation (FR / EN / CR)

---

## 🤝 Contribution

Les contributions sont les bienvenues !

1. Forkez le projet
2. Créez une branche : `git checkout -b feature/ma-fonctionnalite`
3. Committez : `git commit -m 'Ajout de ma fonctionnalité'`
4. Pushez : `git push origin feature/ma-fonctionnalite`
5. Ouvrez une Pull Request

---

## 📜 Licence

**Code** : MIT — voir [LICENSE](LICENSE)

**Données** : CC-Zero

---

## 🙏 Remerciements

- 🏛️ [SysDevRun](https://www.sys-dev-run.fr/) — Producteur du jeu de données
- 🇫🇷 [data.gouv.fr](https://www.data.gouv.fr/) — Plateforme Open Data
- 🗺️ [OpenStreetMap](https://www.openstreetmap.org/) — Fond de carte
- 📊 [Chart.js](https://www.chartjs.org/) — Graphiques
- 🗺️ [Leaflet](https://leafletjs.com/) — Cartographie
- 🎨 [DSFR](https://www.systeme-de-design.gouv.fr/) — Inspiration design

---

**Fait avec ❤️ à La Réunion** 🇷🇪

---

<div align="center">

### 🇫🇷 Gunout · 2026

![Made in France](https://img.shields.io/badge/Made_in-France-002395?style=flat-square&labelColor=FFFFFF&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA5MDAgNjAwIj48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjYwMCIgZmlsbD0iIzAwMjM5NSIvPjxyZWN0IHdpZHRoPSI5MDAiIGhlaWdodD0iNDAwIiB5PSIxMDAiIGZpbGw9IiNmZmYiLz48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjIwMCIgeT0iNDAwIiBmaWxsPSIjZWQyOTM5Ii8+PC9zdmc+)
![GitHub](https://img.shields.io/badge/GitHub-gunout-181717?style=flat-square&logo=github&logoColor=white)
![Year](https://img.shields.io/badge/2026-ED2939?style=flat-square&labelColor=FFFFFF)

<sub>© 2026 <strong>Gunout</strong> — Tous droits réservés.</sub>

</div>
