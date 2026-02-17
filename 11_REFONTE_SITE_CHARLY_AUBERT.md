# REFONTE SITE CHARLYAUBERT.COM — Specification

*Mise a jour : 13 fevrier 2026*
*Reference : `10_POSITIONNEMENT_CHARLY_AUBERT_2026.md`*

---

## 1. Diagnostic du site actuel

### Ce qui ne va pas

**Positionnement obsolete**
- "Creer une vie alignee et abondante" = dev perso generique. N'importe quel coach pourrait ecrire ca.
- Aucune mention du pont tech/terre, de l'IA, de la paille, du contraste qui fait l'unicite de Charly.

**NILA OS est une offre fantome**
- 197 EUR, 6 modules, temoignages generiques (Marie L., Thomas B., Sophie D.)
- L'offre n'a jamais ete vendue de maniere significative
- Elle entre en conflit avec Clarte (meme promesse)
- La page de vente est un template infoproducteur classique

**"Mon histoire" est factice**
- Timeline inventee ("2010 : monde corporate"). La vraie histoire est infiniment plus interessante.
- Charly etait chez les Temoins de Jehovah, puis Epitech, puis Londres, puis investissement immobilier, puis LAOM. Rien de ca n'apparait.

**Social proof generique**
- "5000+ lecteurs", "400+ visiteurs accueillis" avec compteurs animes
- Temoignages sans photos, avec des prenoms generiques
- Ca sonne faux et ca tue la credibilite

**Esthetique anonyme**
- Template Ali Abdaal (cercle jaune, cartes arrondies, gradients bleus)
- Pourrait etre n'importe qui. Ne reflete pas Charly.

**Structure trop lourde**
- 5 sections sur la home, une page NILA OS de 500 lignes, une page "mon histoire"
- Trop de CTA, trop de promesses, trop de contenu pour un site qui n'a pas de trafic

---

## 2. Le nouveau positionnement

Reference : `10_POSITIONNEMENT_CHARLY_AUBERT_2026.md`

> **Charly Aubert aide les gens a utiliser la technologie la plus avancee pour se reconnecter a ce qui ne change jamais : le corps, la terre, et la clarte interieure.**

Le site n'est **pas** une landing page de conversion. La conversion se fait sur laom.fr.
Le site est un **index personnel** : voici qui je suis, voici ce que je pense, voici ou me trouver.

---

## 3. Architecture proposee

### Page unique : index.astro

Le site tient en une seule page, sobre et puissante. Pas de menu complexe. Pas de sous-pages inutiles.

#### Bloc 1 — Hero

```
[Photo contraste : Charly au chantier / Charly devant l'ecran]

Charly Aubert

Je construis le plus grand batiment en paille porteuse au monde.
Je pilote ma vie avec une IA.
Je crois que l'ancrage rend la technologie utile.

[LinkedIn] [YouTube] [Newsletter]
```

- Pas de "Salut, wave emoji". Pas de compteurs animes. Pas de "5000+ lecteurs".
- Une photo reelle, pas un portrait avec cercle jaune.
- Le contraste tech/terre doit etre visible dans l'image ET dans le texte.

#### Bloc 2 — Ce que j'ecris

```
Articles

[Liste des 3-5 derniers articles, heberges sur laom.fr/blog]
- Comment je pilote un ecolieu avec une IA
- Grand Shambala : 850m2 de paille porteuse
- Petit Shambala : le batiment qu'on n'avait jamais prevu
- [Article a venir : Talisman v2]
- [Article a venir : Conscience et souverainete (reecrit)]

Chaque article = titre + 1 ligne de description + lien vers laom.fr/blog/[slug]
```

- Les articles vivent sur laom.fr. Le site Charly est un index.
- Pas de blog autonome sur charlyaubert.com.

#### Bloc 3 — LAOM

```
LAOM

Un ecolieu de 21 hectares dans le sud de l'Aveyron.
Retraites, festival, coliving.

[Photo aerienne LAOM]

[Decouvrir LAOM → laom.fr]
[Prochains evenements → laom.fr/events]
```

- C'est le pont vers la marque lieu. Court. Visuel. Un lien.

#### Bloc 4 — Newsletter

```
Chaque dimanche, je partage mes reflexions.
Pas de spam. Pas de tunnels. Juste de la pensee.

[Email] [S'inscrire]
```

- Formulaire Kit (deja en place).
- Pas de social proof. Pas de "rejoins X lecteurs".

#### Footer

```
Charly Aubert — 2026
[LinkedIn] [YouTube] [Instagram LAOM] [laom.fr]
```

### Pages supprimees

- `/nila-os` : **supprimee**. Redirection vers laom.fr/clarte
- `/mon-histoire` : **supprimee** pour l'instant. Si on la reecrit un jour, ce sera la vraie histoire.
- `/blog/*` : **supprime**. Les articles sont sur laom.fr

---

## 4. Esthetique et design

### Principes

- **Minimaliste** : une page, 4 blocs, c'est tout
- **Lumineux et naturel** : fond clair (blanc casse / creme), pas de gradients
- **Grain argentique** : photos avec un traitement leger, pas sur-saturees
- **Vert / blanc** : palette principale (coherent avec la note de reference originale)
- **Typo sobre** : Inter ou similaire. Pas de serif precieux. Pas de display font.
- **Aucun emoji** dans le contenu
- **Aucun compteur anime**, aucun carrousel, aucun marquee

### Photos necessaires

1. **Hero** : photo de Charly qui montre le contraste. Options :
   - Split screen : chantier a gauche, ecran a droite
   - Charly devant le Grand Shambala avec un laptop
   - Charly les mains pleines de terre, coupe, Charly devant Claude
2. **LAOM** : vue aerienne (deja disponible dans `/images/laom/`)
3. **Pas de photo portrait avec cercle jaune Ali Abdaal**

---

## 5. Stack technique

- **Framework** : Astro (deja en place dans le repo)
- **Hebergement** : Cloudflare Pages (coherent avec laom.fr)
- **Newsletter** : Kit / ConvertKit (deja en place)
- **Domaine** : charlyaubert.com ou charlyaubert.fr (a acheter/configurer)
- **CSS** : inline dans le composant Astro. Pas de framework CSS. Le site est si simple qu'il n'en a pas besoin.

### Simplification du code

Le site actuel a 1400+ lignes de CSS pour la home. Le nouveau site devrait tenir en 200-300 lignes max. On supprime :
- Tous les composants NILA OS
- Toute la section "help" (Ali Abdaal style)
- Toute la section methode
- Toute la section mentorat
- Tous les ebooks
- Tous les temoignages generiques
- Toute l'animation JS (compteurs, wave, intersection observer)

---

## 6. SEO

### Objectif

Quand quelqu'un tape "Charly Aubert" sur Google, il tombe sur ce site. Le site fait le pont vers LAOM.

### Meta

```
title: "Charly Aubert"
description: "Constructeur, fondateur de LAOM, explorateur du pont entre technologie et ancrage."
```

### Liens sortants

- laom.fr (toutes les pages articles, offres, events)
- YouTube (@charlyaubert)
- LinkedIn (profil Charly)
- Instagram (LAOM)

### Schema markup

Person schema pour Charly Aubert. Lie a LAOM (Organization schema sur laom.fr).

---

## 7. Ce que le site n'est PAS

- Pas un blog autonome (les articles sont sur laom.fr)
- Pas un e-commerce
- Pas une landing page de conversion (la conversion est sur laom.fr)
- Pas un portfolio artistique
- Pas une page "a propos" de 3000 mots
- Pas un template infoproducteur
- Pas un CV

---

## 8. Planning de refonte

Voir le plan d'action dans la section suivante du document.
