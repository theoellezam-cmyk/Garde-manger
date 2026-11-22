# Garde-Manger

Application web installable (PWA) pour gérer le stock du frigo, du congélateur et du placard, et la liste de courses d'un foyer.

**Ouvrir l'appli :** https://theoellezam-cmyk.github.io/Garde-manger/

## Fonctions

- **Scanner** en direct avec la caméra (codes-barres EAN/UPC et QR codes), ou depuis une photo.
  - *Ranger* : ajoute le produit au stock et le retire de la liste de courses.
  - *Utiliser* : décompte la quantité consommée.
  - *À racheter* : ajoute le produit à la liste de courses.
- **Reconnaissance des produits** via [Open Food Facts](https://fr.openfoodfacts.org) (nom, marque, contenance, rayon). Un produit inconnu est saisi une fois puis reconnu aux scans suivants.
- **Stock** trié par date limite, par emplacement, avec alertes « à consommer vite ».
- **Courses** rangées par rayon, suggestions des produits terminés ou sous leur seuil de rachat, rangement des achats cochés en un geste.
- **Hors ligne** : l'appli fonctionne sans réseau (seule la recherche Open Food Facts en a besoin).
- **Sauvegarde** : export et import d'un fichier JSON (Stock → Sauvegarde).

Les données sont enregistrées uniquement sur le téléphone (stockage local du navigateur). Rien n'est envoyé ailleurs, à part le code-barres scanné, envoyé à Open Food Facts pour identifier le produit.

## Installer sur le téléphone

- **iPhone** : ouvrir le lien dans Safari → bouton Partager → « Sur l'écran d'accueil ».
- **Android** : ouvrir le lien dans Chrome → bouton « Installer l'appli » en haut, ou menu ⋮ → « Installer l'application ».

## Fichiers

| Fichier | Rôle |
| --- | --- |
| `index.html` | L'application (HTML, CSS et JavaScript dans un seul fichier) |
| `manifest.webmanifest` | Nom, icône et mode plein écran de l'appli installée |
| `sw.js` | Cache hors ligne. Augmenter `VERSION` à chaque mise en ligne |
| `vendor/zxing.min.js` | Lecture des codes-barres ([ZXing](https://github.com/zxing-js/library) 0.21.3, licence Apache-2.0) |
| `icons/` | Icônes de l'appli |

Mise en ligne : GitHub Pages, branche `main`, dossier racine.

## Crédits

Données produits : [Open Food Facts](https://world.openfoodfacts.org), sous licence [ODbL](https://opendatacommons.org/licenses/odbl/1-0/).
