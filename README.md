<div align="center">

<img width="200" height="200" alt="icon" src="https://github.com/user-attachments/assets/e2707416-3ea2-47e2-9a3d-a18011f054c0" />

# VPX VR Injector

**Inject VR Rooms into any Visual Pinball X table — no VR source required.**

[![Version](https://img.shields.io/badge/version-1.6-blueviolet?style=flat-square)](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=flat-square&logo=python)](https://www.python.org/)
[![Platform](https://img.shields.io/badge/platform-Windows-lightgrey?style=flat-square&logo=windows)](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)

</div>

<div align="center">📘 [Documentation / Wiki](https://github.com/Nesta78/VPX-VR-INJECTOR/wiki)</div>

---

## 🇬🇧 English

### What is VPX VR Injector?

**VPX VR Injector** adds a complete VR Room to existing Visual Pinball X (`.vpx`) tables, even when no VR version of the table exists.

Choose a VR pack, load a table, optionally customize the cabinet artwork and geometry, preview the result, then inject the Room into a new `.vpx` file.

The application directly edits VPX OLE Compound File data and injects the required 3D objects, textures, materials and VBScript while preserving the original source table.

### ✨ Main features

- 🎮 **One-click VR injection** into existing `.vpx` tables
- 📦 **Multiple VR packs** for different cabinet eras and styles
- ⚡ **Automatic dimensions** based on the source table playfield
- 🎛️ **Generic Width / Length / X / Y / Z adjustments**
- 💾 **Reusable Generic presets** with import/export
- 🖼️ **Source-table image extraction** with suggestions and previews
- 🧩 **Built-in multi-layer texture editor**
- ✂️ **Inline Crop tool** that preserves the cropped layer's visible size and position
- ⇋ **Duplicate to opposite side** for symmetric cabinet artwork
- 📋 **Paste image from clipboard**
- 🎭 **Automatic `*_Empty` mask workflow**
- 🧊 **Integrated 3D VR Room Preview** using the real VPX meshes and UV mapping from the selected pack
- 🧹 **VR Cleanup** to hide problematic source-table objects only in the generated VR table
- ⚠️ **Rail / Rails suggestions** inside VR Cleanup
- 🔢 **DigitGrid / Flasher DMD detection and repositioning**
- 🕹️ **Progressive VR plunger animation**
- 🌐 **Optional Mixed Reality 360° sphere**
- 🎚️ **F12 VR Room / Mixed Reality switch**
- 🧱 **Reliable material injection**
- 💾 **Save As** for the generated VR table
- 🔄 **Automatic portable updater**
- 🌐 **English / French interface**
- ⚙️ **Standalone Windows executable**

### ✨ AI Artwork Studio — v1.6

Version 1.6 expands the artwork workflow into a provider-independent **AI Artwork Assistant / AI Artwork Studio**.

Supported web providers:

- **Gemini**
- **ChatGPT**

No paid API integration is required. VPX VR Injector prepares the prompt and image bundle, then opens the selected AI website so the user can paste the prompt and drag/drop the prepared images manually.

New AI features include:

- clearly selectable **Gemini / ChatGPT provider**
- provider-specific prompts
- external reference images from your computer, in addition to images extracted from the VPX table
- multi-slot artwork generation workflow
- automatic slot selection when launched from the texture editor
- downloaded HD result import directly into the matching slot
- automatic `*_Empty` mask placement after import
- **Generic Artwork** mode for creating reusable free-form artwork
- Generic Artwork formats:
  - Landscape **16:9**
  - Portrait **9:16**
  - Square **1:1**
- separate prompt files:
  - `gemini_prompt.txt`
  - `chatgpt_prompt.txt`

> AI generation remains a manual web workflow. VPX VR Injector does not bypass the provider's interface, limits or account requirements.

---

### 🚀 Quick start

1. Download the latest release from the [Releases page](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)
2. Extract `VpxVRInjector.zip`
3. Run `VpxVRInjector.exe`
4. Select a `.vpx` table
5. Choose a VR Pack
6. Keep **Auto dimensions** enabled in most cases
7. Optionally adjust Generic values or load a preset
8. Customize artwork with source-table images, the texture editor or the AI Artwork Assistant
9. Optionally use **🧹 VR Cleanup**
10. Optionally inspect the Room with the **3D Preview**
11. Click **Inject VR**
12. Choose the destination filename and folder

The suggested output filename is usually:

```text
TableName_VR.vpx
```

> **Original backup is disabled by default.** Enable it manually if you want an additional safety copy.

> For **EM tables** or tables using an integrated backglass display, keep a `.directb2s` file next to the generated VR table and rename it so its base filename exactly matches the generated `_VR.vpx` file.

> **Requirements:** Windows 10/11

---

### 📦 Included VR Packs

The pack list is loaded dynamically from the `packs/` folder. Current packs include, among others:

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

**VPX VR Injector** ajoute une VR Room complète aux tables Visual Pinball X (`.vpx`) existantes, même lorsqu'aucune version VR de la table n'existe.

Choisissez un pack VR, chargez une table, personnalisez éventuellement l'artwork et la géométrie du cabinet, prévisualisez le résultat puis injectez la Room dans un nouveau fichier `.vpx`.

L'application modifie directement les données OLE Compound File de VPX et injecte les objets 3D, textures, matériaux et code VBScript nécessaires tout en conservant la table source originale.

### ✨ Fonctionnalités principales

- 🎮 **Injection VR en un clic**
- 📦 **Plusieurs packs VR** pour différentes générations de cabinets
- ⚡ **Dimensions automatiques** selon le playfield de la table source
- 🎛️ **Réglages Generic Width / Length / X / Y / Z**
- 💾 **Presets Generic** réutilisables avec import/export
- 🖼️ **Extraction des images de la table source** avec suggestions et aperçus
- 🧩 **Éditeur de textures multi-calques**
- ✂️ **Rognage directement dans l'éditeur** en conservant la taille et la position visuelles
- ⇋ **Dupliquer à l'opposé** pour les artworks symétriques
- 📋 **Coller une image depuis le presse-papiers**
- 🎭 **Gestion automatique des masques `*_Empty`**
- 🧊 **Aperçu 3D intégré** utilisant les vrais meshes et UV du pack VPX
- 🧹 **VR Cleanup** pour masquer certains objets uniquement dans la table VR générée
- ⚠️ **Suggestions Rail / Rails**
- 🔢 **Détection et repositionnement des DMD DigitGrid / Flashers**
- 🕹️ **Animation progressive du plunger VR**
- 🌐 **Sphère 360° Mixed Reality optionnelle**
- 🎚️ **Bascule VR Room / Mixed Reality via F12**
- 🧱 **Injection fiable des matériaux**
- 💾 **Enregistrer sous** pour la table VR générée
- 🔄 **Mise à jour automatique portable**
- 🌐 **Interface Français / Anglais**
- ⚙️ **Exécutable Windows autonome**

### ✨ AI Artwork Studio — v1.6

La version 1.6 transforme l'ancien workflow Gemini en **AI Artwork Assistant / AI Artwork Studio** multi-provider.

Services Web pris en charge :

- **Gemini**
- **ChatGPT**

Aucune API payante n'est nécessaire. VPX VR Injector prépare le prompt et le dossier d'images, puis ouvre le site de l'IA choisie afin que l'utilisateur colle le prompt et glisse-dépose les images manuellement.

Nouveautés IA :

- choix clair du provider **Gemini / ChatGPT**
- prompts adaptés au provider
- ajout d'images de référence externes depuis le PC, en plus des images extraites de la table VPX
- génération guidée de plusieurs slots
- présélection automatique du slot lorsqu'on lance l'assistant depuis l'éditeur
- import direct des résultats HD téléchargés
- ajout automatique du masque `*_Empty` après import
- mode **Artwork générique** pour créer une image libre réutilisable
- formats Artwork générique :
  - Paysage **16:9**
  - Portrait **9:16**
  - Carré **1:1**
- fichiers de prompt distincts :
  - `gemini_prompt.txt`
  - `chatgpt_prompt.txt`

> La génération IA reste un workflow Web manuel. VPX VR Injector ne contourne ni l'interface, ni les limites, ni les conditions de compte des fournisseurs.

---

### 🚀 Démarrage rapide

1. Téléchargez la dernière version depuis la [page Releases](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)
2. Extrayez `VpxVRInjector.zip`
3. Lancez `VpxVRInjector.exe`
4. Sélectionnez une table `.vpx`
5. Choisissez un VR Pack
6. Laissez **Dimensions auto** activé dans la majorité des cas
7. Ajustez éventuellement les valeurs Generic ou chargez un preset
8. Personnalisez les artworks avec les images de la table, l'éditeur ou l'AI Artwork Assistant
9. Utilisez éventuellement **🧹 VR Cleanup**
10. Vérifiez éventuellement le résultat avec l'**Aperçu 3D**
11. Cliquez sur **Injecter VR**
12. Choisissez le nom et le dossier de destination

Le nom proposé utilise généralement :

```text
NomDeLaTable_VR.vpx
```

> **Sauvegarde originale est désactivée par défaut.** Activez-la manuellement si vous souhaitez une copie de sécurité supplémentaire.

> Pour les **tables EM** ou les tables utilisant un affichage intégré au backglass, conservez un fichier `.directb2s` à côté de la table VR générée et renommez-le afin que son nom de base corresponde exactement au fichier `_VR.vpx`.

> **Configuration requise :** Windows 10/11

---

### 📦 Packs VR inclus

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
