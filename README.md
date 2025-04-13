# 📦 Projet : Gestion de Livraison de Repas

## 👥 Auteurs :
- Yosser Jouini  
- Nour Chafai  
- Melek Amri  
- Ferid Haffani  

📅 Date : 07/04/2025

---



## 🚀 1. Cas d'utilisation prioritaires (Sprint 1)

| N° | Cas d’utilisation                        | Acteur   | Priorité |
|----|------------------------------------------|----------|----------|
| 1  | Passer une commande                      | Client   | Haute    |
| 2  | Mettre à jour le statut d’une commande   | Livreur  | Haute    |

---

## ✅ 2. Spécifications détaillées

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
