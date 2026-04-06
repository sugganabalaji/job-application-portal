# Job Application Portal

A Spring Boot MVC application for managing job applications.  
Built with **Spring Boot**, **Spring MVC**, **JSP**, **Lombok**, and **Maven**.

---

## 🚀 Features
- Candidates can check Jobs posted in portal
- Job posting and listing
- Secure form validation and error handling

---

## 🛠️ Tech Stack
- **Backend**: Spring Boot, Spring MVC
- **Frontend**: JSP, Bootstrap
- **ORM/DB**: Store in to ArrayList
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
     │   │── resources/ 
     │   │   ├── static/       # css files 
     │   │   └── application.yaml
     │   └──webapp/    
     │       └── views/        # JSP views
     └── test/                 # Unit & integration tests
```

---

## ⚙️ Setup Instructions
1. **Clone the repo**
```bash
   git clone https://github.com/sugganabalaji/job-application-portal.git
   cd job-application-portal
```
2. **Configure prefix and suffix**
   - Update ```application.yaml```:
   
```properties
    spring:
        mvc:
            view:
                prefix: /views/
                suffix: .jsp
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
    @Data
    @NoArgsConstructor
    @AllArgsConstructor
    @Component
   public class JobPost {
   
      private int postId;
      private String postProfile;
      private String postDesc;
      private Integer reqExperience;
      private List<String> postTechStack;
   
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
```