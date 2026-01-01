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




## 📏 Métriques d’Évaluation

### Performances

- Latence moyenne
- Percentiles (p95, p99)
- Débit (requêtes/seconde)

### Ressources

- Utilisation CPU
- Consommation mémoire

### Simplicité d’Implémentation

- Temps de développement
- Nombre de lignes de code
- Courbe d’apprentissage

### Sécurité

- Support TLS / SSL
- Authentification (OAuth2, JWT)
- Résistance aux attaques

---

## 📊 Résultats

Les résultats sont présentés sous forme de tableaux comparatifs :

- Temps de réponse (latence)
- Débit (throughput)
- Consommation CPU et mémoire
- Facilité d’implémentation
- Sécurité

Ces tableaux permettent une **analyse comparative claire** entre REST, SOAP, GraphQL et gRPC.


