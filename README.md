📚 README - Student Management API
---
📋 Description du projet
---
API RESTful pour la gestion des étudiants développée avec Spring Boot. Cette application permet d'effectuer des opérations CRUD sur des étudiants avec une base de données MySQL.
---
🛠️ Technologies utilisées
---
Java 17

Spring Boot

Spring Data JPA

MySQL

Maven

Swagger (springdoc-openapi)
---
3. Configuration de l'application
---
Dans src/main/resources/application.properties :
---
properties
spring.datasource.url=jdbc:mysql://localhost:3306/student_db?serverTimezone=UTC
spring.datasource.username=root
spring.datasource.password=votre_mot_de_passe
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
server.port=0
---
4. Lancer l'application
   ---
bash
# Avec Maven wrapper
./mvnw spring-boot:run

# Ou avec Maven installé
mvn spring-boot:run
L'application démarrera sur http://localhost:61367 
---
📡 Endpoints de l'API
---
Méthode	Endpoint
---
Description
---
POST	/students/save	Ajouter un nouvel étudiant
---
GET	/students/all	Récupérer tous les étudiants
---
GET	/students/count	Compter le nombre total d'étudiants
---
GET	/students/byYear	Statistiques par année de naissance
---
DELETE	/students/delete/{id}	Supprimer un étudiant par ID
---
📸 Tests avec Postman
---
1 : Ajouter un étudiant (POST)
URL : http://localhost:61367/students/save

Méthode : POST

Headers : Content-Type: application/json

Body :

json
{
    "nom": "LACHGAR",
    "prenom": "Mohamed",
    "dateNaissance": "1985-09-01"
}
---
📷 Capture d'écran :
<img width="1920" height="1080" alt="Screenshot (799)" src="https://github.com/user-attachments/assets/19bdba74-cffe-4374-8ef7-45f693cc6cb4" />
---
2. Test de la récupération de tous les étudiants (GET)

📷 Capture d'écran : 
<img width="1920" height="1080" alt="Screenshot (801)" src="https://github.com/user-attachments/assets/fa5643c1-1b8b-4495-9d92-9881e6e3aa25" />
---
 3 : Récupérer tous les étudiants (GET)
 ---
URL : http://localhost:61367/students/all

---
📷 Capture d'écran :
<img width="1920" height="1080" alt="Screenshot (802)" src="https://github.com/user-attachments/assets/0ab44072-f698-4e5d-bd1c-a5d91f91f7dd" />



4 : Statistiques par année (GET)
URL : http://localhost:61367/students/byYear
---
📷 Capture d'écran :
<img width="1920" height="1080" alt="Screenshot (803)" src="https://github.com/user-attachments/assets/cb8571bd-09e2-4650-a1b7-6825ba734a06" />

Test 6 : Supprimer un étudiant (DELETE)
URL : http://localhost:61367/students/delete/1

📷 Capture d'écran : 
<img width="1920" height="1080" alt="Screenshot (804)" src="https://github.com/user-attachments/assets/688ab165-c6ab-4281-ac1d-7be8be988e82" />
---

📊 Tests unitaires
---
Exécuter les tests :



<img width="1920" height="1080" alt="Screenshot (798)" src="https://github.com/user-attachments/assets/473fdceb-4d61-423f-9aef-3ec0719efbbf" />


📖 Documentation Swagger
Une fois l'application lancée, accédez à :
--
http://localhost:61367/
--
<img width="1920" height="956" alt="Screenshot (805)" src="https://github.com/user-attachments/assets/5bd91513-91a2-43bb-ae35-f4ce8f730a69" />


👨‍💻 Auteur
AIT LECHGUEUR basma
