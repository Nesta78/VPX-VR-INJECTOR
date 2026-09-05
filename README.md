<div align="center">
  <img width="180" height="180" alt="VPX VR Injector" src="https://github.com/user-attachments/assets/e2707416-3ea2-47e2-9a3d-a18011f054c0" />

# VPX VR Injector

**Turn existing Visual Pinball X tables into VR-ready tables — with a modern guided interface, cabinet packs, Room environments, artwork tools, VPS integration and Hybrid support.**

[![Version](https://img.shields.io/badge/version-2.9-blueviolet?style=flat-square)](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)
[![Platform](https://img.shields.io/badge/platform-Windows-lightgrey?style=flat-square&logo=windows)](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)
[![Language](https://img.shields.io/badge/UI-English%20%2F%20Français-6c5ce7?style=flat-square)](https://github.com/Nesta78/VPX-VR-INJECTOR)
[![Standalone](https://img.shields.io/badge/build-standalone-success?style=flat-square)](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)

📘 **[Documentation / Wiki](https://github.com/Nesta78/VPX-VR-INJECTOR/wiki)**

</div>

---

# 🇬🇧 English

## What is VPX VR Injector?

**VPX VR Injector** adds a complete VR setup to an existing Visual Pinball X (`.vpx`) table, even when no dedicated VR version exists.

The source table is preserved. VPX VR Injector creates a separate generated `.vpx` file containing the selected cabinet, Room environment, artwork, DMD adjustments, optional Mixed Reality, cleanup rules and supporting script logic.

It also includes an **experimental Hybrid mode** that keeps the original 2D/Desktop behavior while enabling the injected VR layer only when VPX is running in VR.

## Highlights

- **Multiple Cabinet Packs**: Bally, Data East, Old School, Sega Large Screen, Showcase, Stern, Stern Spike, WPC95 Bally, WPC95 Williams and WPC Williams
- **Room Styles**: Standard, Deluxe and Ultra Minimal
- **Experimental Hybrid mode** for combined 2D/Desktop + VR tables
- **VPS integration**
  - detects existing VR releases
  - shows release information and links
  - recommends the closest Cabinet Pack
  - lets you apply the recommendation directly from the Cabinet page
- **Automatic cabinet dimensions** based on the source playfield
- **Generic Width / Length / X / Y / Z adjustments**
- **DMD Custom** X / Y / Depth / Width / Height corrections
- **Reusable dimension presets**
- **Cabinet button color customization**
- **Animated flipper buttons**
- **Progressive VR plunger**
- **Artwork slots** with per-pack / per-Room compatibility
- **Built-in Standard Room texture library**
- **Built-in Deluxe poster library**
- **Source-table image extraction**
- **Multi-layer image editor**
  - move, resize, rotate and mirror
  - layer visibility and ordering
  - inline crop
  - clipboard paste
  - `*_Empty` masks
  - Duplicate to opposite side
- **AI Artwork Assistant / Studio**
  - Gemini
  - ChatGPT
  - no paid API required
  - source/external references
  - multi-slot workflow
- **Integrated 3D Preview** using the current cabinet, Room, artwork and button color
- **VR Cleanup** with cautious suggestions for rails, lockbars and likely side rails
- **Mixed Reality 360° sphere**
- **DigitGrid / Flasher DMD support**
- **Portable automatic updater**
- **Automatic launch after successful injection**
- **English / French UI**
- **Light / Dark themes**
- **Global text-size control**
- **Quick Tour + Complete Tutorial**
- **Window size and position remembered between launches**

## Quick start

1. Download and extract the latest release.
2. Run `VpxVRInjector.exe`.
3. Load a source `.vpx` table from the **Table** page.
4. Review VPS information if a match is found.
5. Choose or accept the recommended **Cabinet Pack**.
6. Select a **Room Style** or configure **Hybrid** mode.
7. Keep **Automatic dimensions** enabled for the first test.
8. Adjust Generic and DMD values only if needed.
9. Customize artwork.
10. Inspect the result in **Preview 3D**.
11. Use **VR Cleanup** only for source objects that really conflict with the injected VR setup.
12. Optionally enable the **Mixed Reality Sphere**.
13. Click **Inject VR** and save the generated table.

Suggested output name:

```text
TableName_VR.vpx
```

> The source table is not replaced.

## Room Styles

### Standard
Classic VR Room with customizable:
- Left Wall
- Right Wall
- Floor
- Roof

### Deluxe
Detailed apartment-style Room. Complex UV textures are protected automatically, while compatible cabinet artwork and **Poster 1 / Poster 2** remain customizable.

### Ultra Minimal
Cabinet-only configuration:
- cabinet
- backbox / backglass / DMD
- cabinet artwork
- buttons
- plunger

No surrounding Room geometry is injected.

## Experimental Hybrid mode

Hybrid creates one generated `.vpx` intended to work in both:
- **2D/Desktop/Cabinet**
- **VR**

Outside VR, the source table keeps its original presentation. In VR, the injected cabinet and selected environments become active.

A Hybrid table can include:
- Standard
- Deluxe
- Ultra Minimal
- Mixed Reality

Use **F12** to cycle through injected VR environments where supported.

> Hybrid mode is experimental. Keep the original source table and test both 2D/Desktop and VR behavior.

## VPS integration

When a table is loaded, VPX VR Injector can query the public **Virtual Pinball Spreadsheet (VPS)** database.

It can:
- detect dedicated VR releases that already exist
- display release version, authors, features and thumbnail
- open each release page individually
- recommend the closest available Cabinet Pack from matched manufacturer/year metadata

Recommendations are **never forced**. You decide whether to use them.

## Artwork workflow

Artwork can come from:
- default Cabinet Pack / Room assets
- embedded images from the source table
- built-in texture/poster libraries
- external images
- clipboard
- AI-generated artwork

The editor supports multiple layers, mirroring, crop, rotation, reordering and `*_Empty` masks for protected cabinet areas.

## AI Artwork Assistant / Studio

The Studio supports:
- **Gemini**
- **ChatGPT**

VPX VR Injector prepares prompts and reference images, then opens the selected web service. No paid API is required.

For multi-slot creation, keep the same AI conversation so visual identity stays consistent.

## VR Cleanup

VR Cleanup lists source-table GameItems and helps you identify objects that may conflict with the injected cabinet.

Suggestions can include:
- `Rail` / `Rails`
- `SideRail`
- `Lockbar` / `Lock Bar`
- `Lockdownbar` / `Lockdown Bar`
- cautious geometry-based side-rail candidates

Nothing is hidden automatically.

## EM / DirectB2S note

For EM tables or layouts where the score/display is integrated into the backglass, keep a matching `.directb2s` file next to the generated table.

Example:

```text
MyTable_VR.vpx
MyTable_VR.directb2s
```

Both files must share the same base filename.

## Requirements

- Windows 10 / 11
- Visual Pinball X installation for using the generated tables
- No Python installation required for the standalone release

---

# 🇫🇷 Français

## Qu'est-ce que VPX VR Injector ?

**VPX VR Injector** ajoute une configuration VR complète à une table Visual Pinball X (`.vpx`) existante, même lorsqu'aucune version VR dédiée n'existe.

La table source est conservée. VPX VR Injector crée un nouveau fichier `.vpx` contenant le cabinet, la Room, les artworks, les corrections DMD, l'éventuelle Mixed Reality, les règles VR Cleanup et la logique script nécessaire.

Un **mode Hybride expérimental** permet également de conserver le comportement 2D/Desktop d'origine tout en activant la couche VR injectée lorsque VPX fonctionne en VR.

## Points forts

- **Plusieurs Cabinet Packs**
- **Rooms Standard, Deluxe et Ultra Minimal**
- **Mode Hybride expérimental**
- **Intégration VPS**
  - détection des releases VR existantes
  - informations et liens vers les releases
  - recommandation du Cabinet Pack le plus proche
  - application directe de la recommandation depuis la page Cabinet
- **Dimensions automatiques**
- **Réglages Width / Length / X / Y / Z**
- **DMD Custom** X / Y / Depth / Width / Height
- **Presets de dimensions**
- **Couleur personnalisable des boutons**
- **Boutons de flipper animés**
- **Plunger VR progressif**
- **Gestion complète des artworks**
- **Bibliothèque de textures Standard**
- **Bibliothèque de posters Deluxe**
- **Extraction des images intégrées à la table**
- **Éditeur multi-calques**
  - déplacement et redimensionnement
  - rotation et miroir
  - visibilité et ordre des calques
  - crop inline
  - collage presse-papiers
  - masques `*_Empty`
  - Dupliquer à l'opposé
- **AI Artwork Assistant / Studio**
  - Gemini
  - ChatGPT
  - aucune API payante nécessaire
- **Aperçu 3D intégré**
- **VR Cleanup** avec suggestions prudentes
- **Sphère Mixed Reality 360°**
- **Support DMD DigitGrid / Flashers**
- **Mise à jour automatique**
- **Lancement automatique après injection**
- **Interface Français / Anglais**
- **Thèmes clair / sombre**
- **Taille globale du texte**
- **Tour rapide + Tutoriel complet**
- **Mémorisation de la taille et de la position de la fenêtre**

## Démarrage rapide

1. Téléchargez et extrayez la dernière release.
2. Lancez `VpxVRInjector.exe`.
3. Chargez une table `.vpx` depuis l'onglet **Table**.
4. Consultez les informations VPS si une correspondance est trouvée.
5. Choisissez ou acceptez le **Cabinet Pack recommandé**.
6. Sélectionnez une **Room Style** ou configurez le mode **Hybride**.
7. Gardez **Dimensions automatiques** activé pour le premier test.
8. Ajustez les réglages Generic et DMD uniquement si nécessaire.
9. Personnalisez les artworks.
10. Vérifiez le résultat dans **Aperçu 3D**.
11. Utilisez **VR Cleanup** uniquement pour les objets source qui gênent réellement la VR injectée.
12. Activez éventuellement la **Sphère Mixed Reality**.
13. Cliquez sur **Injecter VR** et enregistrez la table générée.

Nom conseillé :

```text
NomDeLaTable_VR.vpx
```

> La table source n'est pas remplacée.

## Room Styles

### Standard
Room VR classique avec :
- Mur gauche
- Mur droit
- Sol
- Plafond

### Deluxe
Room appartement détaillée. Les textures UV complexes sont protégées automatiquement, tandis que les artworks cabinet compatibles et **Poster 1 / Poster 2** restent personnalisables.

### Ultra Minimal
Configuration cabinet uniquement :
- cabinet
- backbox / backglass / DMD
- artworks cabinet
- boutons
- plunger

Aucune géométrie de Room environnante n'est injectée.

## Mode Hybride expérimental

Le mode Hybride crée un seul `.vpx` destiné à fonctionner en :
- **2D/Desktop/Cabinet**
- **VR**

Hors VR, la table source conserve son apparence normale. En VR, le cabinet et les environnements injectés deviennent actifs.

Une table Hybrid peut inclure :
- Standard
- Deluxe
- Ultra Minimal
- Mixed Reality

Utilisez **F12** pour changer d'environnement VR injecté lorsque la configuration le permet.

> Le mode Hybride est expérimental. Conservez la table source et testez toujours le résultat en 2D/Desktop et en VR.

## Intégration VPS

Au chargement d'une table, VPX VR Injector peut interroger la base publique **Virtual Pinball Spreadsheet (VPS)**.

Le logiciel peut :
- détecter les releases VR dédiées déjà disponibles
- afficher version, auteurs, features et miniature
- ouvrir individuellement chaque release
- recommander le Cabinet Pack le plus proche à partir du fabricant et de l'année détectés

Les recommandations ne sont **jamais imposées**.

## Workflow Artwork

Les images peuvent provenir :
- des assets par défaut du Cabinet Pack / de la Room
- des images intégrées à la table source
- des bibliothèques internes
- de fichiers externes
- du presse-papiers
- d'un artwork généré avec une IA

L'éditeur gère les calques, le miroir, le crop, la rotation, l'ordre des calques et les masques `*_Empty`.

## AI Artwork Assistant / Studio

Le Studio prend en charge :
- **Gemini**
- **ChatGPT**

VPX VR Injector prépare le prompt et les références puis ouvre le service Web choisi. Aucune API payante n'est nécessaire.

Pour plusieurs slots, gardez la même conversation IA afin de conserver une identité visuelle cohérente.

## VR Cleanup

VR Cleanup liste les GameItems de la table source et aide à repérer les éléments pouvant entrer en conflit avec le cabinet injecté.

Les suggestions peuvent inclure :
- `Rail` / `Rails`
- `SideRail`
- `Lockbar` / `Lock Bar`
- `Lockdownbar` / `Lockdown Bar`
- certains rails latéraux probables détectés prudemment

Aucun objet n'est masqué automatiquement.

## Note EM / DirectB2S

Pour les tables EM ou les tables dont l'affichage est intégré au backglass, conservez un `.directb2s` portant le même nom de base que la table générée.

Exemple :

```text
MaTable_VR.vpx
MaTable_VR.directb2s
```

## Configuration requise

- Windows 10 / 11
- Visual Pinball X pour utiliser les tables générées
- aucune installation Python nécessaire avec la release autonome

---

<div align="center">

Made with ❤️ for the VPX VR Pinball community.

VR Room resources: **Sixtoe & Dardog**  
Rawd Poster: **JoePicasso**  
VPS data: **all VPS Database contributors**  
Testing & feedback: **Speedygonzales and the VPX community**

**[Documentation / Wiki](https://github.com/Nesta78/VPX-VR-INJECTOR/wiki)** · **[Releases](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)**

</div>
