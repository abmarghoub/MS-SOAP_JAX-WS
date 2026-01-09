# TP : Service Web SOAP avec Spring Boot et Apache CXF

---

## 1. Objectif du TP

* Intégrer Apache CXF pour exposer des services SOAP
* Utiliser JPA pour la persistance des données
* Tester un service SOAP à l’aide de SoapUI
* Comprendre le rôle du WSDL dans les services web SOAP

---

## 2. Architecture du TP

### 2.1 Stack technologique

| Technologie     | Rôle                                                       |
| --------------- | ---------------------------------------------------------- |
| Java 21         | Langage de programmation principal                         |
| Spring Boot 4   | Framework pour le développement rapide d’applications Java |
| Apache CXF 4    | Publication et gestion des services web SOAP               |
| JPA / Hibernate | Mapping objet–relationnel et accès aux données             |
| H2 Database     | Base de données en mémoire pour le développement           |
| Maven           | Gestion des dépendances et du cycle de vie du projet       |
| SoapUI          | Test et validation des services web SOAP                   |
| Lombok          | Réduction du code boilerplate                              |

---

### 2.2 Structure du projet

La structure du projet respecte l’architecture standard de Spring Boot :

<img width="420" height="725" alt="image" src="https://github.com/user-attachments/assets/000fc6b3-3a3c-4b9e-a583-13e4abf7ab6a" />


Chaque couche du projet a un rôle bien défini :

* **entities** : contient les entités JPA
* **repositories** : accès aux données
* **ws** : services web SOAP
* **config** : configuration Apache CXF

---

## 3. Résultats attendus

Après le lancement de l’application, les résultats suivants sont attendus :

### 3.1 Démarrage de l’application

* Le serveur Spring Boot démarre sans erreur

<img width="894" height="577" alt="image" src="https://github.com/user-attachments/assets/ecf0f4db-3d91-4ab6-8866-1a6320e5928a" />

* La base H2 est initialisée automatiquement
  
<img width="727" height="655" alt="image" src="https://github.com/user-attachments/assets/fe0ebe97-fa38-4e8a-a74a-bb098589a898" />
<img width="823" height="522" alt="image" src="https://github.com/user-attachments/assets/ec4cb8ae-f4d1-456e-baf3-b91beaa0b5a2" />

* Le service SOAP est publié via Apache CXF



---

### 3.2 Accès au WSDL

Le WSDL du service SOAP est accessible via l’URL suivante :

```
http://localhost:8085/services/ws?wsdl
```

<img width="321" height="143" alt="image" src="https://github.com/user-attachments/assets/1279f14e-7a32-4581-aa0b-57db72ad60ac" />

---

### 3.3 Tests avec SoapUI

À l’aide de SoapUI, les opérations suivantes sont testées avec succès :

* `createCompte`

<img width="1454" height="699" alt="image" src="https://github.com/user-attachments/assets/8ab6d70c-7d9b-46ef-89c4-2426f9ec31dd" />

* `getCompteById`

<img width="1358" height="553" alt="image" src="https://github.com/user-attachments/assets/c76cbb25-5768-4143-bf0b-9826609c64cf" />

* `getComptes`

<img width="1427" height="679" alt="image" src="https://github.com/user-attachments/assets/b750216b-289b-4826-a399-21a35168e6a8" />

* `deleteCompte`

<img width="1333" height="472" alt="image" src="https://github.com/user-attachments/assets/7a053031-79e1-464d-9845-95c70a431694" />

---

## Auteur:

**Réalisé par :** Abla MARGHOUB <br>
**Encadré par :** Pr. Mohamed LACHGAR <br>
**Module :** Techniques de Programmation Avancée<br>
**Cours :** Architecture Microservices : Conception, Déploiement et Orchestration<br>
**Établissement :** École Normale Supérieure - Université Cadi Ayyad<br>
