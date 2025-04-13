# 📦 Projet : Gestion de Livraison de Repas

## 👥 Auteurs :
- Yosser Jouini  
- Nour Chafai  
- Melek Amri  
- Ferid Haffani  

---

## 🧠 1. Identification des classes "métier"

| Classe         | Rôle métier                                                                 |
|----------------|------------------------------------------------------------------------------|
| `User`         | Super-classe pour les différents types d’utilisateurs                       |
| `Customer`     | Spécialisation de `User` qui passe des commandes                            |
| `DeliveryPerson`| Spécialisation de `User` qui livre les commandes                          |
| `Gestionnaire` | Gère les utilisateurs, les menus et les véhicules                           |
| `Restaurant`   | Point central du système, propose des menus et prépare les commandes        |
| `Menu`         | Regroupe les `Item` proposés                                                |
| `Item`         | Produit individuel avec nom, prix                                           |
| `Order`        | Commande passée par un client                                               |
| `OrderStatus`  | Enumération : En attente, En cours, Livrée…                                 |
| `Vehicle`      | Utilisé par un livreur pour les livraisons                                  |
| `Adress`       | Adresse associée à un `Customer` ou à un `Restaurant`                       |

---

## 🧬 2. Diagramme de classes



---

## 🔄 3. Diagrammes de séquence (Sprint 1)

### 🎯 UC1 – Passer une commande

**Acteur** : Client  
**Classe principale** : `Customer`  

#### Objets/Instances :
- Client (acteur humain)  
- Customer (objet métier représentant le client)  
- Menu (propose les items)  
- Order (commande créée)  
- Restaurant (reçoit la commande)

#### 🔁 Séquence :
1. Le Client consulte le menu.
2. Customer interroge le Menu → Affiche les items.
3. Le Client sélectionne les items.
4. Customer crée une commande `Order` avec les items.
5. Le statut de la commande est mis à `"En attente"`.
6. La commande est envoyée au `Restaurant`.
7. Le Client reçoit une confirmation.



---

### 🎯 UC2 – Mettre à jour le statut d'une commande

**Acteur** : Livreur  
**Classe principale** : `DeliveryPerson`

#### Objets/Instances :
- Livreur (acteur humain)  
- DeliveryPerson (objet métier représentant le livreur)  
- Order (commande à livrer)  
- Client (recevra une notification)

#### 🔁 Séquence :
1. Le Livreur consulte ses commandes via `DeliveryPerson`.
2. Il reçoit la liste de commandes.
3. Il choisit une commande → demande une mise à jour du statut.
4. `DeliveryPerson` modifie l’attribut `status` de `Order`.
5. `Order` notifie le Client.
6. Le Livreur reçoit une confirmation.



---

## 📂 Structure du dépôt recommandée

