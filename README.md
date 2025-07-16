# <img src="docs/assets/clever-icon.png" alt="logo" width="40" style="vertical-align: middle;"/> BeGraceful - Calorie Diary App
BeGraceful - an application for monitoring nutrition and activity. Users can track calories, steps, workouts


### 📖 Features
- Accounting for food consumed
- Tracking activity and steps
- Personalized Goals
- Light/dark mode toggle
- Cross platform


## 🚀 Setup Instructions
Install my-project with npm

```bash
  #
```

    
## 🖼️ Screenshots & GIFs
#### Screenshots
![Start page](docs/screenshots/start-page.jpg)
![Registration page](docs/screenshots/registration-page.jpg)
![Personal info page](docs/screenshots/personal-info-page.jpg)
![Log in page](docs/screenshots/log-in-page.jpg)
![Home page](docs/screenshots/home-page.jpg)
![Profile page](docs/screenshots/profile-page.jpg)

#### GIFs
![Registration](docs/gifs/registration.gif)
![Log out - Log in](docs/gifs/logOut-logIn.gif)
![Add meal](docs/gifs/add-meal.gif)
![Add activity](docs/gifs/add-activity.gif)
![Update weight](docs/gifs/update-weight.gif)


## 🔗 API Documentation `template`

#### Get all items

```http
  GET /api/items
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `api_key` | `string` | **Required**. Your API key |

#### add(num1, num2)


## 🏗️ Architecture & Diagrams
### 1. System Overview  
![System Overview](docs/diagrams/high-level-system.png)

![System Component Diagram](docs/diagrams/system-component.png)

### 2. Database Schema  
![ER Diagram](docs/diagrams/database-entity-relationship.png)

### 3. Frontend Architecture  
![Frontend](docs/diagrams/frontend-architecture.png)



## Authors
- [@Retr0-46](https://github.com/Retr0-46) - backend
- [@kas-whr](https://github.com/kas-whr) - frontend
- [@1r444444](https://github.com/1r444444) - UI/UX design + frontend
- [@DariaKomzolova](https://github.com/DariaKomzolova) - frontend
- [@]() - backend

## Implementation checklist

### Technical requirements (20 points)
#### Backend development (8 points)
- [ ] Go-based microservices architecture (minimum 3 services) (3 points)
- [ ] RESTful API with Swagger documentation (1 point)
- [ ] gRPC implementation for communication between microservices (1 point)
- [ ] PostgreSQL database with proper schema design (1 point)
- [x] JWT-based authentication and authorization (1 point)
- [ ] Comprehensive unit and integration tests (1 point)

#### Frontend development (8 points)
- [x] Flutter-based cross-platform application (mobile + web) (3 points)
- [x] Responsive UI design with custom [widgets](https://github.com/BeGraceful-Inc/BeGraceful/tree/dev2/frontend/lib/src/ui/widgets) (1 point)
- [x] State management implementation (1 point)
- [ ] Offline data persistence (1 point)
- [ ] Unit and widget [tests](https://github.com/BeGraceful-Inc/BeGraceful/tree/dev2/frontend/test) (1 point)
- [x] Support light and dark mode (1 point)

#### DevOps & deployment (4 points)
- [ ] Docker compose for all services (1 point) [front](), [back](https://github.com/BeGraceful-Inc/BeGraceful/blob/dev2/backend/docker-compose.yml)
- [ ] CI/CD pipeline implementation (1 point)
- [ ] Environment configuration management using config files (1 point)
- [ ] GitHub pages for the project (1 point)

### Non-Technical Requirements (10 points)
#### Project management (4 points)
- [x] GitHub organization with well-maintained repository (1 point)
- [ ] Regular commits and meaningful pull requests from all team members (1 point)
- [x] [Project board](https://github.com/orgs/BeGraceful-Inc/projects/1) (GitHub Projects) with task tracking (1 point)
- [x] Team member roles and responsibilities documentation (1 point)

#### Documentation (4 points)
- [ ] Project overview and setup instructions (1 point)
- [x] [Screenshots]() and [GIFs]() of key features (1 point)
- [ ] API documentation (1 point)
- [x] [Architecture diagrams]() and explanations (1 point)

#### Code quality (2 points)
- [ ] Consistent code style and formatting during CI/CD pipeline (1 point)
- [ ] Code review participation and resolution (1 point)

### Bonus Features (up to 10 points)
- [ ] Localization for Russian (RU) and English (ENG) languages (2 points)
- [ ] Good UI/UX design (up to 3 points)
- [ ] Integration with external APIs (fitness trackers, health devices) (up to 5 points)
- [ ] Comprehensive error handling and user feedback (up to 2 points)
- [ ] Advanced animations and transitions (up to 3 points)
- [ ] Widget implementation for native mobile elements (up to 2 points)

Total points implemented: XX/30 (excluding bonus points)

`Note: For each implemented feature, provide a brief description or link to the relevant implementation below the checklist.`
