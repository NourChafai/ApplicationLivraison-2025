# 📦 Projet : Gestion de Livraison de Repas

## 👥 Auteurs :
- Yosser Jouini  
- Nour Chafai  
- Melek Amri  
- Ferid Haffani  

📅 Date : 07/04/2025

---

## 🧾 1. Introduction

Ce projet simule une plateforme de gestion de commandes pour un restaurant, incluant les interactions entre **clients**, **livreurs**, **gestionnaires**, et le **système de livraison**.

L’objectif est de permettre la gestion :
- des **utilisateurs** (création, connexion),
- des **commandes** (création, suivi),
- des **livraisons** (véhicule, statut),
- et des **menus/items** proposés par le restaurant.

---

## 📋 2. Spécifications du projet

### 🔧 Notions de base & contraintes
- **Commandes** : composées d’un ou plusieurs items.
- **Utilisateurs** : clients, livreurs, gestionnaires.
- **Livraison** : nécessite une adresse et un véhicule associé.
- **Statut de commande** : en attente → en préparation → en livraison → livrée.
- **Menu** : liste des items proposés par le restaurant.

---

## 🎭 3. Acteurs et fonctionnalités

### 👤 Client
- Créer un compte et se connecter  
- Parcourir le menu  
- Passer une commande  
- Suivre le statut de sa commande  

### 🚚 Livreur
- Se connecter  
- Voir les commandes assignées  
- Mettre à jour le statut des commandes  
- Voir son véhicule assigné  

### 🧑‍💼 Gestionnaire
- Se connecter  
- Ajouter/modifier des items du menu  
- Gérer les utilisateurs  
- Gérer les véhicules  

---

## 🚀 4. Cas d'utilisation prioritaires (Sprint 1)

| N° | Cas d’utilisation                        | Acteur   | Priorité |
|----|------------------------------------------|----------|----------|
| 1  | Passer une commande                      | Client   | Haute    |
| 2  | Mettre à jour le statut d’une commande   | Livreur  | Haute    |

---

## ✅ 5. Spécifications détaillées

### 📌 Cas d'utilisation 1 : Passer une commande

- **Acteur principal** : Client  
- **Préconditions** :
  - Le client est connecté  
  - Le menu du restaurant est visible  
- **Postconditions** :
  - Une commande est créée avec les items choisis  
  - Le statut de la commande est `"En attente"`

#### 🧪 Table de décision — Passer une commande

| Cas | Connexion valide | Menu visible | Items sélectionnés | Résultat attendu     |
|-----|------------------|--------------|---------------------|----------------------|
| 1   | ✅               | ✅           | ✅                  | ✅ Commande créée     |
| 2   | ❌               | ✅           | ✅                  | ❌ Erreur             |
| 3   | ✅               | ❌           | ✅                  | ❌ Erreur             |
| 4   | ✅               | ✅           | ❌                  | ❌ Erreur             |

---

### 📌 Cas d'utilisation 2 : Mettre à jour le statut d'une commande

- **Acteur principal** : Livreur  
- **Préconditions** :
  - Le livreur est connecté  
  - Il a une commande assignée  
- **Postconditions** :
  - Le statut de la commande est mis à jour : `"En livraison"` ou `"Livrée"`

#### 🧪 Table de décision — Mettre à jour le statut

| Cas | Connexion valide | Commande assignée | Statut sélectionné | Résultat attendu       |
|-----|------------------|-------------------|---------------------|------------------------|
| 1   | ✅               | ✅                | En livraison        | ✅ Statut mis à jour    |
| 2   | ❌               | ✅                | En livraison        | ❌ Erreur               |
| 3   | ✅               | ❌                | Livrée              | ❌ Erreur               |
| 4   | ✅               | ✅                | Invalide            | ❌ Erreur               |

---

## 📂 6. Organisation du projet Git

```
NomProjet/
├── Diagrammes/
│   ├── cas_utilisation.pu
│   ├── cas_utilisation.png
├── src/
│   ├── Main.java
│   ├── Commande.java
│   ├── ...
├── README.md
```

---

## 🔧 À faire pour le prochain Sprint :
- Ajouter les cas d’utilisation secondaires
- Intégrer les tests unitaires
- Implémenter les modules en Java
