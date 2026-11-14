# Deux pages de garde – Mémoire CCP2 ECSR

Le projet contient **deux versions A4 portrait** placées au début du PDF :

1. **Couverture 1 – LaTeX/TikZ modifiable** : `couverture.tex` et textes dans `couverture_config.tex`.
2. **Couverture 2 – Illustration fixe** : `couverture_image.tex` et `images/couverture_image_session_2026_2027.png`, portant la mention **Session 2026–2027**.

## Conserver une seule couverture à la fin

Dans `main.tex`, repérer ces paramètres :

```latex
\CouvertureEditabletrue
\CouvertureImagetrue
```

- **Les deux** : conserver `true` pour les deux.
- **Seulement la version LaTeX** : remplacer `\CouvertureImagetrue` par `\CouvertureImagefalse`.
- **Seulement la version image** : remplacer `\CouvertureEditabletrue` par `\CouvertureEditablefalse`.

Ouvrir `main.tex` dans VS Code et compiler avec **Ctrl+Alt+B** (LaTeX Workshop + MiKTeX + Perl). Les pages après les couvertures gardent le format A4 portrait.

### Remarque sur l'éditabilité

Seule la première couverture est intégralement éditable dans LaTeX pour ses titres et légendes. Les textes de la seconde font partie de l'image PNG : changer leur contenu exige de modifier l'image ou de basculer sur la version TikZ.

# Mémoire CCP2 ECSR – Couverture éditable

## Modifier les textes de couverture
Ouvrir `couverture_config.tex` et remplacer les valeurs entre accolades, sans supprimer les commandes.
Les lignes du titre, le sous-titre, les quatre piliers, le lieu et la signature sont modifiables.

## Modifier le graphisme
Le fichier `couverture.tex` utilise TikZ (dessins vectoriels). Les images de marque institutionnelles sont `images/logo_aftral.png` et `images/logo_afpa.png`. La photographie est `images/photo_conducteur.png`.

## Compiler sous Windows
Installer MiKTeX, Strawberry Perl, VS Code et LaTeX Workshop ; ouvrir ce dossier et lancer `Ctrl+Alt+B` sur `main.tex`.
Compiler avec pdfLaTeX/latexmk. La couverture est A4 portrait comme tout le mémoire.

## Structure
Les dix chapitres existants sont conservés dans `chapitres/`.

Les visuels institutionnels sont extraits de l'image de référence fournie. Vérifier la conformité des logos si besoin d'une impression officielle.
