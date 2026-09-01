<div align="center">

<img width="200" height="200" alt="icon" src="https://github.com/user-attachments/assets/e2707416-3ea2-47e2-9a3d-a18011f054c0" />

# VPX VR Injector

**Inject VR Rooms into any Visual Pinball X table — no VR source required.**

[![Version](https://img.shields.io/badge/version-2.2-blueviolet?style=flat-square)](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=flat-square&logo=python)](https://www.python.org/)
[![Platform](https://img.shields.io/badge/platform-Windows-lightgrey?style=flat-square&logo=windows)](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)

</div>

<div align="center">📘 [Documentation / Wiki](https://github.com/Nesta78/VPX-VR-INJECTOR/wiki)</div>

---

## 🇬🇧 English

### What is VPX VR Injector?

**VPX VR Injector** adds a complete VR setup to existing Visual Pinball X (`.vpx`) tables, even when no dedicated VR version exists.

The cabinet and the VR environment are selected independently:

- **Cabinet Pack** — cabinet geometry, backbox/DMD setup and cabinet-specific artwork slots.
- **Room Style** — the environment around the cabinet.

Load a source table, choose the cabinet and Room Style, adjust dimensions and DMD placement if needed, customize artwork and button color, preview the result, clean conflicting source objects, then inject everything into a separate VR-ready `.vpx` file.

VPX VR Injector directly edits VPX OLE Compound File data and injects the required 3D objects, textures, materials and VBScript while preserving the source table.

### ✨ Main features

- 🎮 **One-click VR injection** into existing `.vpx` tables
- 📦 **Multiple Cabinet Packs** for different cabinet eras and styles
- 🏠 **Independent Room Style selection**: Standard or Deluxe
- ⚡ **Automatic cabinet dimensions** based on the source playfield
- 🎛️ **Generic Width / Length / X / Y / Z adjustments**
- 🔢 **DMD Custom X / Y / Depth / Width / Height fine adjustments**
- 💾 **Reusable Generic presets**, including DMD Custom values, with import/export
- 🎨 **Custom cabinet button color** with live 3D Preview
- 🕹️ **Animated cabinet flipper buttons**: the center moves while the ring stays fixed
- 🕹️ **Progressive VR plunger animation**
- 🖼️ **Source-table image extraction** with suggestions and previews
- 🧩 **Built-in multi-layer texture editor**
- ✂️ **Inline Crop tool** that preserves visible size and position
- ⇋ **Duplicate to opposite side** for symmetric artwork
- 📋 **Paste image from clipboard**
- 🎭 **Automatic `*_Empty` mask workflow**
- 🧱 **Built-in Texture Library** for Standard Room walls, floor and roof
- 🖼️ **Built-in poster library** for Deluxe Poster 1 / Poster 2
- ✨ **AI Artwork Assistant / Studio** for Gemini and ChatGPT web workflows
- 🧊 **Integrated 3D Preview** using real VPX meshes, UV mapping and current custom settings
- 🧹 **VR Cleanup** to hide selected source-table objects only in the generated VR table
- ⚠️ **Combined source-table warning** for existing VR objects and possible Rail/Rails conflicts, with direct access to VR Cleanup
- 🔢 **DigitGrid / Flasher DMD detection and repositioning**
- 🌐 **Optional Mixed Reality 360° sphere**
- 🎚️ **F12 VR Room / Mixed Reality switch**
- 💾 **Save As** for the generated VR table
- ▶️ **Optional automatic launch after a successful injection**
- 🔄 **Portable automatic updater**
- 🌗 **Dark / Light themes**
- 🌐 **English / French interface**
- 🎓 **Quick Tour and Complete Tutorial**
- ⚙️ **Standalone Windows executable**

### 🏠 Room Styles

#### Standard Room

The Standard Room provides the classic VR environment with customizable:

- Left Wall
- Right Wall
- Floor
- Roof
- cabinet artwork
- backbox / backglass artwork
- other pack-specific artwork slots

Compatible Room slots include a built-in texture library.

#### Deluxe Room

The Deluxe Room uses a detailed apartment environment with complex UV-mapped assets.

To protect those UV maps, **Apartment Walls**, **Furniture 1** and **Furniture 2** are injected automatically and are not editable.

You can still customize:

- all compatible cabinet artwork
- **Poster 1**
- **Poster 2**

Poster slots include their own built-in poster library.

### 🎨 Cabinet button customization

The **BUTTONS CUSTOM** section lets you choose one color for the complete left and right flipper buttons, including the fixed rings and moving centers.

The selected color is visible in the 3D Preview. In the generated table, only the center of each flipper button moves when its flipper key is pressed; the outer ring remains attached to the cabinet.

VPX VR Injector uses its own dedicated button material, so changing the button color does not alter unrelated materials from the source table.

### 🔢 DMD Custom

The DMD follows the final backbox transformation automatically. Most tables need no manual correction.

For unusual layouts, **DMD Custom** provides:

- X
- Y
- Depth
- Width
- Height

Keep all values at `0` when the automatic placement is correct. DMD Custom values are stored with Generic dimension presets.

### 🧹 VR Cleanup and automatic source-table detection

When a source table is loaded, VPX VR Injector can detect:

- objects that appear to belong to an existing VR setup
- potentially conflicting objects whose names contain **Rail** or **Rails**

If one or both categories are detected, a single warning summarizes the result and offers to open **VR Cleanup**.

VR Cleanup lists source GameItems and lets you mark supported objects as **Hide in VR**. The source file is not modified; the visibility change is applied only to the generated VR table.

### ✨ AI Artwork Assistant / Studio

VPX VR Injector supports web-based workflows with:

- **Gemini**
- **ChatGPT**

No paid API integration is required. The application prepares prompts and image bundles, then opens the selected AI website for manual upload/paste.

It supports source-table references, external references, multi-slot workflows, `*_Empty` masks, direct result import and Generic Artwork formats (16:9, 9:16 and 1:1).

### 🚀 Quick start

1. Download and extract the latest release.
2. Run `VpxVRInjector.exe`.
3. Choose a **Cabinet Pack**.
4. Choose a **Room Style**.
5. Load a `.vpx` source table.
6. Keep **Auto dimensions** enabled for the first test.
7. Adjust Generic / DMD Custom values only if needed.
8. Choose the cabinet **button color** if desired.
9. Customize artwork.
10. Check the result in the **3D Preview**.
11. Use **VR Cleanup** if the source-table warning suggests it or if geometry conflicts are visible.
12. Optionally enable the **Mixed Reality sphere**.
13. Click **Inject VR** and choose the destination.
14. Optionally let VPX VR Injector launch the generated table automatically.

Suggested output filename:

```text
TableName_VR.vpx
```

> **Original backup is disabled by default.** Enable it manually if you want an additional safety copy.

> For **EM tables** or tables whose display is integrated into the backglass, keep a `.directb2s` next to the generated VR table and rename it so the base filename exactly matches the generated `_VR.vpx` file.

> **Requirements:** Windows 10 / 11.

### 📦 Included Cabinet Packs

The list is loaded dynamically from `packs/`. Current packs include:

- Bally
- Data East
- Old School
- Sega Large Screen
- Showcase
- Stern
- Stern Spike
- WPC95 Bally
- WPC95 Williams
- WPC Williams

---

## 🇫🇷 Français

### Qu'est-ce que VPX VR Injector ?

**VPX VR Injector** ajoute un environnement VR complet aux tables Visual Pinball X (`.vpx`) existantes, même lorsqu'aucune version VR dédiée n'existe.

Le cabinet et l'environnement VR sont choisis indépendamment :

- **Cabinet Pack** — géométrie du pincab, configuration backbox/DMD et slots d'artwork propres au cabinet.
- **Room Style** — environnement autour du cabinet.

Chargez une table source, choisissez le cabinet et la Room Style, ajustez si nécessaire les dimensions et le DMD, personnalisez les artworks et la couleur des boutons, vérifiez le résultat dans l'Aperçu 3D, nettoyez les objets source gênants puis injectez l'ensemble dans un nouveau fichier `.vpx` VR.

VPX VR Injector modifie directement les données OLE Compound File de VPX et injecte les objets 3D, textures, matériaux et VBScript nécessaires tout en préservant la table source.

### ✨ Fonctionnalités principales

- 🎮 **Injection VR en un clic**
- 📦 **Plusieurs Cabinet Packs**
- 🏠 **Room Style indépendante** : Standard ou Deluxe
- ⚡ **Dimensions automatiques** selon le playfield source
- 🎛️ **Réglages Generic Width / Length / X / Y / Z**
- 🔢 **Réglages DMD Custom X / Y / Depth / Width / Height**
- 💾 **Presets Generic** incluant les valeurs DMD Custom, avec import/export
- 🎨 **Couleur personnalisable des boutons du pincab**, visible dans l'Aperçu 3D
- 🕹️ **Boutons de flipper animés** : seul le poussoir central s'enfonce, la bague reste fixe
- 🕹️ **Animation progressive du plunger VR**
- 🖼️ **Extraction des images de la table source**
- 🧩 **Éditeur de textures multi-calques**
- ✂️ **Rognage directement dans l'éditeur**
- ⇋ **Dupliquer à l'opposé**
- 📋 **Coller une image depuis le presse-papiers**
- 🎭 **Gestion automatique des masques `*_Empty`**
- 🧱 **Bibliothèque de textures intégrée** pour murs, sol et plafond de la Room Standard
- 🖼️ **Bibliothèque de posters intégrée** pour Poster 1 / Poster 2 en Deluxe
- ✨ **AI Artwork Assistant / Studio** pour Gemini et ChatGPT
- 🧊 **Aperçu 3D intégré** utilisant les vrais meshes/UV VPX et les réglages courants
- 🧹 **VR Cleanup**
- ⚠️ **Alerte combinée** si des objets VR existants et/ou des objets Rail/Rails sont détectés, avec ouverture directe de VR Cleanup
- 🔢 **Détection et repositionnement des DMD DigitGrid / Flashers**
- 🌐 **Sphère 360° Mixed Reality optionnelle**
- 🎚️ **Bascule VR Room / Mixed Reality via F12**
- 💾 **Enregistrer sous**
- ▶️ **Lancement automatique optionnel après injection réussie**
- 🔄 **Mise à jour automatique portable**
- 🌗 **Thèmes sombre / clair**
- 🌐 **Interface Français / Anglais**
- 🎓 **Tour rapide et Tutoriel complet**
- ⚙️ **Exécutable Windows autonome**

### 🏠 Room Styles

#### Room Standard

La Room Standard propose l'environnement classique avec :

- Mur gauche
- Mur droit
- Sol
- Plafond
- artworks du cabinet
- backbox / backglass
- autres slots propres au Cabinet Pack

Les slots de Room compatibles disposent d'une bibliothèque de textures intégrée.

#### Room Deluxe

La Room Deluxe utilise un appartement détaillé basé sur des objets 3D aux UV complexes.

Pour ne pas casser ces UV, **Apartment Walls**, **Furniture 1** et **Furniture 2** sont injectés automatiquement et ne sont pas modifiables.

Vous pouvez toujours personnaliser :

- tous les artworks cabinet compatibles
- **Poster 1**
- **Poster 2**

Les posters disposent de leur propre bibliothèque intégrée.

### 🎨 Personnalisation des boutons du pincab

La section **BUTTONS CUSTOM** permet de choisir une seule couleur appliquée aux deux boutons complets : bague fixe + poussoir central.

La couleur choisie apparaît dans l'Aperçu 3D. Dans la table générée, seule la partie centrale du bouton s'enfonce avec la touche de flipper correspondante ; la bague reste fixée au cabinet.

VPX VR Injector utilise un matériau dédié aux boutons, sans modifier les matériaux sans rapport de la table source.

### 🔢 DMD Custom

Le DMD suit automatiquement la transformation finale du backbox. Dans la majorité des cas, aucun réglage manuel n'est nécessaire.

Pour les tables atypiques, **DMD Custom** permet d'ajuster :

- X
- Y
- Depth
- Width
- Height

Laissez toutes les valeurs à `0` si le placement automatique est correct. Les valeurs DMD Custom sont enregistrées dans les presets Generic.

### 🧹 VR Cleanup et détection automatique

Au chargement d'une table source, VPX VR Injector peut détecter :

- des objets semblant appartenir à une ancienne configuration VR
- des objets potentiellement gênants dont le nom contient **Rail** ou **Rails**

Si une ou deux catégories sont trouvées, une seule alerte récapitule la détection et propose d'ouvrir **VR Cleanup**.

VR Cleanup liste les GameItems et permet de sélectionner les objets à **Masquer en VR**. La table source n'est pas modifiée : le masquage est appliqué uniquement à la nouvelle table VR.

### ✨ AI Artwork Assistant / Studio

VPX VR Injector prend en charge les workflows Web :

- **Gemini**
- **ChatGPT**

Aucune API payante n'est nécessaire. L'application prépare le prompt et les images, puis ouvre le site choisi pour le collage et le dépôt manuels.

Les références source/externes, les workflows multi-slots, les masques `*_Empty`, l'import du résultat et les formats Artwork générique 16:9 / 9:16 / 1:1 sont pris en charge.

### 🚀 Démarrage rapide

1. Téléchargez et extrayez la dernière release.
2. Lancez `VpxVRInjector.exe`.
3. Choisissez un **Cabinet Pack**.
4. Choisissez une **Room Style**.
5. Chargez la table `.vpx` source.
6. Gardez **Dimensions auto** activé pour le premier essai.
7. Ajustez les valeurs Generic / DMD Custom uniquement si nécessaire.
8. Choisissez éventuellement la **couleur des boutons**.
9. Personnalisez les artworks.
10. Vérifiez le résultat dans l'**Aperçu 3D**.
11. Utilisez **VR Cleanup** si l'alerte le suggère ou si des objets se superposent.
12. Activez éventuellement la **sphère Mixed Reality**.
13. Cliquez sur **Injecter VR** et choisissez la destination.
14. Activez éventuellement le lancement automatique de la table générée.

Nom suggéré :

```text
NomDeLaTable_VR.vpx
```

> **Sauvegarde originale est désactivée par défaut.** Activez-la manuellement si vous souhaitez une copie de sécurité supplémentaire.

> Pour les **tables EM** ou les tables dont l'affichage est intégré au backglass, conservez un `.directb2s` à côté de la table VR générée et renommez-le pour que son nom de base corresponde exactement au fichier `_VR.vpx`.

> **Configuration requise :** Windows 10 / 11.

### 📦 Cabinet Packs inclus

La liste est chargée dynamiquement depuis `packs/`. Elle comprend actuellement :

- Bally
- Data East
- Old School
- Sega Large Screen
- Showcase
- Stern
- Stern Spike
- WPC95 Bally
- WPC95 Williams
- WPC Williams

---

<div align="center">

Made with ❤️ for the VPX VR Pinball community — thank you to **Sixtoe & Dardog** for the VR Room resources, and special thanks to **Speedygonzales** for extensive testing and feedback.

[⬆ Back to top](#vpx-vr-injector)

</div>
