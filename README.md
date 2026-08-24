<p align="center">
  <img src="stormstack.png" width="170" alt="Stormstack">
</p>

<h1 align="center">STORMSTACK</h1>

<p align="center">
  Empilement de photos d'orage dans le navigateur. Un seul fichier HTML, aucun serveur, aucun envoi.
</p>

<p align="center">
  <a href="https://infinition.github.io/stormstack/"><b>Ouvrir l'application</b></a>
</p>

---

## Ce que ça fait

Photographier un orage donne une rafale d'images presque identiques, chacune avec un ou deux éclairs.
Stormstack les superpose et les fusionne en mode Éclaircir, ce qui ne retient que les pixels les plus
clairs de chaque calque. Résultat : tous les éclairs de la séquence sur une seule image, sans toucher
au ciel de fond.

Le masque de chaque calque se peint à la main, en coordonnées image, donc il suit le calque quand on
le déplace ou le redimensionne.

Tout se passe dans l'onglet. Les photos ne quittent jamais la machine.

## Utilisation

1. Glisse tes photos n'importe où sur la page, ou clique **+ Importer**.
2. Le premier calque reste en Normal, les suivants passent en **Éclaircir**. Le bouton ⚡ force tous
   les calques supérieurs dans ce mode.
3. Aligne les calques : glisse l'image dans le canevas, tire une **poignée d'angle** pour l'échelle,
   ou saisis les valeurs au pixel dans le panneau.
4. **Gomme** pour effacer une zone du calque actif (un éclair parasite, un reflet), **Restaurer** pour
   la ramener. Dureté et flux règlent le bord de la brosse.
5. **Exporter PNG**.

### Ajustements

Par calque et pour l'ensemble : `Contenir`, `Couvrir`, `Largeur`, `Hauteur`, `1:1`, `Centrer`.
Utile quand les photos ne sortent pas toutes du même boîtier ou du même recadrage.

### Réglage fin

Opacité, échelle, X et Y disposent chacun d'un curseur, d'un champ de saisie directe et de pas fins.
X et Y se règlent au pixel avec `+1` / `-1`, par dix avec `+10` / `-10`, et aux flèches du clavier.

## Raccourcis

| Touche | Action |
| --- | --- |
| `V` | Déplacer |
| `E` | Gomme |
| `R` | Restaurer |
| `[` `]` | Taille de brosse |
| Flèches | Déplacer le calque de 1 px (10 px avec `Maj`) |
| `F` | Ajuster la vue |
| `Échap` | Fermer le panneau des calques |
| `Ctrl` + `Z` | Annuler |
| `Ctrl` + `Maj` + `Z` | Rétablir |
| Molette | Zoom |
| Espace ou clic droit | Déplacer la vue |

## Mobile et tablette

L'interface s'adapte au tactile : cibles élargies, panneau des calques escamotable, poignées de
redimensionnement agrandies, marges gérées autour des encoches.

- Un doigt : outil actif.
- Deux doigts : zoom et déplacement de la vue.
- Le panneau des calques se referme d'un appui hors de sa zone.

Sur iOS, `Partager → Sur l'écran d'accueil` installe l'application en plein écran. À l'export, le PNG
s'ouvre dans un onglet : `Partager → Enregistrer dans Photos`.

## Formats et limites

Les formats lus sont ceux du navigateur : JPEG, PNG, WebP, AVIF, TIFF, GIF, BMP.

**HEIC** n'est décodable par aucun navigateur de bureau. Si tes photos viennent d'un iPhone, règle
`Réglages → Appareil photo → Formats → Plus compatible`, ou convertis-les en JPEG. L'application
détecte le cas et le signale.

La résolution de travail est plafonnée pour tenir dans la mémoire canvas, très limitée sur iOS. Le
réglage **Travail** va de 2048 px à la pleine résolution et s'applique aux imports suivants. Si
l'export échoue faute de mémoire, baisse ce réglage.

## Installation locale

Aucune dépendance, aucune étape de build. Télécharge `index.html` et ouvre-le. Le fichier est
autonome, icônes comprises, et fonctionne hors ligne.

## Limites connues

Les chaînes de l'interface sont en français, écrites en dur. Le passage à une base multilingue reste
à faire.

## Licence

MIT.
