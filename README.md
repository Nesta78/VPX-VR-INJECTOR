<div align="center">

<img width="200" height="200" alt="icon" src="https://github.com/user-attachments/assets/e2707416-3ea2-47e2-9a3d-a18011f054c0" />



# VPX VR Injector

**Inject VR Rooms into any Visual Pinball X table — no VR source required.**

[![Version](https://img.shields.io/badge/version-0.97-blueviolet?style=flat-square)](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)
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
- 🧩 **Texture Editor** — multi-layer composition, positioning, scaling, rotation, mirroring, keyboard nudging and layer reordering
- ⇋ **Duplicate to opposite side — new in 0.97** — instantly create a mirrored, symmetrically positioned copy for cabinet side artwork
- 🪟 **Improved editor windows — new in 0.97** — native minimize/maximize controls and more comfortable editing
- ⧉ **Duplicate layers — new in 0.96**
- 🗂️ **Available Images inside the editor — new in 0.96** — add an extracted source-table image directly as a new layer
- 🎭 **Smart `*_Empty` mask workflow** — when available, the selected artwork is placed underneath the pack mask automatically
- 🔢 **DigitGrid / Flasher DMD support** — automatic detection and repositioning for non-standard VPX displays
- 🌐 **Mixed Reality 360° sphere — new in 0.97** — optional MR sphere with Green, Magenta, White or Black chroma-key colors
- 🎚️ **In-game VR/MR switch — new in 0.97** — use the VPX F12 menu to switch between the standard VR Room and Mixed Reality
- 🧱 **Safer material injection — new in 0.97** — fixes duplicated / missing materials and pink VR objects on affected tables
- 🌐 **Bilingual interface** — English and French (FR/EN)
- 🔔 **Update checker** — notified when a new version is available on GitHub
- 🛡️ **Non-destructive** — the injected table is saved separately and an optional backup can be created
- 🖥️ **Improved layout — new in 0.97** — scrollable options panel, always-visible Inject VR button and a more compact log area
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

### 🆕 What's new in 0.97

Version **0.97** focuses on Mixed Reality support, texture-editor usability, material reliability and pack accuracy:

- **Optional 360° Mixed Reality sphere** can be injected with the VR Room.
- Four MR sphere colors are available: **Green** (`0,255,0`), **Magenta** (`255,0,255`), **White** (`255,255,255`) and **Black** (`0,0,0`).
- When the MR option is enabled, the generated table receives a **VPX F12 option** to switch between **VR Room** and **Mixed Reality** while in game.
- The standard **VR Room remains the default** when the table starts.
- The texture editor now supports **keyboard nudging**: arrow keys move the active image by 1 px, while **Shift + Arrow** moves it by 10 px.
- Image resizing from corners was corrected so dragging outward always enlarges and dragging inward always reduces, including mirrored artwork.
- **Duplicate to opposite side** automatically creates/updates a mirrored copy and positions it symmetrically across the vertical center line — ideal for cabinet side art.
- Texture-editor windows now use the **native Windows minimize / maximize / restore / close controls**.
- Material injection was reworked to correctly keep legacy and modern VPX material structures synchronized, preventing **duplicated material entries / Dear ImGui ID conflict warnings**.
- Material availability checks were hardened to prevent VR objects from referencing materials that were not actually injected, fixing affected **pink / magenta objects**.
- The **Bally pack** was refreshed from a new reference VR Room, preserving its updated material definitions.
- Bally backglass adaptation was corrected so the backglass keeps the reference scale instead of being distorted by automatic table-length scaling.
- Selected **WPC95 Bally / WPC95 Williams** VR metal parts now use **Metal Chrome** where configured in the 0.97 packs.
- The main interface was compacted: the right-side options area is **scrollable**, **Inject VR stays visible**, and the **LOG panel is smaller**.

All 0.96 artwork-extraction, Generic preset, `*_Empty` mask and editor features remain available in 0.97.


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
- 🧩 **Éditeur de textures** — calques multiples, déplacement, redimensionnement, rotation, miroir, ajustement au clavier et réorganisation
- ⇋ **Dupliquer à l'opposé — nouveauté 0.97** — crée instantanément une copie miroir positionnée symétriquement pour les side arts du cabinet
- 🪟 **Fenêtres d'édition améliorées — nouveauté 0.97** — boutons Windows natifs réduire / agrandir / restaurer
- ⧉ **Duplication des calques — nouveauté 0.96**
- 🗂️ **Images disponibles dans l'éditeur — nouveauté 0.96** — ajout direct d'une image extraite comme nouveau calque
- 🎭 **Gestion intelligente des masques `*_Empty`** — l'artwork choisi est automatiquement placé sous le masque du pack
- 🔢 **Support des DMD DigitGrid / Flashers** — détection et repositionnement automatiques des affichages VPX non standards
- 🌐 **Sphère 360° Mixed Reality — nouveauté 0.97** — sphère MR optionnelle avec couleurs Vert, Magenta, Blanc ou Noir
- 🎚️ **Bascule VR/MR en jeu — nouveauté 0.97** — le menu F12 de VPX permet de passer de la VR Room standard à la Mixed Reality
- 🧱 **Injection des matériaux fiabilisée — nouveauté 0.97** — correction des matériaux dupliqués / manquants et des objets VR roses
- 🌐 **Interface bilingue** — Français et Anglais (FR/EN)
- 🔔 **Vérificateur de mises à jour** — notification lorsqu'une nouvelle version est disponible sur GitHub
- 🛡️ **Non-destructif** — la table injectée est sauvegardée séparément et une sauvegarde optionnelle peut être créée
- 🖥️ **Interface optimisée — nouveauté 0.97** — panneau d'options scrollable, bouton Injecter VR toujours visible et zone LOG plus compacte
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

### 🆕 Nouveautés 0.97

La version **0.97** apporte surtout le support Mixed Reality, des améliorations importantes de l'éditeur de textures, une injection des matériaux plus fiable et plusieurs corrections de packs :

- Une **sphère 360° Mixed Reality** peut maintenant être injectée en option avec la VR Room.
- Quatre couleurs de sphère MR sont proposées : **Vert** (`0,255,0`), **Magenta** (`255,0,255`), **Blanc** (`255,255,255`) et **Noir** (`0,0,0`).
- Si l'option MR est activée, la table générée reçoit une option **F12 dans VPX** permettant de basculer en jeu entre **VR Room** et **Mixed Reality**.
- La **VR Room standard reste le mode par défaut** au lancement de la table.
- L'éditeur de textures permet maintenant le **déplacement précis au clavier** : les flèches déplacent l'image active de 1 px, et **Shift + Flèche** de 10 px.
- Le redimensionnement par les coins a été corrigé : tirer vers l'extérieur agrandit toujours l'image et revenir vers l'intérieur la réduit, y compris sur une image en miroir.
- Le bouton **Dupliquer à l'opposé** crée/met à jour automatiquement une copie miroir et la place symétriquement par rapport à l'axe vertical central — idéal pour les side arts de caisse.
- Les fenêtres de l'éditeur utilisent maintenant les boutons **Windows natifs réduire / agrandir / restaurer / fermer**.
- L'injection des matériaux VPX a été revue afin de synchroniser correctement les structures legacy et modernes, ce qui supprime les **doublons de matériaux / warnings Dear ImGui d'ID en conflit**.
- Les vérifications des matériaux réellement injectés ont été renforcées afin d'éviter les références invalides responsables d'**objets roses / magenta**.
- Le **pack Bally** a été reconstruit à partir d'une nouvelle VR Room de référence tout en conservant ses matériaux mis à jour.
- L'adaptation du backglass Bally a été corrigée afin qu'il conserve l'échelle de référence au lieu d'être déformé par le redimensionnement automatique lié à la longueur de la table.
- Certaines pièces métalliques VR des packs **WPC95 Bally / WPC95 Williams** utilisent désormais **Metal Chrome** conformément aux réglages de la 0.97.
- L'interface principale a été compactée : panneau droit **scrollable**, bouton **Injecter VR toujours visible** et zone **LOG réduite**.

Toutes les fonctions de la 0.96 liées à l'extraction d'images, aux presets Generic, aux masques `*_Empty` et à l'éditeur restent disponibles dans la 0.97.


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
