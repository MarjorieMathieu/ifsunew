# IFSU Équilibre — ifsu-equilibre.be

Site de Marjorie Mathieu — Yoga Viniyoga & Méditation Védique IFSU  
Ath, Hainaut, Belgique

---

## Structure

```
/
├── index.html          # Accueil — vidéo + résumés + liens vers chaque section
├── yoga.html           # Yoga Viniyoga — horaires, tarifs, qui suis-je
├── meditation.html     # Méditation Védique IFSU — méthode, parcours, FAQ
├── ateliers.html       # Ateliers 3h, Solstice, Causeries mensuelles
├── retraite.html       # Retraite novembre 2026 — Koningsteen
└── style.css           # Feuille de style partagée
```

Pas de dossier `images/` — tous les assets (photos et vidéo) sont embarqués en base64 directement dans les fichiers HTML. Le site est auto-suffisant : aucune dépendance externe de fichiers locaux.

---

## Déploiement GitHub Pages

1. Pusher tous les fichiers à la racine du dépôt
2. Dans les Settings du dépôt → Pages → Source : `main` / `root`
3. Le domaine personnalisé `ifsu-equilibre.be` est configuré via le fichier `CNAME`

```
# CNAME (à créer si absent)
ifsu-equilibre.be
```

---

## Assets embarqués

| Fichier source | Page | Rôle |
|---|---|---|
| `8480746-hd_1920_1080_25fps.mp4` | index.html | Vidéo hero accueil (autoplay, muted, loop) |
| `cours_prive_.jpeg` | yoga.html | Photo séance privée (max-height 320px) |
| `krishnamacharya_page_yoga.jpg` | yoga.html | Portrait Krishnamacharya + bloc lignée |
| `qui_suis-je.png` | yoga.html | Portrait Marjorie — section formation |
| `qui_suis-je1.png` | yoga.html | Portrait Marjorie — bannière citation |
| `relaxation.jpeg` | yoga.html | Photo relaxation avant CTA |
| `cours_collectif.jpg` | ateliers.html | Photo ambiance cours |
| `IFSUEQUIILBREMED.webp` | meditation.html | Photo ambiance méditation |
| `Gururaj_Ananda_yogi_page_me_ditatio.jpg` | meditation.html | Portrait Gururaj Ananda Yogi |
| `vivekananda_page_me_ditation.jpg` | meditation.html | Portrait Vivekananda |
| `koningsteen1.webp` | retraite.html | Photo hero fond (bâtiment dans les arbres) |
| `IFSU-RETRAITE.png` | retraite.html | Vue du domaine Koningsteen |
| `Tuinzaal.webp` | retraite.html | Salle de pratique Tuinzaal |
| `IFSU-RETRAITE1.webp` | retraite.html | Salle de méditation |
| `IFSU-RETRAITE2.webp` | retraite.html | Salle ronde |

**Non encore placés :** `pranayama.jpg`, `IMG_1162.jpg` — à intégrer sur indication.

---

## Mettre à jour une image

Les images étant en base64 dans le HTML, pour remplacer une photo :

1. Encoder la nouvelle image : `base64 -w 0 nouvelle-photo.jpg`
2. Préfixer avec `data:image/jpeg;base64,` (adapter le type MIME)
3. Remplacer la valeur `src="data:image/..."` correspondante dans le HTML

---

## Typo & palette

| Rôle | Valeur |
|------|--------|
| Titres / citations | Cormorant Garamond (Google Fonts) |
| Corps / labels | DM Sans (Google Fonts) |
| `--ardoise` | `#4A6274` |
| `--ardoise-dark` | `#2C3F52` |
| `--lin` | `#F7F3EE` |
| `--terracotta` | `#C4714A` |
| `--gold` | `#C9A84C` |
| `--anthracite` | `#2C2C2C` |
| `--gris-bleuté` | `#7A9AB0` |

---

## Modifier le contenu

Chaque page est autonome. Le CSS partagé est dans `style.css`.  
La navigation et le footer sont répétés dans chaque fichier HTML — modifier les deux si besoin.

**Règle de déploiement :** ne jamais modifier `style.css` sans tester les 5 pages.

---

## Contact

ifsu@etik.com · 0477 09 18 03  
[facebook.com/IFSU.Yoga.Meditation.Ath](https://facebook.com/IFSU.Yoga.Meditation.Ath)  
[mastodon.social/@IFSUYogameditation](https://mastodon.social/@IFSUYogameditation)
