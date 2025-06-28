# Blood Bank Management System

Un système de gestion de banque de sang développé avec **Spring Boot** pour le backend et **Angular 8** pour le frontend.

## 🩸 Objectif

Ce projet vise à gérer efficacement les donneurs de sang, les stocks de sang, les hôpitaux et les utilisateurs du système. Il comprend l'authentification avec Spring Security et JWT.

---

## 🛠️ Technologies Utilisées

### Backend :
- Java 11
- Spring Boot 2.5.0
- Spring Data JPA
- Spring Security
- MySQL
- JWT (JSON Web Tokens)
- Lombok
- H2 (base de données embarquée pour les tests)

### Frontend :
- Angular 8 (dans un dossier séparé, non inclus ici)

## 📁 Structure du projet

 src/
├── main/
│   ├── java/
│   │   └── com.application.bloodbankmanagement/
│   │       ├── controller/       # Gère les requêtes HTTP
│   │       ├── model/            # Contient les entités JPA (classes de base de données)
│   │       ├── repository/       # Interfaces JPA pour accéder aux données
│   │       ├── security/         # Configuration de la sécurité (JWT, filtres, etc.)
│   │       └── service/          # Logique métier
│   └── resources/
│       ├── application.properties # Configuration de l'application
│       └── static/                # Contenu statique (si utilisé)
└── test/                          # Tests unitaires et d’intégration



Interface d’inscription

![image](https://github.com/user-attachments/assets/877e5838-6bd5-4567-85e1-4e6b839430ed)

Interface d’authentification

![image](https://github.com/user-attachments/assets/0426e435-7bd6-4816-87ee-7cac8847628e)

Interface du Tableau de bord

![image](https://github.com/user-attachments/assets/6a71b458-ca8d-4a6f-8941-4bdf4ef64a10)

Interface Ajouter donateur

![image](https://github.com/user-attachments/assets/fa27d197-5e0e-4ba4-9f45-f621aa148754)

Interface Historique des demndes de sang

![image](https://github.com/user-attachments/assets/da928fb3-7cde-4812-854e-f8783ed08da1)

Pipeline DevOps et assurance qualité:

 Dans ce chapitre, nous abordons le pipeline DevOps mis en place pour assurer l'efficacité du développement, le déploiement automatisé, et l'assurance qualité de notre application de prise de rendez-vous médicaux et de téléconsultation. L'intégration de processus d'intégration continue (CI) et de déploiement continu (CD) garantit une livraison rapide et fiable des nouvelles versions de l'application. L'objectif est d'automatiser les différentes étapes du cycle de développement tout en maintenant une qualité de code élevée, une détection rapide des erreurs et un déploiement fluide. Ce chapitre détaille les différentes étapes de notre pipeline DevOps, les outils utilisés pour chaque phase, ainsi que les tests automatisés qui couvrent l'ensemble des fonctionnalités critiques de l'application.



![image](https://github.com/user-attachments/assets/9302fa92-15e1-4407-866d-7672f656c389)


 Nous avons mis en place une approche multi-niveaux pour couvrir tous les aspects critiques de l’application : • Tests Unitaires : Vérifient le bon fonctionnement des composants isolés • Tests d’Intégration : Valident les interactions entre les différents modules • Tests End-to-End (E2E) : Simulent le parcours utilisateur • Tests de Performance : S’assurent que l’application supporte la charge attendue


![image](https://github.com/user-attachments/assets/7bbbe83d-a56a-4f90-b68c-53eb399a4491)


Cette capture d’écran montre l’exécution réussie de notre pipeline CI suite aux commits
 Ajout du premier workflow GitHub Actions et Correction du fichier ci.yml sur la branche main.
 Le workflow, défini dans .github/workflows/ci.yml, a été déclenché et exécuté correctement à deux reprises. Chaque exécution a duré 11 secondes et porte le nom CI Pipeline, affiché dans la section All workflows.

Ce chapitre a détaillé le pipeline DevOps mis en place pour assurer une gestion efficace du cycle de développement, du déploiement et des tests de notre application de prise de rendez-vous médicaux et de téléconsultation. L'intégration continue (CI) et le déploiement continu (CD) sont des éléments essentiels pour garantir une mise en production rapide et fiable, tout en maintenant une qualité de code optimale. Les tests automatisés jouent un rôle clé en vérifiant la stabilité de l'application à chaque itération, assurant ainsi une expérience utilisateur fluide et sans erreur. Grâce à cette approche DevOps, nous avons renforcé la collaboration entre les équipes et accéléré la mise sur le marché de notre solution tout en garantissant sa qualité.




## ⚙️ Configuration du Backend

### Fichier `application.properties` :
```properties
server.port=8080

spring.datasource.url=jdbc:mysql://localhost:3306/bloodbanksystem
spring.datasource.username=root
spring.datasource.password=Gowthamraj@258

spring.jpa.show-sql=true
spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL55Dialect







