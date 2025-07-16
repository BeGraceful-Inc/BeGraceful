`<img src="/logo.png" alt="logo" width="40" style="vertical-align: middle;"/>`


# BeGraceful - Calorie Diary App
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
  npm install my-project
  cd my-project
```

    
## 🖼️ Screenshots & GIFs

#### Screenshots
![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)

#### GIFs
![Demo GIF](assets/gifs/meal_addition.gif)


## 🔗 API Documentation

#### Get all items

```http
  GET /api/items
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `api_key` | `string` | **Required**. Your API key |

#### Get item

```http
  GET /api/items/${id}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of item to fetch |

#### add(num1, num2)


## 🏗️ Architecture & Diagrams
## Authors

- [@octokatherine](https://www.github.com/octokatherine)

## Implementation checklist

### Technical requirements (20 points)
#### Backend development (8 points)
- [ ] Go-based microservices architecture (minimum 3 services) (3 points)
- [ ] RESTful API with Swagger documentation (1 point)
- [ ] gRPC implementation for communication between microservices (1 point)
- [ ] PostgreSQL database with proper schema design (1 point)
- [ ] JWT-based authentication and authorization (1 point)
- [ ] Comprehensive unit and integration tests (1 point)

#### Frontend development (8 points)
- [ ] Flutter-based cross-platform application (mobile + web) (3 points)
- [ ] Responsive UI design with custom widgets (1 point)
- [ ] State management implementation (1 point)
- [ ] Offline data persistence (1 point)
- [ ] Unit and widget tests (1 point)
- [ ] Support light and dark mode (1 point)

#### DevOps & deployment (4 points)
- [ ] Docker compose for all services (1 point)
- [ ] CI/CD pipeline implementation (1 point)
- [ ] Environment configuration management using config files (1 point)
- [ ] GitHub pages for the project (1 point)

### Non-Technical Requirements (10 points)
#### Project management (4 points)
- [ ] GitHub organization with well-maintained repository (1 point)
- [ ] Regular commits and meaningful pull requests from all team members (1 point)
- [ ] Project board (GitHub Projects) with task tracking (1 point)
- [ ] Team member roles and responsibilities documentation (1 point)

#### Documentation (4 points)
- [ ] Project overview and setup instructions (1 point)
- [ ] Screenshots and GIFs of key features (1 point)
- [ ] API documentation (1 point)
- [ ] Architecture diagrams and explanations (1 point)

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
