*Members see only projects where they have assigned tasks

### Dashboard
- Stats: Total projects, tasks by status, overdue count
- Overdue task list with red highlighting
- Admin: Recent activity across all tasks
- Member: Personal task list with quick status update

### Projects
- Create, edit, delete projects
- Status: Active / On Hold / Completed
- Per-project task counts and overdue alerts

### Tasks
- Create tasks inside projects
- Assign to any team member
- Priority: Low / Medium / High
- Status: Todo / In Progress / Done
- Due date with overdue detection
- Inline status update dropdown

### Team Management (Admin)
- View all registered users
- Promote/demote roles (Admin ↔ Member)

---

## 🗂️ Project Structure

```
taskmanager/
├── src/main/java/com/taskmanager/
│   ├── TaskManagerApplication.java
│   ├── DataInitializer.java
│   ├── config/
│   │   └── SecurityConfig.java
│   ├── controller/
│   │   ├── AuthController.java
│   │   ├── DashboardController.java
│   │   ├── ProjectController.java
│   │   ├── TaskController.java
│   │   └── UserController.java
│   ├── model/
│   │   ├── User.java
│   │   ├── Project.java
│   │   ├── Task.java
│   │   ├── Role.java
│   │   ├── TaskStatus.java
│   │   ├── Priority.java
│   │   └── ProjectStatus.java
│   ├── repository/
│   │   ├── UserRepository.java
│   │   ├── ProjectRepository.java
│   │   └── TaskRepository.java
│   └── service/
│       ├── UserService.java
│       ├── UserDetailsServiceImpl.java
│       ├── ProjectService.java
│       └── TaskService.java
└── src/main/resources/
    ├── application.properties       ← Local H2
    ├── application-prod.properties  ← Railway MySQL
    └── templates/
        ├── login.html
        ├── register.html
        ├── dashboard.html
        ├── fragments/layout.html
        ├── projects/
        │   ├── list.html
        │   ├── form.html
        │   └── detail.html
        ├── tasks/edit.html
        └── users/list.html
```

---

## 🛠 Tech Stack

- **Backend**: Java 17, Spring Boot 3.2, Spring Security, Spring Data JPA
- **Frontend**: Thymeleaf, plain HTML/CSS (no external CSS framework)
- **Database**: H2 (local dev) / MySQL (production)
- **Build**: Maven
- **Deployment**: Railway
