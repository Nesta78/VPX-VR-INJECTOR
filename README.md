<div align="center">

<img width="200" height="200" alt="icon" src="https://github.com/user-attachments/assets/e2707416-3ea2-47e2-9a3d-a18011f054c0" />

# VPX VR Injector

**Inject VR Rooms into any Visual Pinball X table — no VR source required.**

[![Version](https://img.shields.io/badge/version-2.0-blueviolet?style=flat-square)](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=flat-square&logo=python)](https://www.python.org/)
[![Platform](https://img.shields.io/badge/platform-Windows-lightgrey?style=flat-square&logo=windows)](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)

</div>

<div align="center">📘 [Documentation / Wiki](https://github.com/Nesta78/VPX-VR-INJECTOR/wiki)</div>

---

## 🇬🇧 English

### What is VPX VR Injector?

**VPX VR Injector** adds a complete VR setup to existing Visual Pinball X (`.vpx`) tables, even when no VR version of the table exists.

Starting with **v2.0**, the cabinet and the VR environment are handled separately:

- **Cabinet Pack** — choose the cabinet type that best matches the table.
- **Room Style** — choose the environment around the cabinet.

This lets the same cabinet pack work with different VR environments without duplicating complete packs.

Load a table, choose a Cabinet Pack and Room Style, customize compatible artwork, preview the result, then inject everything into a new `.vpx` file.

The application directly edits VPX OLE Compound File data and injects the required 3D objects, textures, materials and VBScript while preserving the original source table.

### ✨ Main features

- 🎮 **One-click VR injection** into existing `.vpx` tables
- 📦 **Multiple Cabinet Packs** for different cabinet eras and styles
- 🏠 **Independent Room Style selection**
- 🧱 **Standard Room** with customizable floor, roof and wall artwork
- 🛋️ **Deluxe Room** with detailed apartment geometry and furniture
- 🖼️ **Editable Deluxe posters** while complex apartment UV maps stay protected
- ⚡ **Automatic dimensions** based on the source table playfield
- 🎛️ **Generic Width / Length / X / Y / Z adjustments**
- 💾 **Reusable Generic presets** with import/export
- 🖼️ **Source-table image extraction** with suggestions and previews
- 🧩 **Built-in multi-layer texture editor**
- ✂️ **Inline Crop tool** that preserves the cropped layer's visible size and position
- ⇋ **Duplicate to opposite side** for symmetric cabinet artwork
- 📋 **Paste image from clipboard**
- 🎭 **Automatic `*_Empty` mask workflow**
- 🧱 **Built-in Texture Library** for Standard Room floor, roof and wall textures
- 🧊 **Integrated 3D Preview** using the real VPX meshes, UV mapping and selected Room Style
- 🧹 **VR Cleanup** to hide problematic source-table objects only in the generated VR table
- ⚠️ **Existing VR-object detection** when the loaded source table already appears to contain a VR Room
- 🔢 **DigitGrid / Flasher DMD detection and repositioning**
- 🕹️ **Progressive VR plunger animation**
- 🌐 **Optional Mixed Reality 360° sphere**
- 🎚️ **F12 VR Room / Mixed Reality switch**, compatible with Standard and Deluxe Rooms
- 🧱 **Reliable material injection**
- 💾 **Save As** for the generated VR table
- 🔄 **Automatic portable updater**
- 🌗 **Dark / Light interface themes**
- 🌐 **English / French interface**
- 🎓 **Quick Tour and Detailed Tutorial**
- ⚙️ **Standalone Windows executable**

### 🏠 Room Styles — v2.0

#### Standard Room

The Standard Room keeps the classic VPX VR Injector workflow.

Depending on the selected Cabinet Pack, you can customize:

- Left Wall
- Right Wall
- Floor
- Roof
- cabinet artwork
- backbox / backglass artwork
- other pack-specific artwork slots

The Standard Room also supports the **Built-in Texture Library** introduced in v1.9.

#### Deluxe Room

The Deluxe Room uses detailed apartment geometry made from complex UV-mapped 3D assets.

To avoid breaking those UV maps:

- **Apartment Walls**
- **Furniture 1**
- **Furniture 2**

are injected automatically and are intentionally **not editable**.

You can still customize:

- all compatible **cabinet artwork**
- **Poster 1**
- **Poster 2**

The 3D Preview, injection logic and Mixed Reality sphere automatically follow the selected Room Style.

---

### 🧱 Built-in Texture Library — v1.9

For compatible Standard Room slots, the texture editor includes a **Built-in Texture Library**.

Available categories include:

- Floor
- Roof
- Left Wall
- Right Wall

A built-in texture can be selected, previewed and used as the current slot artwork, then edited normally in the texture editor.

Wall textures are displayed in their natural visual orientation in:

- the library
- the editor
- the main slot preview
- the 3D Preview
- the final injected VR Room

VPX VR Injector handles the technical VPX orientation internally.

---

### ✨ AI Artwork Assistant / Studio

VPX VR Injector supports two web-based AI providers:

- **Gemini**
- **ChatGPT**

No paid API integration is required. VPX VR Injector prepares the prompt and image bundle, then opens the selected AI website so the user can paste the prompt and drag/drop the prepared images manually.

Features include:

- selectable **Gemini / ChatGPT provider**
- provider-specific prompts
- external reference images from your computer
- source-table images as references
- multi-slot artwork generation workflow
- automatic slot selection when launched from the texture editor
- downloaded HD result import directly into the matching slot
- automatic `*_Empty` mask placement after import
- **Generic Artwork** mode
- Generic Artwork formats:
  - Landscape **16:9**
  - Portrait **9:16**
  - Square **1:1**
- separate prompt files:
  - `gemini_prompt.txt`
  - `chatgpt_prompt.txt`

Available AI targets automatically follow the selected Room Style. In Deluxe mode, protected Apartment UV textures are not exposed as editable AI targets.

> AI generation remains a manual web workflow. VPX VR Injector does not bypass the provider's interface, limits or account requirements.

---

### 🚀 Quick start

1. Download the latest release from the [Releases page](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)
2. Extract `VpxVRInjector.zip`
3. Run `VpxVRInjector.exe`
4. Select a **Cabinet Pack**
5. Select a **Room Style**
6. Load a `.vpx` source table
7. Keep **Auto dimensions** enabled in most cases
8. Optionally adjust Generic values or load a preset
9. Customize compatible artwork
10. Optionally use **🧹 VR Cleanup**
11. Inspect the result with the **3D Preview**
12. Optionally enable the **Mixed Reality sphere**
13. Click **Inject VR**
14. Choose the destination filename and folder

The suggested output filename is usually:

```text
TableName_VR.vpx
```

> If the source table already appears to contain VR objects, VPX VR Injector displays a warning because injecting another VR setup may create duplicated or overlapping geometry.

> **Original backup is disabled by default.** Enable it manually if you want an additional safety copy.

> For **EM tables** or tables using an integrated backglass display, keep a `.directb2s` file next to the generated VR table and rename it so its base filename exactly matches the generated `_VR.vpx` file.

> **Requirements:** Windows 10/11

---

### 📦 Included Cabinet Packs

The Cabinet Pack list is loaded dynamically from the `packs/` folder. Current packs include, among others:

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

**VPX VR Injector** ajoute un environnement VR complet aux tables Visual Pinball X (`.vpx`) existantes, même lorsqu'aucune version VR de la table n'existe.

À partir de la **v2.0**, le cabinet et l'environnement VR sont gérés séparément :

- **Cabinet Pack** — choisissez le type de cabinet correspondant à la table.
- **Room Style** — choisissez l'environnement autour du cabinet.

Cela permet d'utiliser le même Cabinet Pack avec plusieurs environnements VR sans dupliquer des packs complets.

Chargez une table, choisissez un Cabinet Pack et une Room Style, personnalisez les artworks compatibles, prévisualisez le résultat puis injectez l'ensemble dans un nouveau fichier `.vpx`.

L'application modifie directement les données OLE Compound File de VPX et injecte les objets 3D, textures, matériaux et code VBScript nécessaires tout en conservant la table source originale.

### ✨ Fonctionnalités principales

- 🎮 **Injection VR en un clic**
- 📦 **Plusieurs Cabinet Packs** pour différentes générations de cabinets
- 🏠 **Choix indépendant de la Room Style**
- 🧱 **Room Standard** avec sol, plafond et murs personnalisables
- 🛋️ **Room Deluxe** avec appartement détaillé et mobilier
- 🖼️ **Posters Deluxe personnalisables**, tout en protégeant les UV complexes de l'appartement
- ⚡ **Dimensions automatiques** selon le playfield source
- 🎛️ **Réglages Generic Width / Length / X / Y / Z**
- 💾 **Presets Generic** réutilisables avec import/export
- 🖼️ **Extraction des images de la table source** avec suggestions et aperçus
- 🧩 **Éditeur de textures multi-calques**
- ✂️ **Rognage directement dans l'éditeur**
- ⇋ **Dupliquer à l'opposé**
- 📋 **Coller une image depuis le presse-papiers**
- 🎭 **Gestion automatique des masques `*_Empty`**
- 🧱 **Bibliothèque de textures intégrée** pour le sol, plafond et murs de la Room Standard
- 🧊 **Aperçu 3D intégré** utilisant les vrais meshes, UV et la Room Style sélectionnée
- 🧹 **VR Cleanup**
- ⚠️ **Détection d'objets VR existants** dans la table source
- 🔢 **Détection et repositionnement des DMD DigitGrid / Flashers**
- 🕹️ **Animation progressive du plunger VR**
- 🌐 **Sphère 360° Mixed Reality optionnelle**
- 🎚️ **Bascule VR Room / Mixed Reality via F12**, compatible Standard et Deluxe
- 🧱 **Injection fiable des matériaux**
- 💾 **Enregistrer sous**
- 🔄 **Mise à jour automatique portable**
- 🌗 **Thèmes sombre / clair**
- 🌐 **Interface Français / Anglais**
- 🎓 **Tour rapide et Tutoriel complet**
- ⚙️ **Exécutable Windows autonome**

### 🏠 Room Styles — v2.0

#### Room Standard

La Room Standard conserve le fonctionnement classique de VPX VR Injector.

Selon le Cabinet Pack sélectionné, vous pouvez notamment personnaliser :

- Mur gauche
- Mur droit
- Sol
- Plafond
- artwork du cabinet
- backbox / backglass
- autres slots spécifiques au pack

La Room Standard donne également accès à la **Bibliothèque de textures intégrée** introduite en v1.9.

#### Room Deluxe

La Room Deluxe utilise une géométrie d'appartement détaillée basée sur des objets 3D aux UV complexes.

Afin de ne pas casser ces UV :

- **Apartment Walls**
- **Furniture 1**
- **Furniture 2**

sont injectés automatiquement et volontairement **non modifiables**.

Vous pouvez toujours personnaliser :

- tous les **artworks du cabinet** compatibles
- **Poster 1**
- **Poster 2**

L'Aperçu 3D, l'injection et la sphère Mixed Reality s'adaptent automatiquement à la Room Style sélectionnée.

---

### 🧱 Bibliothèque de textures intégrée — v1.9

Pour les slots compatibles de la Room Standard, l'éditeur propose une **Bibliothèque de textures intégrée**.

Catégories disponibles :

- Sol
- Plafond
- Mur gauche
- Mur droit

Une texture intégrée peut être sélectionnée, prévisualisée, appliquée au slot puis modifiée normalement dans l'éditeur.

Les textures de murs sont affichées dans leur orientation visuelle naturelle dans :

- la bibliothèque
- l'éditeur
- la vignette du slot
- l'Aperçu 3D
- la VR Room injectée

VPX VR Injector gère automatiquement l'orientation technique nécessaire à VPX.

---

### ✨ AI Artwork Assistant / Studio

VPX VR Injector prend en charge deux services IA Web :

- **Gemini**
- **ChatGPT**

Aucune API payante n'est nécessaire. VPX VR Injector prépare le prompt et les images puis ouvre le site du provider choisi.

Fonctionnalités :

- choix **Gemini / ChatGPT**
- prompts adaptés au provider
- images de référence externes
- images extraites de la table source
- génération guidée de plusieurs slots
- présélection du slot depuis l'éditeur
- import direct du résultat HD
- placement automatique du masque `*_Empty`
- mode **Artwork générique**
- formats :
  - Paysage **16:9**
  - Portrait **9:16**
  - Carré **1:1**
- fichiers :
  - `gemini_prompt.txt`
  - `chatgpt_prompt.txt`

Les cibles IA disponibles suivent automatiquement la Room Style choisie. En mode Deluxe, les UV protégés de l'appartement ne sont pas proposés comme cibles modifiables.

> La génération IA reste un workflow Web manuel. VPX VR Injector ne contourne ni l'interface, ni les limites, ni les conditions de compte des fournisseurs.

---

### 🚀 Démarrage rapide

1. Téléchargez la dernière version depuis la [page Releases](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)
2. Extrayez `VpxVRInjector.zip`
3. Lancez `VpxVRInjector.exe`
4. Choisissez un **Cabinet Pack**
5. Choisissez une **Room Style**
6. Chargez une table `.vpx`
7. Laissez **Dimensions auto** activé dans la majorité des cas
8. Ajustez éventuellement les valeurs Generic ou chargez un preset
9. Personnalisez les artworks compatibles
10. Utilisez éventuellement **🧹 VR Cleanup**
11. Vérifiez le résultat avec l'**Aperçu 3D**
12. Activez éventuellement la **sphère Mixed Reality**
13. Cliquez sur **Injecter VR**
14. Choisissez le nom et le dossier de destination

Le nom proposé utilise généralement :

```text
NomDeLaTable_VR.vpx
```

> Si la table source semble déjà contenir des objets VR, VPX VR Injector affiche une alerte car une nouvelle injection peut créer des doublons ou superpositions.

> **Sauvegarde originale est désactivée par défaut.** Activez-la manuellement si vous souhaitez une copie de sécurité supplémentaire.

> Pour les **tables EM** ou les tables utilisant un affichage intégré au backglass, conservez un fichier `.directb2s` à côté de la table VR générée et renommez-le afin que son nom de base corresponde exactement au fichier `_VR.vpx`.

> **Configuration requise :** Windows 10/11

---

### 📦 Cabinet Packs inclus

La liste est chargée dynamiquement depuis le dossier `packs/`. La version actuelle comprend notamment :

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
