<div align="center">

<img width="200" height="200" alt="icon" src="https://github.com/user-attachments/assets/e2707416-3ea2-47e2-9a3d-a18011f054c0" />



# VPX VR Injector

**Inject VR Rooms into any Visual Pinball X table — no VR source required.**

[![Version](https://img.shields.io/badge/version-1.5-blueviolet?style=flat-square)](https://github.com/Nesta78/VPX-VR-INJECTOR/releases)
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
- 💾 **Choose the output location — new in 1.2** — select the filename and folder of the generated VR table with a standard Save As dialog
- 🔄 **Automatic VR Wall orientation — new in 1.2** — Left / Right Wall textures are shown in the natural orientation in the GUI and automatically rotated as required during VPX injection
- ⚡ **Smoother source-image extraction — new in 1.2** — image decoding and thumbnail generation run in the background so the GUI stays responsive
- 🧊 **Integrated 3D VR Room Preview — new in 1.3** — inspect the selected pack directly inside VPX VR Injector using the real VPX meshes, UV mapping and currently selected textures
- 🎥 **Interactive 3D views — new in 1.3** — orbit, zoom and switch between Front / Left / Right / Rear / Top / 3/4 views without launching VPX
- 🧹 **VR Cleanup — new in 1.3** — inspect source-table objects before injection and make selected objects invisible only in the generated VR table
- ⚠️ **Rail / Rails cleanup suggestions — new in 1.3** — likely problematic rail objects are automatically shown first and can be selected in one click
- ✨ **Gemini artwork assistant — new in 1.1** — select several images extracted from the source table, choose a target texture slot, and prepare a slot-specific prompt plus the correct green-mask template for Gemini Web
- 🧠 **Slot-aware Gemini prompts — new in 1.1** — dedicated instructions for Cabinet, Backbox, Backglass, VR Walls, Floor and Roof, including strict green-mask preservation and cabinet-side orientation rules
- 📂 **Automatic Gemini bundle — new in 1.1** — creates a temporary folder containing the selected reference images, the matching green template and a text copy of the generated prompt
- 🪟 **Improved Gemini window — new in 1.2** — native minimize / maximize / restore controls for the Gemini preparation dialog
- 🎨 **AI / artist reminder — new in 1.2** — the interface reminds users that AI can help create quick artwork, while original work from graphic artists remains the preferred choice whenever available
- 🧩 **Texture Editor** — multi-layer composition, positioning, scaling, rotation, mirroring, keyboard nudging and layer reordering
- 📋 **Paste image as a new layer — new in 1.1** — use the Paste Image button or `Ctrl+V` to add an image from the Windows clipboard directly into the editor
- ✨ **Gemini assistant from the editor — new in 1.1** — launches the same multi-reference Gemini workflow available from the main window
- 🎨 **Gemini Artwork Studio — new in 1.5** — prepare several artwork slots in one guided session while reusing the same reference selection and Gemini conversation
- 🧭 **Context-aware Gemini target — new in 1.5** — when Gemini is opened from the texture editor, the slot currently being edited is selected automatically
- 📋 **Reliable manual Gemini prompt workflow — new in 1.5** — prompts are copied to the clipboard but never pasted automatically; prepared image bundles are opened for manual drag-and-drop into the same Gemini conversation
- 📥 **HD Gemini result import — new in 1.5** — import the downloaded high-resolution result directly into the correct slot; when a matching `*_Empty` mask exists, the editor automatically places it above the generated artwork
- ✂️ **Inline layer crop — new in 1.5** — crop the selected layer directly inside the texture editor canvas while preserving the cropped artwork's visible size and position
- 🕹️ **Progressive VR plunger animation — new in 1.5** — the injected `PinCab_Shooter` follows a progressive pull/release animation instead of jumping instantly to full travel
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
- 🔄 **Automatic portable updater — new in 1.4** — checks GitHub Releases automatically, downloads and validates the update, safely replaces the portable installation, rolls back on failure and relaunches VPX VR Injector
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
6. Optionally reuse images embedded in the source table, customize them in the built-in editor, crop layers directly on the canvas, or prepare artwork with Gemini / Gemini Artwork Studio
7. Optionally open **🧹 VR Cleanup** to hide source-table objects that should not remain visible in VR.
8. Optionally open the **3D VR Room Preview** to inspect the cabinet and Room before injection.
9. **Inject** — choose where to save the generated `.vpx` file, then open it in Visual Pinball X with VR mode enabled.

> **Original backup is disabled by default in 1.3.** Enable it manually if you want VPX VR Injector to create an additional safety copy.

> For **EM tables**, or tables whose score/display is integrated into the backglass, keep a `.directb2s` file in the same folder and rename it so its base filename exactly matches the generated `_VR.vpx` table.

> **Requirements:** Windows 10/11

---

### 🆕 What's new in 1.2 → 1.5

#### Version 1.2

- The generated VR table can now be saved **wherever you want** using a standard **Save As** dialog.
- **Left / Right Wall orientation is handled automatically**: walls are shown naturally in the GUI/editor and rotated as required only for VPX injection.
- Source-table image extraction was moved to a **background worker**, keeping the loading animation and interface much smoother.
- The Gemini preparation window now supports native **minimize / maximize / restore** controls.
- A short reminder was added to the Gemini workflow: AI is useful for quick artwork creation, but **original artwork from graphic artists remains the preferred choice whenever available**.
- Special thanks added for **Speedygonzales**, for extensive testing and feedback.

#### Version 1.3

- Added an integrated **3D VR Room Preview** directly inside VPX VR Injector — no need to launch VPX.
- The viewer uses the **real VPX meshes, object transforms and UV mapping** from the selected pack, together with the textures currently selected in the GUI.
- Preview the **Cabinet, Backbox, Backglass, Walls, Floor, Roof and other pack hardware** in one complete 3D scene.
- Interactive controls include orbit, zoom and preset **Front / Left / Right / Rear / Top / 3/4** views.
- The 3D viewer uses an **OpenGL depth buffer** for clean surface occlusion and is fully translated in English and French.
- Added **🧹 VR Cleanup** to inspect source-table objects before injection.
- Objects containing **Rail / Rails** are highlighted as cleanup suggestions because they are frequent sources of visual conflicts in injected VR Rooms.
- Search the source object list, select the objects to hide and VPX VR Injector sets their visibility to **False only in the generated VR table**.
- VR Cleanup supports the different VPX visibility fields used by Ramps, Primitives, Flashers, Flippers, Triggers, Gates, Spinners and other supported object types.
- **Original backup is now disabled by default**, while remaining available as an optional safety feature.

#### Version 1.4

- Added a **fully automatic portable updater** based on GitHub Releases.
- VPX VR Injector can automatically check for a newer version at startup, in addition to the manual Help menu check.
- Updates are downloaded to a temporary staging area and validated before the current installation is touched.
- The dedicated updater waits for VPX VR Injector to close, safely replaces the portable files, preserves user data, and relaunches the application.
- A previous-version backup and rollback path are kept so a failed replacement can be restored safely.

#### Version 1.5

- Added **Gemini Artwork Studio** for preparing several artwork slots in one guided session.
- Reference images are selected once and reused across the selected slots. Cabinet, Backbox and Backglass are selected by default; VR Walls, Floor and Roof remain optional.
- The Studio is launched from the existing Gemini window instead of adding another button to the main interface.
- Gemini should remain in the **same conversation** for all selected slots. The current prompt is copied to the clipboard and the prepared image bundle is opened for manual drag-and-drop.
- Automatic prompt pasting was removed for reliability: the user remains in control of when the prompt is pasted into Gemini.
- Generated HD images downloaded from Gemini can be imported directly into the correct slot. If a matching `*_Empty` mask exists, it is automatically placed above the imported artwork in the editor.
- When Gemini is opened from the texture editor, the **currently edited slot is preselected automatically**.
- Added **inline layer cropping** directly on the texture-editor canvas, with resize/move handles, Apply / Cancel / Reset controls and keyboard validation. The cropped area keeps its visual size and position instead of being resized after validation.
- Added a **progressive VR plunger animation** for the injected `PinCab_Shooter`, avoiding the instant full-travel effect of earlier experiments.
- 
All previous Gemini, Mixed Reality, source-image extraction, Generic preset, DigitGrid, material-injection and texture-editor features remain available.


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
- 💾 **Choix de l'emplacement de sortie — nouveauté 1.2** — choisissez le nom et le dossier de la table VR générée via une boîte Enregistrer sous
- 🔄 **Orientation automatique des murs VR — nouveauté 1.2** — les murs gauche/droit sont affichés dans le bon sens dans le GUI puis retournés automatiquement comme nécessaire lors de l'injection VPX
- ⚡ **Extraction des images plus fluide — nouveauté 1.2** — décodage des images et création des miniatures en arrière-plan afin de garder l'interface réactive
- 🧊 **Aperçu 3D intégré de la VR Room — nouveauté 1.3** — visualisez le pack sélectionné directement dans VPX VR Injector avec les vrais meshes VPX, leurs UV et les textures actuellement choisies
- 🎥 **Vues 3D interactives — nouveauté 1.3** — rotation libre, zoom et vues Avant / Gauche / Droite / Arrière / Dessus / 3/4 sans lancer VPX
- 🧹 **VR Cleanup — nouveauté 1.3** — inspectez les objets de la table source avant injection et rendez certains objets invisibles uniquement dans la table VR générée
- ⚠️ **Suggestions Rail / Rails — nouveauté 1.3** — les objets susceptibles de poser problème en VR sont automatiquement remontés en priorité
- ✨ **Assistant de génération d'artwork avec Gemini — nouveauté 1.1** — sélectionnez plusieurs images extraites de la table source, choisissez un slot cible et préparez automatiquement un prompt adapté ainsi que le bon template à masque vert pour Gemini Web
- 🧠 **Prompts Gemini adaptés au slot — nouveauté 1.1** — instructions dédiées pour Cabinet, Backbox, Backglass, murs VR, sol et plafond, avec respect strict du masque vert et règles d'orientation spécifiques au cabinet
- 📂 **Dossier Gemini automatique — nouveauté 1.1** — création d'un dossier temporaire contenant les images de référence sélectionnées, le template vert correspondant et une copie texte du prompt généré
- 🪟 **Fenêtre Gemini améliorée — nouveauté 1.2** — contrôles natifs réduire / agrandir / restaurer dans la fenêtre de préparation Gemini
- 🎨 **Rappel IA / graphistes — nouveauté 1.2** — le logiciel rappelle que l'IA peut aider à créer rapidement un artwork, mais que le travail original des graphistes reste le choix privilégié lorsqu'il est disponible
- 🧩 **Éditeur de textures** — calques multiples, déplacement, redimensionnement, rotation, miroir, ajustement au clavier et réorganisation
- 📋 **Coller une image comme nouveau calque — nouveauté 1.1** — utilisez le bouton Coller une image ou `Ctrl+V` pour ajouter directement dans l'éditeur une image présente dans le presse-papiers Windows
- ✨ **Assistant Gemini depuis l'éditeur — nouveauté 1.1** — ouvre le même workflow multi-images que celui disponible depuis la fenêtre principale
- 🎨 **Gemini Artwork Studio — nouveauté 1.5** — préparez plusieurs slots d'artwork dans une seule session guidée en réutilisant la même sélection d'images de référence et la même conversation Gemini
- 🧭 **Cible Gemini contextuelle — nouveauté 1.5** — lorsque Gemini est ouvert depuis l'éditeur de textures, le slot en cours d'édition est automatiquement présélectionné
- 📋 **Workflow Gemini manuel plus fiable — nouveauté 1.5** — le prompt est copié dans le presse-papiers mais n'est jamais collé automatiquement ; les dossiers d'images préparés sont ouverts pour être glissés-déposés manuellement dans la même conversation Gemini
- 📥 **Import HD du résultat Gemini — nouveauté 1.5** — importez directement l'image haute résolution téléchargée dans le bon slot ; lorsqu'un masque `*_Empty` correspondant existe, l'éditeur le place automatiquement au-dessus de l'artwork généré
- ✂️ **Rognage directement dans l'éditeur — nouveauté 1.5** — rognez le calque sélectionné directement sur le canvas tout en conservant la taille et la position visuelles de la zone conservée
- 🕹️ **Animation progressive du plunger VR — nouveauté 1.5** — le `PinCab_Shooter` injecté suit un mouvement progressif lors du tirage et du relâchement au lieu de passer instantanément à sa course maximale
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
- 🔄 **Mise à jour automatique portable — nouveauté 1.4** — vérifie automatiquement les Releases GitHub, télécharge et valide la mise à jour, remplace l'installation portable de façon sûre, restaure l'ancienne version en cas d'échec puis relance VPX VR Injector
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
6. Réutilisez éventuellement les images intégrées à la table source, personnalisez-les dans l'éditeur, rognez les calques directement sur le canvas ou préparez des artworks avec Gemini / Gemini Artwork Studio
7. Ouvrez éventuellement **🧹 VR Cleanup** pour masquer les objets de la table source qui ne doivent pas rester visibles en VR.
8. Utilisez éventuellement l'**Aperçu 3D de la VR Room** pour vérifier le cabinet et la Room avant injection.
9. **Injectez** — choisissez où enregistrer le fichier `.vpx` généré, puis ouvrez-le dans Visual Pinball X avec le mode VR activé.

> **Sauvegarde originale est désactivée par défaut depuis la 1.3.** Activez-la manuellement si vous souhaitez créer une copie de sécurité supplémentaire.

> Pour les **tables EM**, ou les tables dont le score/l'affichage est intégré au backglass, conservez un fichier `.directb2s` dans le même dossier et renommez-le afin que son nom de base corresponde exactement à celui de la table `_VR.vpx` générée.

> **Configuration requise :** Windows 10/11

---

### 🆕 Nouveautés 1.2 → 1.5

#### Version 1.2

- La table VR générée peut maintenant être enregistrée **où vous le souhaitez** grâce à une boîte **Enregistrer sous**.
- L'orientation des **murs gauche / droit** est gérée automatiquement : ils sont affichés dans le bon sens dans le GUI/éditeur et retournés uniquement lorsque VPX en a besoin lors de l'injection.
- L'extraction des images de la table source est maintenant exécutée dans un **worker en arrière-plan**, ce qui rend la barre de chargement et l'interface beaucoup plus fluides.
- La fenêtre de préparation Gemini possède désormais les contrôles natifs **réduire / agrandir / restaurer**.
- Un rappel a été ajouté dans le workflow Gemini : l'IA est pratique pour créer rapidement, mais **le travail original des graphistes reste le choix privilégié lorsqu'il est disponible**.
- Ajout de remerciements spéciaux à **Speedygonzales** pour ses nombreux tests et retours.

#### Version 1.3

- Ajout d'un **Aperçu 3D intégré de la VR Room** directement dans VPX VR Injector, sans lancer VPX.
- Le viewer utilise les **vrais meshes VPX, transformations d'objets et coordonnées UV** du pack sélectionné, avec les textures actuellement choisies dans le GUI.
- Visualisation du **Cabinet, Backbox, Backglass, murs, sol, plafond et autres éléments matériels du pack** dans une scène 3D complète.
- Contrôles interactifs : rotation libre, zoom et vues **Avant / Gauche / Droite / Arrière / Dessus / 3/4**.
- Le viewer 3D utilise un **depth buffer OpenGL** pour une occultation propre des surfaces et possède une interface entièrement traduite FR/EN.
- Ajout de **🧹 VR Cleanup** pour inspecter les objets de la table source avant injection.
- Les objets contenant **Rail / Rails** sont mis en avant comme suggestions, car ils provoquent fréquemment des conflits visuels dans les VR Rooms injectées.
- Recherche dans la liste, sélection des objets à masquer, puis passage de leur visibilité à **False uniquement dans la table VR générée**.
- VR Cleanup gère les différents champs de visibilité VPX utilisés notamment par les Ramps, Primitives, Flashers, Flippers, Triggers, Gates, Spinners et autres types pris en charge.
- **Sauvegarde originale est désormais décochée par défaut**, tout en restant disponible comme option de sécurité.

#### Version 1.4

- Ajout d'un **système de mise à jour automatique portable** basé sur les Releases GitHub.
- VPX VR Injector peut vérifier automatiquement au démarrage si une nouvelle version existe, en complément de la vérification manuelle du menu Aide.
- La mise à jour est téléchargée dans une zone temporaire et validée avant toute modification de l'installation actuelle.
- L'updater dédié attend la fermeture de VPX VR Injector, remplace proprement les fichiers portables, conserve les données utilisateur puis relance l'application.
- Une sauvegarde de la version précédente et une procédure de rollback permettent de restaurer l'installation en cas d'échec.

#### Version 1.5

- Ajout du **Gemini Artwork Studio** pour préparer plusieurs slots d'artwork dans une seule session guidée.
- Les images de référence sont sélectionnées une seule fois puis réutilisées pour les slots choisis. Cabinet, Backbox et Backglass sont cochés par défaut ; les murs VR, le sol et le plafond restent optionnels.
- Le Studio est accessible depuis la fenêtre Gemini existante afin de ne pas ajouter un nouveau bouton dans l'interface principale.
- Il faut conserver **la même conversation Gemini** pour tous les slots sélectionnés. Le prompt courant est copié dans le presse-papiers et le dossier d'images préparé s'ouvre pour permettre un glisser-déposer manuel.
- Le collage automatique du prompt a été supprimé pour plus de fiabilité : l'utilisateur choisit lui-même quand le coller dans Gemini.
- Les images HD téléchargées depuis Gemini peuvent être importées directement dans le bon slot. Si un masque `*_Empty` correspondant existe, il est automatiquement ajouté au-dessus de l'artwork importé dans l'éditeur.
- Lorsque Gemini est lancé depuis l'éditeur de textures, le **slot actuellement édité est automatiquement présélectionné**.
- Ajout du **rognage directement sur le canvas** de l'éditeur, avec poignées de déplacement/redimensionnement, Appliquer / Annuler / Reset et validation clavier. La zone conservée garde sa taille et sa position visuelles au lieu d'être redimensionnée après validation.
- Ajout d'une **animation progressive du plunger VR** pour le `PinCab_Shooter` injecté, afin d'éviter un passage instantané à la course maximale.
Toutes les fonctions précédentes Gemini, Mixed Reality, extraction d'images, presets Generic, DigitGrid, injection des matériaux et éditeur restent disponibles.


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

Made with ❤️ for the VPX VR Pinball community — thank you to **Sixtoe & Dardog** for the VR Room resources, and special thanks to **Speedygonzales** for extensive testing and feedback.

[⬆ Back to top](#vpx-vr-injector)

</div>
