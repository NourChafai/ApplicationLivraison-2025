# 📦 Projet : Application de Livraison - Modélisation Orientée Objet

Ce dépôt présente un résume sur les étapes complètes de la conception préliminaire

---

## ✅ Étape 1 : Raffinement du diagramme de classes

**Objectif** : Ajouter des contraintes au diagramme de classes pour le rendre plus précis et faciliter la programmation.

### 🔧 Actions effectuées :
- Ajout de **cardinalités précises** entre les classes.
- Ajout de **notes UML** exprimant des **règles métier** (ex. une commande ne peut être livrée sans livreur).
- Transformation de certaines classes en **enum** (ex. `OrderStatus`).
- Utilisation d’un héritage pour factoriser `Person` entre `Customer`, `User` et `DeliveryPerson`.
- Définition des contraintes de validité des objets (commande doit contenir au moins un item, etc.).



---

## ✅ Étape 2 : Diagramme de machine d'états

**Objectif** : Modéliser le **cycle de vie d’une commande (`Order`)** à travers ses différents états.

### 🔄 États modélisés :
- `EnAttente (PENDING)`
- `EnCours (PROCESSING)`
- `Livrée (DELIVERED)`
- `Annulée (CANCELLED)`

### 🔁 Transitions possibles :
- Paiement → EnAttente → EnCours
- Livraison → EnCours → Livrée
- Annulation → EnAttente/EnCours → Annulée



---

## ✅ Étape 3 : Deuxième raffinement

### 1. Traduction des **associations** en **attributs**
Toutes les associations du diagramme UML ont été traduites en attributs dans les classes Java (`Order`, `Restaurant`, `Gestionnaire`, etc.).

### 2. Traduction des **agrégations / compositions**
- **Composition** : ex. `Restaurant` possède son propre `Menu` créé dans le constructeur.
- **Agrégation** : ex. `Order` possède une liste d’`Item` fournie à la création.

### 3. Traduction des **diagrammes de séquence et machine d’états** en algorithmes

#### 🔸 Diagrammes de séquence
- **Passer une commande** : consulté → sélection → commande créée → enregistrée.
- **Mise à jour du statut par le livreur** : livreur sélectionne une commande et modifie son état.



📁 Voir : `delivery_app_java_classes.zip`
📁 Voir : `algorithme_diagramme_d'etat.txt`
📁 Voir : `algorithme_diagrammes_de_sequence.txt`

---




