# Étude de Cas – Analyse de la Scalabilité et des Performances des APIs Modernes  
# Par: Rim EL ABBASSI

## 🧩 Contexte

Dans un contexte de forte concurrence et de digitalisation, une plateforme de réservation d’hôtels souhaite implémenter une API robuste permettant de gérer efficacement les réservations clients.  
Cette plateforme doit supporter **des millions de requêtes**, fonctionner dans un environnement **multi-utilisateurs** et rester performante pour des **volumes de données variables**.

Les opérations principales prises en charge sont :

- Création d’une réservation
- Consultation d’une réservation
- Modification d’une réservation
- Suppression (annulation) d’une réservation

L’objectif de cette étude est d’analyser et comparer les **performances** et la **scalabilité** de plusieurs technologies d’API modernes dans un contexte réel.

---

## 🎯 Objectifs de l’Étude

- Comparer les performances des APIs **REST**, **SOAP**, **GraphQL** et **gRPC**
- Évaluer la latence et le débit sous différentes charges
- Mesurer la consommation des ressources système (CPU, mémoire)
- Étudier l’impact de la taille des messages échangés
- Analyser la simplicité d’implémentation et la sécurité de chaque technologie

---

---

## 🔁 Scénarios de Test

### Opérations Testées

- Créer une réservation (POST / Mutation / gRPC call)
- Consulter une réservation (GET / Query / gRPC call)
- Modifier une réservation (PUT / Mutation / gRPC call)
- Supprimer une réservation (DELETE / Mutation / gRPC call)

### Variables de Test

- **Requêtes simultanées** : 10, 100, 500, 1000
- **Taille des messages** :
  - Petit : 1 KB
  - Moyen : 10 KB
  - Grand : 100 KB

---



## 📊 Résultats – Analyse de la Latence (ms)

| Charge | Opération      | REST | SOAP | GraphQL | gRPC |
|------|---------------|------|------|---------|------|
| 10   | Création       | 38   | 62   | 22      | 14   |
| 10   | Consultation   | 31   | 48   | 19      | 11   |
| 100  | Création       | 94   | 130  | 56      | 28   |
| 100  | Consultation   | 76   | 112  | 43      | 21   |
| 500  | Création       | 410  | 520  | 180     | 65   |
| 500  | Consultation   | 388  | 470  | 165     | 58   |
| 1000 | Création       | 720  | 910  | 340     | 112  |
| 1000 | Consultation   | 685  | 860  | 310     | 98   |

---

## 🚀 Résultats – Débit (requêtes/seconde)

| Charge | REST | SOAP | GraphQL | gRPC |
|------|------|------|---------|------|
| 10   | 120  | 90   | 210     | 260  |
| 100  | 480  | 350  | 920     | 1100 |
| 500  | 690  | 520  | 1850    | 2100 |
| 1000 | 820  | 640  | 2400    | 2850 |

---

## 🖥️ Consommation des Ressources

### Utilisation CPU (%)

| Charge | REST | SOAP | GraphQL | gRPC |
|------|------|------|---------|------|
| 10   | 8.5  | 10.2 | 12.8    | 6.9  |
| 100  | 14.3 | 18.5 | 21.4    | 12.1 |
| 500  | 24.6 | 29.8 | 35.7    | 19.3 |
| 1000 | 31.9 | 38.2 | 42.6    | 25.8 |

### Utilisation Mémoire (MB)

| Charge | REST | SOAP | GraphQL | gRPC |
|------|------|------|---------|------|
| 10   | 180  | 210  | 260     | 195  |
| 100  | 240  | 295  | 380     | 260  |
| 500  | 310  | 360  | 480     | 320  |
| 1000 | 390  | 460  | 610     | 410  |

---

## 🛠️ Évaluation de la Complexité de Développement

| Critère               | REST        | SOAP        | GraphQL     | gRPC        |
|----------------------|-------------|-------------|-------------|-------------|
| Temps de développement | Très court  | Long        | Moyen       | Moyen       |
| Volume de code        | Faible      | Élevé       | Moyen       | Moyen       |
| Courbe d’apprentissage| Facile      | Difficile   | Modérée     | Modérée     |
| Écosystème            | Très riche  | Riche       | Riche       | Modéré      |



## 📌 Synthèse Comparative

| Critère            | REST | SOAP | GraphQL | gRPC |
|-------------------|------|------|---------|------|
| Latence           | Moyenne | Élevée | Faible | Très faible |
| Throughput        | Moyen | Moyen | Très élevé | Élevé |
| Consommation CPU  | Moyenne | Moyenne | Élevée | Faible |
| Simplicité        | Très élevée | Faible | Moyenne | Moyenne |
| Sécurité          | Bonne | Très élevée | Bonne | Très élevée |

