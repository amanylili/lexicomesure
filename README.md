# Lexicomesure

**Lexicomesure** est un logiciel libre d'analyse lexicométrique (textométrie) de corpus, en français. Son nom dit ce qu'il fait : prendre la mesure du lexique d'un corpus.

Il tient dans une seule page HTML. Il fonctionne dans n'importe quel navigateur récent, sans installation, sans serveur et sans connexion internet. Les textes analysés ne quittent jamais l'ordinateur.

Il s'inspire des grands logiciels de la tradition française d'analyse des données textuelles : Iramuteq, Lexico, Hyperbase, Le Trameur, SATO et DTM-Vic.

## Utilisation

1. Téléchargez `index.html` (ou clonez le dépôt).
2. Ouvrez le fichier par un double-clic dans Chrome, Firefox ou Edge.
3. Collez un texte, ouvrez des fichiers `.txt` ou chargez le corpus d'exemple, puis cliquez sur **Analyser le corpus**.

Si GitHub Pages est activé sur ce dépôt, le logiciel s'utilise aussi directement en ligne.

## Format du corpus

Le format Iramuteq est reconnu. Chaque texte commence par une ligne étoilée qui porte ses variables :

```
**** *auteur_hugo *genre_roman *decennie_1860
Texte du premier document…

**** *auteur_zola *genre_roman *decennie_1880
Texte du deuxième document…
```

Un fichier sans ligne étoilée devient un texte unique, avec la variable `*fichier`.

## Analyses disponibles

| Analyse | Description | Logiciels qui l'ont inspirée |
|---|---|---|
| Statistiques | Occurrences, formes, hapax, loi de Zipf, croissance du vocabulaire, gamme des fréquences | Lexico, Hyperbase |
| Dictionnaire | Formes et fréquences, avec mots-outils et formes pleines | Lexico |
| Concordancier | Contexte de chaque occurrence ; troncature `*`, alternatives `\|`, expressions de plusieurs mots, expressions régulières | Le Trameur, SATO, Lexico |
| Cooccurrents | Formes attirées autour d'un pôle, avec un score hypergéométrique | Lexico, Le Trameur |
| Segments répétés | Suites de formes répétées, sans franchir la ponctuation | Lexico |
| Spécificités | Modèle hypergéométrique de Lafon, par variable, par texte ou par tranche | Lexico, Hyperbase |
| Ventilation | Répartition d'une ou plusieurs formes dans les parties | Hyperbase, Le Trameur |
| AFC | Analyse factorielle des correspondances : valeurs propres, coordonnées, contributions, cos² | DTM-Vic, Lexico |
| Classification de Reinert | CHD sur segments de texte : dendrogramme, profils, anti-profils, variables, segments caractéristiques, AFC des classes | Iramuteq (Alceste) |
| Similitudes | Arbre maximum des cooccurrences, détection de communautés | Iramuteq |
| Nuage de mots | Par corpus ou par modalité | Iramuteq |

Chaque tableau s'exporte en CSV (séparateur point-virgule). Chaque graphique s'exporte en SVG ou en PNG.

## Limites

- Il n'y a pas de lemmatisation par dictionnaire : les analyses portent sur les formes graphiques. Une option regroupe seulement le singulier et le pluriel.
- La classification de Reinert est une CHD simple. Elle ne fait pas la double classification d'Iramuteq.

## Licence

MIT
