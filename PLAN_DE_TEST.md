# PLAN DE TEST

## Objectif
Ce document décrit la stratégie de test de l'application City Explorer, en se concentrant sur la fonctionnalité de filtrage des villes.

---

## Analyse des Risques

### Risques Projet
| Risque | Probabilité | Impact | Criticité |
|--------|------------|--------|----------|
| Manque de temps pour implémenter tous les tests | Élevée | Moyenne | Élevée |
| Mauvaise configuration des outils de test | Moyenne | Moyenne | Moyenne |

### Risques Produit
| Risque | Probabilité | Impact | Criticité |
|--------|------------|--------|----------|
| Mauvais rayon de recherche | Moyenne | Moyenne | Élevée |
| Filtre incorrect (population / région) | Élevée | Élevée | Critique |

---

## Périmètre des Tests

La campagne de test se concentre uniquement sur :
> **La fonctionnalité de filtrage des villes**
- Filtre par population
- Filtre par région

---

## Approches de Test

Les tests seront réalisés selon une approche en pyramide :

- **Tests unitaires** : validation des fonctions isolées (ex : formatage, filtres)
- **Tests d’intégration** : vérification de la communication entre API et base de données
- **Tests système (E2E)** : simulation du comportement utilisateur avec Cypress
- **Tests d’acceptation** : validation manuelle des scénarios utilisateurs

---

## Critères de sortie

La campagne de test est considérée comme terminée lorsque :

- Tous les tests unitaires passent avec succès
- Les endpoints principaux retournent un statut **200 OK**
- Le filtre de recherche fonctionne correctement dans l’interface
- Aucun bug bloquant n’est présent sur la fonctionnalité testée

---

## Livrables de tests

Les éléments produits durant cette campagne sont :

- Le fichier `PLAN_DE_TEST.md`
- Les fichiers de tests unitaires
- Les tests d’intégration (API)
- Le dossier Cypress contenant les tests E2E
- Le cahier de recette rempli (tests d’acceptation)

---

## Tâches à réaliser

- Identifier une fonction à tester (unitaire)
- Écrire au moins 2 tests unitaires
- Tester un endpoint de recherche (intégration)
- Installer et configurer Cypress
- Créer un test E2E simple
- Rédiger et exécuter les tests d’acceptation

---

## Besoins en ressources

### Humaines
- 1 développeur (réalisation des tests)

### Matérielles
- Ordinateur de développement
- Node.js / Java
- Navigateur web
- Cypress

---

## Risques et contingences

- **Risque : Cypress ne fonctionne pas correctement**
  → Solution : simplifier les tests ou tester manuellement

- **Risque : manque de temps**
  → Solution : prioriser une seule fonctionnalité (filtrage)

- **Risque : erreurs API**
  → Solution : tester avec des données fixes