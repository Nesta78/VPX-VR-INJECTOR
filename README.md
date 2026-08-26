<div align="center">

<img width="200" height="200" alt="icon" src="https://github.com/user-attachments/assets/e2707416-3ea2-47e2-9a3d-a18011f054c0" />



# VPX VR Injector

**Inject VR Rooms into any Visual Pinball X table — no VR source required.**

[![Version](https://img.shields.io/badge/version-0.96-blueviolet?style=flat-square)](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)
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
- 🖼️ **Source table image extraction — new in 0.96** — browse artwork embedded in the original VPX and reuse it for the VR cabinet
- 🔎 **Smart artwork suggestions** — likely backglass, cabinet, blades, speaker, apron and other useful images are highlighted automatically
- 👁️ **Hover previews** for extracted table images
- 🧩 **Texture Editor** — multi-layer composition, positioning, scaling, rotation, mirroring and layer reordering
- ⧉ **Duplicate layers — new in 0.96**
- 🗂️ **Available Images inside the editor — new in 0.96** — add an extracted source-table image directly as a new layer
- 🎭 **Smart `*_Empty` mask workflow** — when available, the selected artwork is placed underneath the pack mask automatically
- 🔢 **DigitGrid / Flasher DMD support** — automatic detection and repositioning for non-standard VPX displays
- 🌐 **Bilingual interface** — English and French (FR/EN)
- 🔔 **Update checker** — notified when a new version is available on GitHub
- 🛡️ **Non-destructive** — the injected table is saved separately and an optional backup can be created
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

### 🆕 What's new in 0.96

Version **0.96** focuses on artwork reuse and faster VR cabinet customization:

- **Generic value presets** can be created, deleted, imported and exported as `.vrippreset` files.
- Images embedded in the **source VPX table** can be extracted automatically.
- The injector suggests useful artwork candidates while still providing a **Show all** view.
- Extracted images can be previewed by **hovering their names**.
- **Use as...** can send an extracted image directly to a compatible texture slot.
- When a matching `*_Empty` mask exists, the editor automatically places the selected artwork **under the mask**.
- Layers can now be **duplicated**.
- The texture editor includes an **Available Images** browser so extracted source-table artwork can be added without leaving the editor.
- Image extraction was made more robust by validating and normalizing embedded images before preview/use.

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
- 🖼️ **Extraction des images de la table source — nouveauté 0.96** — réutilisez les artworks intégrés au fichier VPX
- 🔎 **Suggestions intelligentes d'artworks** — backglass, cabinet, blades, speaker, apron et autres images utiles sont mises en avant
- 👁️ **Aperçu au survol** des images extraites
- 🧩 **Éditeur de textures** — calques multiples, déplacement, redimensionnement, rotation, miroir et réorganisation
- ⧉ **Duplication des calques — nouveauté 0.96**
- 🗂️ **Images disponibles dans l'éditeur — nouveauté 0.96** — ajout direct d'une image extraite comme nouveau calque
- 🎭 **Gestion intelligente des masques `*_Empty`** — l'artwork choisi est automatiquement placé sous le masque du pack
- 🔢 **Support des DMD DigitGrid / Flashers** — détection et repositionnement automatiques des affichages VPX non standards
- 🌐 **Interface bilingue** — Français et Anglais (FR/EN)
- 🔔 **Vérificateur de mises à jour** — notification lorsqu'une nouvelle version est disponible sur GitHub
- 🛡️ **Non-destructif** — la table injectée est sauvegardée séparément et une sauvegarde optionnelle peut être créée
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

### 🆕 Nouveautés 0.96

La version **0.96** améliore surtout la réutilisation des artworks et la personnalisation du cabinet VR :

- Les **presets de valeurs Generic** peuvent être créés, supprimés, importés et exportés au format `.vrippreset`.
- Les images intégrées dans la **table VPX source** peuvent être extraites automatiquement.
- Le logiciel propose une sélection d'images potentiellement utiles tout en conservant un affichage **Tout afficher**.
- Les images extraites disposent d'un **aperçu au survol**.
- **Utiliser comme...** permet d'envoyer une image extraite directement vers un slot compatible.
- Lorsqu'un masque `*_Empty` correspondant existe, l'éditeur place automatiquement l'artwork **sous le masque**.
- Les calques peuvent maintenant être **dupliqués**.
- L'éditeur dispose d'un bouton **Images disponibles** pour ajouter les artworks extraits sans revenir à l'écran principal.
- L'extraction des images a été renforcée grâce à une validation et une normalisation des formats avant aperçu/utilisation.

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
