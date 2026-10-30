# 📸 Nina Carducci – Débogage et optimisation d'un site de photographe

🌐 **Site en ligne :** https://moldu77.github.io/Site-web-Nina-Carducci-Photographe/

🇫🇷 Français · 🇬🇧 [English](#-english)

## Contexte

Projet réalisé dans le cadre de la formation **Développeur Web d'OpenClassrooms**.
Nina Carducci, photographe à Bordeaux, souhaitait améliorer les performances, le référencement et l'accessibilité de son site portfolio, et faire corriger deux bugs de sa galerie. Ma mission : auditer le site existant, le corriger et l'optimiser, puis rendre compte de l'intervention à la cliente.

## Résultats

Scores Lighthouse avant → après optimisation :

| | Performances | Accessibilité | Bonnes pratiques | SEO |
|---|:---:|:---:|:---:|:---:|
| 🖥️ Desktop | 65 → **98** | 68 → **100** | 100 → **100** | 70 → **100** |
| 📱 Mobile | 66 → **91** | 73 → **100** | 100 → **96** | 73 → **100** |

- **Poids des images :** 30,9 Mo → 0,43 Mo (**−98,6 %**, environ 72 fois plus léger)
- **Audit WAVE (accessibilité) :** 17 erreurs → **0**, score AIM 4,7 → **9,4 / 10**
- **Cahier de recette :** 22 tests fonctionnels, tous validés

## Ce que j'ai fait

**Bugs corrigés** (`maugallery.js`)
- Les flèches de la fenêtre d'agrandissement ne changeaient pas de photo : elles passent maintenant à la suivante ou à la précédente, et bouclent en fin de liste
- Le filtre sélectionné n'était plus mis en évidence : il reçoit maintenant le fond doré

**Performances**
- Images converties en WebP et redimensionnées, avec des versions plus légères pour mobile (`<picture>`)
- Chargement différé des images hors écran, chargement prioritaire de la première image du carrousel
- Hauteur fixe du carrousel pour stabiliser l'affichage (CLS), scripts chargés avec `defer`

**SEO**
- Titre, description, langue et consignes pour les robots d'indexation
- Référencement local avec Schema.org (adresse, téléphone, horaires)
- Balises Open Graph et Twitter Card pour l'aperçu lors des partages
- Structure sémantique : un seul titre principal, hiérarchie des titres sans saut, balises `header`, `nav`, `main`, `section`

**Accessibilité**
- Textes alternatifs sur toutes les images
- Champs du formulaire reliés à leur intitulé, champs obligatoires
- Boutons du carrousel en français, lien Instagram explicite et sécurisé, curseur adapté sur les éléments cliquables

**Livrables** : rapport d'intervention pour la cliente et cahier de recette

## Technologies

HTML5 · CSS3 · JavaScript · Bootstrap · Lighthouse · WAVE · Schema.org · GitHub Pages

## Lancer le projet en local

```bash
git clone https://github.com/Moldu77/Site-web-Nina-Carducci-Photographe.git
```

Puis ouvrir `index.html` dans le navigateur (ou utiliser l'extension Live Server de VS Code).

---

## 🇬🇧 English

**Context:** project completed as part of the **OpenClassrooms Web Developer** program. The goal was to audit, debug and optimize the existing portfolio website of a photographer based in Bordeaux, then report the work to the client.

**Results (Lighthouse, before → after):**

| | Performance | Accessibility | Best practices | SEO |
|---|:---:|:---:|:---:|:---:|
| 🖥️ Desktop | 65 → **98** | 68 → **100** | 100 → **100** | 70 → **100** |
| 📱 Mobile | 66 → **91** | 73 → **100** | 100 → **96** | 73 → **100** |

- **Image weight:** 30.9 MB → 0.43 MB (**−98.6%**)
- **WAVE accessibility audit:** 17 errors → **0**, AIM score 4.7 → **9.4 / 10**
- **Test plan:** 22 functional tests, all passed

**What I did:**

- **Bug fixes** in `maugallery.js`: lightbox previous/next navigation, active filter highlighting
- **Performance:** WebP images in several sizes (`<picture>`), lazy loading, carousel height fixed to reduce CLS, deferred scripts
- **SEO:** meta tags, local SEO with Schema.org, Open Graph and Twitter Card, semantic HTML structure
- **Accessibility:** alt texts, labelled form fields, French carousel controls, explicit Instagram link
- **Deliverables:** client report and test plan

**Tech stack:** HTML5 · CSS3 · JavaScript · Bootstrap · Lighthouse · WAVE · Schema.org · GitHub Pages

---

👤 **Auteur / Author :** Maxym Duculty – [LinkedIn](https://www.linkedin.com/in/maxym-duculty) · [GitHub](https://github.com/Moldu77)
