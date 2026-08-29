<div align="center">

<img width="200" height="200" alt="icon" src="https://github.com/user-attachments/assets/e2707416-3ea2-47e2-9a3d-a18011f054c0" />



# VPX VR Injector

**Inject VR Rooms into any Visual Pinball X table — no VR source required.**

[![Version](https://img.shields.io/badge/version-1.2-blueviolet?style=flat-square)](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=flat-square&logo=python)](https://www.python.org/)
[![Platform](https://img.shields.io/badge/platform-Windows-lightgrey?style=flat-square&logo=windows)](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)

</div>

<div align="center">📘 [Documentation / Wiki](https://github.com/Nesta78/VPX-VR-INJECTOR/wiki)</div>

---

## 🇬🇧 English

### What is VPX VR Injector?

**VPX VR Injector** is a tool that brings VR support to Visual Pinball X tables that were never designed for it. Instead of waiting for table authors to release a VR version, you can inject a full VR Room — cabinet, backglass, topper, floor — directly into any `.vpx` file, in just a few clicks.

The tool works by directly manipulating the **OLE Compound File** format of `.vpx` files, inserting 3D primitives, textures, materials, and the necessary VBScript code, while correctly updating all internal counters and structures that VPX requires to load the new objects.

---

### ✨ Features

- 🎮 **One-click VR injection** into any existing `.vpx` table
- 📦 **Curated VR Packs** — Stern Modern, Data East Classic, WPC95, WPC Williams, Bally, Showcase, Old School, and more
- ⚡ **Automatic VR Room scaling** based on the source table playfield dimensions
- 🎛️ **Generic value presets** — save, delete, import and export reusable Width / Length / X / Y / Z adjustments
- ↔️ **Centered Generic X coordinate — new in 1.0** — `X = 0` keeps the cabinet horizontally centered while Width changes
- ℹ️ **Old School proportional-dimension warning — new in 1.0** — clearly explains that large Width / Length values are proportional and can create very large geometry changes
- 🖼️ **Source table image extraction** — browse artwork embedded in the original VPX and reuse it for the VR cabinet
- 🔎 **Smart artwork suggestions** — likely backglass, cabinet, blades, speaker, apron and other useful images are highlighted automatically
- 👁️ **Hover previews** for extracted table images
- ✨ **Gemini artwork assistant — new in 1.1** — select several images extracted from the source table, choose a target texture slot, and prepare a slot-specific prompt plus the correct green-mask template for Gemini Web
- 🧠 **Slot-aware Gemini prompts — new in 1.1** — dedicated instructions for Cabinet, Backbox, Backglass, VR Walls, Floor and Roof, including strict green-mask preservation and cabinet-side orientation rules
- 📂 **Automatic Gemini bundle — new in 1.1** — creates a temporary folder containing the selected reference images, the matching green template and a text copy of the generated prompt
- 🧩 **Texture Editor** — multi-layer composition, positioning, scaling, rotation, mirroring, keyboard nudging and layer reordering
- 📋 **Paste image as a new layer — new in 1.1** — use the Paste Image button or `Ctrl+V` to add an image from the Windows clipboard directly into the editor
- ✨ **Gemini assistant from the editor — new in 1.1** — launches the same multi-reference Gemini workflow available from the main window
- ⇋ **Duplicate to opposite side** — instantly create a mirrored, symmetrically positioned copy for cabinet side artwork
- 🪟 **Improved editor windows** — native minimize/maximize controls and more comfortable editing
- ⧉ **Duplicate layers**
- 🗂️ **Available Images inside the editor** — add an extracted source-table image directly as a new layer
- 🎭 **Smart `*_Empty` mask workflow** — when available, the selected artwork is placed underneath the pack mask automatically
- 🔢 **DigitGrid / Flasher DMD support** — automatic detection and repositioning for non-standard VPX displays
- 🌐 **Mixed Reality 360° sphere** — optional MR sphere with Green, Magenta, White or Black chroma-key colors
- 🎚️ **In-game VR/MR switch** — use the VPX F12 menu to switch between the standard VR Room and Mixed Reality
- 🧱 **Safer material injection** — fixes duplicated / missing materials and pink VR objects on affected tables
- 🌐 **Bilingual interface** — English and French (FR/EN)
- 🔔 **Update checker** — notified when a new version is available on GitHub
- 🛡️ **Non-destructive** — the injected table is saved separately and an optional backup can be created
- 🖥️ **Improved layout** — scrollable options panel, always-visible Inject VR button and a more compact log area
- ⚙️ **Standalone executable** — no Python installation required; just download and run

---

### 🚀 Getting Started

1. **Download** the latest release from the [Releases page](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)
2. **Extract** `VpxVRInjector.zip` anywhere on your machine
3. **Run** `VpxVRInjector.exe`
4. **Select** your `.vpx` table file
5. **Choose** a VR Pack from the list
6. Optionally reuse images embedded in the source table or customize them in the built-in editor
7. **Inject** — done! Open the output file in Visual Pinball X with VR mode enabled

> For **EM tables**, or tables whose score/display is integrated into the backglass, keep a `.directb2s` file in the same folder and rename it so its base filename exactly matches the generated `_VR.vpx` table.

> **Requirements:** Windows 10/11

---

### 🆕 What's new in 1.1

Version **1.1** focuses on artwork creation and makes it much easier to build custom VR textures from the artwork already stored inside a VPX table.

- **Generate artwork with Gemini** is now available directly from the main window.
- Select **multiple source-table images** and use them together as visual references for Gemini.
- Choose the target slot before generation: **Cabinet, Backbox, Backglass, VR Wall Left, VR Wall Right, Floor or Roof**, depending on the selected pack and available templates.
- VPX VR Injector automatically selects the matching **green-mask template** for the current VR pack and target slot.
- The generated Gemini prompt is **slot-specific**. Cabinet prompts include mirrored side-art rules, 90° side-panel orientation, protected hardware/cutouts and strict instructions to fill every green pixel without painting outside the mask.
- A dedicated temporary folder is created containing the selected reference images, the correct template and `gemini_prompt.txt`.
- The prompt is copied to the clipboard and VPX VR Injector opens the temporary folder and Gemini Web. Drag the prepared images into Gemini and paste the prompt to generate the artwork.
- The workflow uses **Gemini Web**, so VPX VR Injector does not require a Gemini API key, paid API integration or its own AI server.
- The built-in texture editor can now **paste an image from the clipboard as a new layer** using the Paste Image button or `Ctrl+V` — useful for bringing a Gemini result straight back into the editor.
- The texture editor now exposes the **same Generate artwork with Gemini assistant** as the main window instead of a separate simplified workflow.
- Generic X positioning uses a **centered coordinate system**: `X = 0` keeps the cabinet horizontally centered when Width changes.
- Old School dimensions now display a contextual warning because **Width / Length are proportional adjustments**; very large values can cause very large geometry changes.

All previous Mixed Reality, source-image extraction, Generic preset, DigitGrid, material-injection and texture-editor features remain available in 1.1.

> **Gemini workflow note:** generated results still depend on Gemini following the supplied mask instructions. The green templates and prompts are designed to strongly constrain the result, but the final image should always be visually checked before use.


### 📦 Included VR Packs

| Pack | Era / Style |
|------|------------|
| Stern Modern | Modern Stern cabinet style |
| Data East Classic | Early 90s Data East |
| WPC95 | Williams WPC-95 era |
| WPC Williams | Classic Williams |
| Bally | Classic Bally |
| Showcase | Display showcase style |
| Old School | EM / early SS era |  
| + more... | |

---

---

## 🇫🇷 Français

### Qu'est-ce que VPX VR Injector ?

**VPX VR Injector** est un outil permettant d'ajouter le support VR aux tables Visual Pinball X qui n'ont jamais été conçues pour la réalité virtuelle. Plutôt que d'attendre qu'un auteur de table publie une version VR, vous pouvez injecter une Salle VR complète — cabinet, backglass, topper, sol — directement dans n'importe quel fichier `.vpx`, en quelques clics.

L'outil fonctionne en manipulant directement le format **OLE Compound File** des fichiers `.vpx` : il insère des primitives 3D, des textures, des matériaux et le code VBScript nécessaire, tout en mettant correctement à jour les compteurs et structures internes requis par VPX pour charger les nouveaux objets.

---

### ✨ Fonctionnalités

- 🎮 **Injection VR en un clic** dans n'importe quelle table `.vpx` existante
- 📦 **VR Packs sélectionnés** — Stern Modern, Data East Classic, WPC95, WPC Williams, Bally, Showcase, Old School, et plus encore
- ⚡ **Adaptation automatique de la VR Room** aux dimensions du playfield de la table source
- 🎛️ **Presets de valeurs Generic** — sauvegarde, suppression, import et export des réglages Width / Length / X / Y / Z
- ↔️ **Coordonnée X Generic centrée — nouveauté 1.0** — `X = 0` conserve le cabinet centré horizontalement lorsque Width change
- ℹ️ **Avertissement dimensions Old School — nouveauté 1.0** — indique clairement que Width / Length sont proportionnels et que de grandes valeurs peuvent provoquer de très grands changements de géométrie
- 🖼️ **Extraction des images de la table source** — réutilisez les artworks intégrés au fichier VPX
- 🔎 **Suggestions intelligentes d'artworks** — backglass, cabinet, blades, speaker, apron et autres images utiles sont mises en avant
- 👁️ **Aperçu au survol** des images extraites
- ✨ **Assistant de génération d'artwork avec Gemini — nouveauté 1.1** — sélectionnez plusieurs images extraites de la table source, choisissez un slot cible et préparez automatiquement un prompt adapté ainsi que le bon template à masque vert pour Gemini Web
- 🧠 **Prompts Gemini adaptés au slot — nouveauté 1.1** — instructions dédiées pour Cabinet, Backbox, Backglass, murs VR, sol et plafond, avec respect strict du masque vert et règles d'orientation spécifiques au cabinet
- 📂 **Dossier Gemini automatique — nouveauté 1.1** — création d'un dossier temporaire contenant les images de référence sélectionnées, le template vert correspondant et une copie texte du prompt généré
- 🧩 **Éditeur de textures** — calques multiples, déplacement, redimensionnement, rotation, miroir, ajustement au clavier et réorganisation
- 📋 **Coller une image comme nouveau calque — nouveauté 1.1** — utilisez le bouton Coller une image ou `Ctrl+V` pour ajouter directement dans l'éditeur une image présente dans le presse-papiers Windows
- ✨ **Assistant Gemini depuis l'éditeur — nouveauté 1.1** — ouvre le même workflow multi-images que celui disponible depuis la fenêtre principale
- ⇋ **Dupliquer à l'opposé** — crée instantanément une copie miroir positionnée symétriquement pour les side arts du cabinet
- 🪟 **Fenêtres d'édition améliorées** — boutons Windows natifs réduire / agrandir / restaurer
- ⧉ **Duplication des calques**
- 🗂️ **Images disponibles dans l'éditeur** — ajout direct d'une image extraite comme nouveau calque
- 🎭 **Gestion intelligente des masques `*_Empty`** — l'artwork choisi est automatiquement placé sous le masque du pack
- 🔢 **Support des DMD DigitGrid / Flashers** — détection et repositionnement automatiques des affichages VPX non standards
- 🌐 **Sphère 360° Mixed Reality** — sphère MR optionnelle avec couleurs Vert, Magenta, Blanc ou Noir
- 🎚️ **Bascule VR/MR en jeu** — le menu F12 de VPX permet de passer de la VR Room standard à la Mixed Reality
- 🧱 **Injection des matériaux fiabilisée** — correction des matériaux dupliqués / manquants et des objets VR roses
- 🌐 **Interface bilingue** — Français et Anglais (FR/EN)
- 🔔 **Vérificateur de mises à jour** — notification lorsqu'une nouvelle version est disponible sur GitHub
- 🛡️ **Non-destructif** — la table injectée est sauvegardée séparément et une sauvegarde optionnelle peut être créée
- 🖥️ **Interface optimisée** — panneau d'options scrollable, bouton Injecter VR toujours visible et zone LOG plus compacte
- ⚙️ **Exécutable autonome** — aucune installation de Python requise ; téléchargez et lancez directement

---

### 🚀 Démarrage rapide

1. **Téléchargez** la dernière version depuis la [page Releases](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)
2. **Extrayez** `VpxVRInjector.zip` où vous le souhaitez
3. **Lancez** `VpxVRInjector.exe`
4. **Sélectionnez** votre fichier `.vpx`
5. **Choisissez** un VR Pack dans la liste
6. Réutilisez éventuellement les images intégrées à la table source ou personnalisez-les dans l'éditeur
7. **Injectez** — c'est tout ! Ouvrez le fichier de sortie dans Visual Pinball X avec le mode VR activé

> Pour les **tables EM**, ou les tables dont le score/l'affichage est intégré au backglass, conservez un fichier `.directb2s` dans le même dossier et renommez-le afin que son nom de base corresponde exactement à celui de la table `_VR.vpx` générée.

> **Configuration requise :** Windows 10/11

---

### 🆕 Nouveautés 1.1

La version **1.1** se concentre sur la création d'artworks et facilite fortement la fabrication de textures VR personnalisées à partir des images déjà présentes dans une table VPX.

- Le bouton **Générer un artwork avec Gemini** est maintenant disponible directement dans la fenêtre principale.
- Vous pouvez sélectionner **plusieurs images de la table source** et les utiliser ensemble comme références visuelles dans Gemini.
- Choisissez le slot à générer : **Cabinet, Backbox, Backglass, Mur VR gauche, Mur VR droit, Sol ou Plafond**, selon le pack sélectionné et les templates disponibles.
- VPX VR Injector sélectionne automatiquement le **template à masque vert** correspondant au pack VR et au slot cible.
- Le prompt Gemini est **adapté au slot**. Pour le Cabinet, il intègre notamment les règles de miroir des sides, leur orientation à 90°, la protection des éléments matériels/découpes et des consignes strictes pour remplir tous les pixels verts sans dépasser du masque.
- Un dossier temporaire dédié est créé avec les images de référence sélectionnées, le bon template et un fichier `gemini_prompt.txt`.
- Le prompt est copié dans le presse-papiers et VPX VR Injector ouvre le dossier temporaire ainsi que Gemini Web. Il suffit ensuite de glisser les images préparées dans Gemini et de coller le prompt.
- Le workflow utilise **Gemini Web** : VPX VR Injector n'a donc besoin ni d'une clé API Gemini, ni d'une API payante, ni de son propre serveur IA.
- L'éditeur de textures permet maintenant de **coller une image du presse-papiers comme nouveau calque** via le bouton Coller une image ou `Ctrl+V` — idéal pour réimporter immédiatement une génération Gemini.
- L'éditeur utilise désormais le **même assistant Générer un artwork avec Gemini** que la fenêtre principale, au lieu d'un workflow Gemini séparé et simplifié.
- Le positionnement Generic en X utilise maintenant un **repère centré** : `X = 0` conserve le cabinet centré horizontalement lorsque Width change.
- Les dimensions du pack Old School affichent désormais un avertissement contextuel : **Width / Length sont des ajustements proportionnels** et des valeurs très élevées peuvent provoquer de très grands changements de géométrie.

Toutes les fonctions précédentes concernant la Mixed Reality, l'extraction d'images, les presets Generic, DigitGrid, l'injection des matériaux et l'éditeur restent disponibles dans la 1.1.

> **À propos de Gemini :** le résultat final dépend toujours de la façon dont Gemini respecte les consignes du masque. Les templates verts et les prompts sont conçus pour fortement contraindre la génération, mais il reste conseillé de vérifier visuellement l'image avant de l'utiliser.


### 📦 VR Packs inclus

| Pack | Ère / Style |
|------|------------|
| Stern Modern | Style cabinet Stern moderne |
| Data East Classic | Data East début des années 90 |
| WPC95 | Ère Williams WPC-95 |
| WPC Williams | Williams classique |
| Bally | Bally classique |
| Showcase | Style vitrine d'exposition |
| Old School | Ère EM / early SS | 
| + d'autres... | |

---

---

<div align="center">

Made with ❤️ for the VPX VR pinball cabinet community - Thank you to Sixtoe & Dardog vor VR Rooms ressources :)

[⬆ Back to top](#vpx-vr-injector)

</div>
