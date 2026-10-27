# Carte des réalisations – Sénégal

Prototype de cartographie web conçu par **CEGIT** (Centre d'Expertise en Géomatique et Ingénierie Territoriale, https://cegitgroup.com) pour permettre à l'État du Sénégal et aux collectivités territoriales de communiquer sur les réalisations de leurs mandats.

## Fonctionnalités

- Carte des 14 régions avec les projets livrés, en chantier ou programmés, pictogramme par type d'ouvrage
- Fiche projet : description, emplacement, montant, financement, calendrier, avancement, photos, sources officielles
- Filtres : porteur (État / collectivités), avancement, provenance des données (réelles / exemples), région, orientation Sénégal 2050, secteur, année de livraison
- Points d'attention : échéance dépassée, adaptation au climat, égalité femmes-hommes
- Vue « Investissement par région » (carte choroplèthe)
- Liens Street View, Google Maps et Mapillary pour chaque projet
- Visite guidée automatique pour les présentations
- Export CSV de la sélection
- Lien partageable vers chaque fiche (`#projet-103`)

## Données

- **Projets réels** : issus des communiqués du Conseil des ministres, de la loi de finances initiale 2026 et de la presse (Le Soleil, APS, Dakaractu, Ndarinfo). Chaque fiche renvoie vers sa source. Montants tels qu'annoncés, données arrêtées au 27 octobre 2026.
- **Exemples** : projets fictifs, signalés comme tels, illustrant l'usage par les communes et départements.
- **Limites administratives** : [geoBoundaries](https://www.geoboundaries.org) (CC BY 4.0).

## Ajouter des photos

1. Déposer les images (JPEG, PNG ou WebP) dans le dossier `photos/`.
2. Les déclarer dans `photos/photos.json`, en utilisant l'identifiant du projet (visible dans le lien de la fiche, par exemple `#projet-103`) :

```json
{
  "103": [
    { "src": "photos/aeroport-ziguinchor-piste.jpg", "legende": "Piste réhabilitée", "credit": "Ministère des Infrastructures" }
  ]
}
```

Tant qu'aucune photo n'est déclarée pour un projet, sa fiche affiche une illustration. N'utiliser que des photos dont les droits sont acquis.

## Publication

Site statique : aucun serveur requis. Activer GitHub Pages sur la branche `main` (dossier racine).

© 2026 CEGIT – Prototype de démonstration.
