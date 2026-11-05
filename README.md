# Modèle de soutenance de PFE — Master TSI (M2), Aix-Marseille Université

Modèle Beamer pour la soutenance du projet de fin d'études (PFE) du Master
Traitement du Signal et des Images (TSI) : format 16:9, en français, avec
un thème sobre (`pfetsi`) livré dans le dépôt.

Le fichier [`soutenance.pdf`](soutenance.pdf) montre le résultat attendu.
Les diapositives reprennent le projet d'exemple du
[modèle de rapport](https://github.com/mmnawaf/report-template).

## Contenu du dépôt

```
soutenance.tex            Diaporama à compléter (point d'entrée)
beamerthemepfetsi.sty     Thème (ne pas modifier)
references.bib            Bibliographie
figures/                  Figures et schéma TikZ
soutenance.pdf            Exemple compilé
```

## Structure du diaporama

| Section | Diapositives |
|---|---|
| — | Titre et plan (une seule diapositive) |
| Introduction | Contexte et motivation ; problématique et objectifs |
| État de l'art | Méthodes existantes |
| Méthodologie | Formulation du problème ; méthode proposée ; extension |
| Expérimentations | Données et protocole ; résultats quantitatifs ; résultats qualitatifs |
| Conclusion | Conclusion et perspectives |
| — | Merci — Questions ? |
| Annexes | Diapositives de secours pour les questions (non comptées) |

## Compiler

**Overleaf (recommandé).** Téléchargez le dépôt au format ZIP (bouton
*Code → Download ZIP*), puis dans Overleaf : *New Project → Upload Project*.
Le document principal est `soutenance.tex`.

**En local** (TeX Live 2023 ou plus récent, avec `biber`) :

```bash
latexmk -pdf soutenance.tex   # compilation
latexmk -c                    # nettoyage des fichiers auxiliaires
```

## Aide-mémoire

Chaque élément est illustré et commenté dans `soutenance.tex`.

| Élément | Commande |
|---|---|
| Diapositive de titre et plan | `\diapotitre` |
| Diapositive de clôture | `\diapoquestions` |
| Diapositive | `\begin{frame}{Titre} ... \end{frame}` |
| Deux colonnes | `\begin{columns} \begin{column}{0.48\textwidth} ...` |
| Encadrés | `block`, `alertblock`, `exampleblock` |
| Mise en évidence | `\alert{texte}` |
| Apparition des points un par un | `\begin{itemize}[<+->]` |
| Apparition d'un élément à l'étape *n* | `\uncover<n->{...}` |
| Notes de l'orateur | `\note[item]{...}` (affichage : voir le préambule) |
| Annexes non comptées | `\annexes`, puis les diapositives de secours |
| Version imprimable sans animations | option `handout` de `\documentclass` |
| Diapositives de transition entre sections | `\usetheme[intercalaires]{pfetsi}` |
| Logos en bas à gauche | `\logos{figures/logos/a, figures/logos/b}` |

## Conseils pour la soutenance

- Une idée par diapositive, énoncée dans son titre.
- Peu de texte : des mots-clés, pas des phrases ; le discours complète.
- Des figures lisibles depuis le fond de la salle ; reprenez celles du
  rapport et agrandissez-les.
- Des résultats chiffrés et comparés à une méthode de référence.
- Répartissez la parole entre les membres du groupe et répétez en vous
  chronométrant.
- Préparez des diapositives de secours en annexe pour les questions
  probables.
