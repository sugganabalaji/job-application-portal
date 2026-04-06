# Job Application Portal

A Spring Boot MVC application for managing job applications.  
Built with **Spring Boot**, **Spring MVC**, **Thymeleaf**, **Lombok**, and **Maven**.

---

## 🚀 Features
- Candidate registration and profile management
- Job posting and listing
- Application submission and tracking
- Admin dashboard for managing jobs and applicants
- Secure form validation and error handling

---

## 🛠️ Tech Stack
- **Backend**: Spring Boot, Spring MVC
- **Frontend**: Thymeleaf templates, Bootstrap
- **ORM/DB**: JPA/Hibernate, PostgreSQL/MySQL
- **Utilities**: Lombok for boilerplate reduction
- **Build Tool**: Maven

---

## 📂 Project Structure

```
src/ ├── main/ 
     │   ├── java/com/example/jobapp 
     │   │   ├── controller/   # MVC Controllers 
     │   │   ├── service/      # Business logic 
     │   │   ├── repository/   # JPA Repositories 
     │   │   ├── model/        # Entities with Lombok 
     │   │   └── config/       # App configuration 
     │   └── resources/ │       
     ├── templates/    # Thymeleaf views 
     │       └── application.properties 
     └── test/                 # Unit & integration tests
```

---

## ⚙️ Setup Instructions
1. **Clone the repo**
```bash
   git clone https://github.com/sugganabalaji/job-application-portal.git
   cd job-application-portal
```
2. **Configure Database**
   - Update ```application.properties``` with your DB credentials:
   
```properties
     spring.datasource.url=jdbc:postgresql://localhost:5432/jobapp
     spring.datasource.username=postgres
     spring.datasource.password=root
     spring.jpa.hibernate.ddl-auto=update
```

3. **Run & Build**
```bash
   mvn clean install
   mvn spring-boot:run
```
4. **Access the Application**
- Open your browser and navigate to [http://localhost:8080](http://localhost:8080)

**🧑‍💻 Lombok Usage**

Lombok is used throughout the project to reduce boilerplate code. Annotations like `@Data`, `@Entity`, `@Service`, and `@Controller` are extensively used to streamline entity classes, service classes, and controller classes respectively. This approach enhances readability and maintainability by eliminating redundant getter/setter methods, constructors, and boilerplate annotations.
- `@Data` for getters/setters
- `@Builder` for Object creation with builder pattern
- `@NoArgsConstuctor` and `@AllArgsConstrutor` for Constructor
- `@Entity`+ Lambok annotations for clean models

Example:
 ```java
    @Entity
    @Data
    @NoArgsConstructor
    @AllArgsConstructor
    @Builder
    public class Candidate {
        @Id
        @GeneratedValue(strategy = GenerationType.IDENTITY)
        private Long id;
        private String fullName;
        private String email;
        private String resumeLink;
    }
```

For more information on Lombok,
- [Lombok GitHub](https://github.com/rzwitserloot/lombok)
- [Lombok Documentation](https://projectlombok.org/features/all)
  
**✅ Future Enhancements**

- Role-based authentication (Spring Security)
- File upload for resumes
- REST API endpoints for external integration
- Dockerization for deployment

**📄 License**

This project is licensed under the MIT License.


---

```
This README is structured to impress recruiters: clear tech stack, setup steps, and clean code samples.

Would you like me to also draft a **short GitHub repo description** (the one‑liner that appears under the repo title) so it’s recruiter‑ready?
```