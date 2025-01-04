# ORM JPA Hibernate Spring Data  

Projet réalisé par Firdawsse Ahchouche

 **Introduction** 
Ce projet a pour objectif de développer une application de gestion des utilisateurs et des rôles.  
L'application repose sur Spring Boot, Spring Data JPA, et Hibernate pour assurer la gestion des relations entre entités et des opérations CRUD.  
Les principales fonctionnalités incluent :  
- Ajouter des utilisateurs et des rôles.  
- Assigner des rôles à des utilisateurs.  
- Consulter et modifier les utilisateurs ainsi que leurs rôles respectifs.  


 Fonctionnalités  
1. **Ajout et gestion des utilisateurs** : Créer, consulter, et modifier des utilisateurs.  
2. **Ajout et gestion des rôles** : Ajouter de nouveaux rôles et les attribuer aux utilisateurs.  
3. **Gestion des relations utilisateurs-rôles** : Implémentation d'une relation **@ManyToMany**.  


## Structure du Projet  
L'architecture du projet est organisée en plusieurs packages modulaires :  
![image](https://github.com/user-attachments/assets/9a000095-6732-43a7-9f79-ac686b8e8407)


### 1. **Package entities**  
- Contient les entités `User` et `Role`, qui représentent les tables dans la base de données.  
- Relation entre les entités :  
  - `User` ↔ `Role` : Relation **@ManyToMany**.  

### 2. **Package repositories**  
- Inclut les interfaces `UserRepository` et `RoleRepository`, qui héritent de `JpaRepository`.  
- Fournit des méthodes pour effectuer les opérations CRUD de manière automatique.  

### 3. **Package `service`**  
- Contient les services de l'application et leur implémentation :  
  - **`UserService`** : Interface définissant les méthodes métier pour gérer les utilisateurs.  
  - **`UserServiceImpl`** : Implémentation de l'interface `UserService`.  

### 4. **Fichier `application.properties`**  
- Contient les configurations essentielles du projet, notamment la configuration de la base de données.  


## Configuration  

### 1. **Base de Données**  
L'application utilise une base de données H2 en mémoire pour un déploiement simple et rapide.  

Conclusion
Ce projet illustre les concepts clés de Spring Boot, Spring Data JPA, et Hibernate pour construire une application performante et modulaire.
Il peut facilement être étendu pour inclure des fonctionnalités supplémentaires telles que :
-L'authentification.
-La gestion avancée des autorisations.
