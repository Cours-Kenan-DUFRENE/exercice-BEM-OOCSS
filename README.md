# Atelier avancé — Refonte d'une page e‑commerce (BEM + OOCSS + SCSS)

## Objectif
Refactorer **entièrement** cette page afin d'obtenir une architecture **professionnelle** :
- **BEM** (structure locale des composants)
- **OOCSS** (objets réutilisables)
- **CSS** ou **SCSS**

> Vous devez décider de la structure. Aucune solution n'est fournie dans ces fichiers.
> Testez, justifiez, itérez.

---

## Critères d'acceptation (à respecter absolument)
- Aucune classe **visuelle** dans le HTML final (`.blue`, `.big`, `.white`, etc.) ✅
- Pas d'éléments imbriqués BEM du type `__` en cascade (`.block__el__sub`) ❌
- Les objets OOCSS (`.box`, `.media`, `.grid`, `.button`) sont **réutilisables** et **indépendants** ✅
- Le CSS final est issu d'une **compilation SCSS** propre (fichiers partiels + `style.scss`) ✅
- Responsive **mobile-first** et focus visibles (accessibilité) ✅

---

## Étapes guidées

### 1) Cartographier
- Listez **vos blocs BEM** (header, nav, hero, product-grid, product-card, promo-banner, footer).
- Listez **les éléments** de chaque bloc (ex: `product-card__image`, `product-card__title`, etc.).
- Définissez **les modificateurs** (`product-card--promo`, `button--primary`, `nav__link--active`, `promo-banner--dark`).

### 2) Renommer dans `index.html`
- Remplacez toutes les classes génériques par vos noms **BEM**.
- Conservez la sémantique HTML (pas de `div` inutile).

### 3) Extraire les **objets OOCSS**
- Système de boutons `.button` + modifiers (`--primary`, `--secondary`, `--success`, `--ghost`, `--lg`, `--block`).
- `.box` : conteneur visuel générique (fond, border, shadow, padding).
- `.media` : alignement visuel image + texte.
- `.grid` : `.grid--cols-3`, `.grid--cols-4` avec responsive.

### 4) Refactorer les **composants BEM**
- **Header** : brand/logo, nav, CTA login.
- **Hero** : titres, sous-titres, actions, media.
- **Product grid** : titre + liste de **product-card** (promo vs normal).
- **Promo banner** : variante sombre + image.
- **Footer** : colonnes + liens.

### 5) Responsive & a11y
- Mobile-first : 1 colonne → 2 → 4.
- Focus visibles sur les liens/boutons.
- Masquage `.only-desktop` géré proprement via utilitaire.

---

## 💾 Livrables
- `index.html` refactoré en BEM
- `css/` + `style.css`
- (Optionnel) `DECISIONS.md` : expliquez votre choix d’architecture.

Bon courage. La **qualité de l’architecture** compte autant que le rendu.
