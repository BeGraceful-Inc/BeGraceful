# <img src="docs/assets/clever-icon.png" alt="logo" width="40" style="vertical-align: middle;"/> BeGraceful - Calorie Diary App
BeGraceful - an application for monitoring nutrition and activity. Users can track calories, steps, workouts

### 📖 Features
- Accounting for food consumed
- Tracking activity and steps
- Personalized Goals
- Light/dark mode toggle
- Cross platform

## 🚀 Quick Start

### Prerequisites
- Flutter SDK (for frontend)
- Go (for backend)
- Docker & Docker Compose (optional)
- PostgreSQL (for backend)

### Running the Application

#### Option1: Using Docker Compose
```bash
# Clone the repository
git clone https://github.com/BeGraceful-Inc/BeGraceful.git
cd BeGraceful

# Start all services (backend + frontend)
docker-compose up --build
```

Frontend will be available at: http://localhost:8080  
Backend services:
- Auth Service: http://localhost:8001
- Profile Service: http://localhost:8002  
- Calories Service: http://localhost:803
#### Option 2: Local Development
```bash
# Backend
cd backend
docker-compose up -d  # Start PostgreSQL
cd auth_service && go run ./cmd/auth/main.go
cd ../profile_service && go run ./cmd/profile/main.go  
cd ../calories_service && go run ./cmd/calories/main.go

# Frontend
cd frontend
flutter run -d chrome  # For web
# or
flutter run -d emulator-5554 For Android
```

## 🏗️ Backend Architecture

### Microservices Overview
BeGraceful backend is built using a **microservices architecture** with three independent Go services:

####1. **Auth Service** (`auth_service`)
- **Port**: 81 **Purpose**: User authentication and authorization
- **Key Features**:
  - User registration and login
  - JWT token generation and validation
  - Password hashing and security
- **API Endpoints**:
  - `POST /api/v1h/register` - User registration
  - `POST /api/v1/auth/login` - User login
  - `POST /api/v1/validate` - Token validation

#### 2. **Profile Service** (`profile_service`)
- **Port**: 82 **Purpose**: User profile management
- **Key Features**:
  - Personal information storage (name, age, height, weight)
  - Activity level and fitness goals
  - Weight tracking and updates
- **API Endpoints**:
  - `GET /api/v1/profiles/{user_id}` - Get user profile
  - `PUT /api/v1/profiles/{user_id}` - Update profile
  - `PATCH /api/v1/profiles/{user_id}/weight` - Update current weight

#### 3. **Calories Service** (`calories_service`)
- **Port**: 83 **Purpose**: Nutrition and activity tracking
- **Key Features**:
  - Food intake logging with nutritional information
  - Workout and activity tracking
  - Daily calorie and macro summaries
  - Step counting integration
- **API Endpoints**:
  - `POST /api/v1lories/food` - Log food intake
  - `POST /api/v1/calories/workout` - Log workout
  - `GET /api/v1/calories/summary` - Get daily summary
  - `POST /api/v1/calories/steps` - Update step count

### Service Communication
- **Inter-service communication**: HTTP REST APIs
- **Authentication**: JWT tokens passed in Authorization headers
- **Database**: Each service has its own PostgreSQL schema
- **API Documentation**: Swagger/OpenAPI specs for each service

### Data Flow Example
1. **User Registration**:
   ```
   Frontend → Auth Service → Database
   ```
2. **Profile Update**:
   ```
   Frontend → Profile Service → Database
   ```
   3. **Food Logging**:
   ```
   Frontend → Calories Service → Database
   ```

### Database Schema
Each service maintains its own database tables:
- **Auth Service**: `users` table
- **Profile Service**: `profiles` table  
- **Calories Service**: `food_entries`, `workout_entries`, `step_entries` tables

### Security
- JWT-based authentication across all services
- Password hashing using bcrypt
- Input validation and sanitization
- CORS configuration for web frontend

### Deployment
- **Development**: Docker Compose for local development
- **Production**: Each service can be deployed independently
- **Scaling**: Services can be scaled horizontally based on load

## 🖼️ Screenshots & GIFs
#### Screenshots
-Start page](docs/screenshots/start-page.jpg)
- [Registration page](docs/screenshots/registration-page.jpg)
- [Personal info page](docs/screenshots/personal-info-page.jpg)
- [Log in page](docs/screenshots/log-in-page.jpg)
- [Home page](docs/screenshots/home-page.jpg)
- [Profile page](docs/screenshots/profile-page.jpg)

#### GIFs
- [Registration](docs/gifs/registration.gif)
-Log out - Log in](docs/gifs/logOut-logIn.gif)
- [Add meal](docs/gifs/add-meal.gif)
- [Add activity](docs/gifs/add-activity.gif)
- [Update weight](docs/gifs/update-weight.gif)

## 🔗 API Documentation

### Authentication Endpoints
```http
POST /api/v1/auth/register
POST /api/v1uth/login
```

### Profile Endpoints  
```http
GET /api/v1/profiles/{user_id}
PUT /api/v1/profiles/{user_id}
PATCH /api/v1/profiles/{user_id}/weight
```

### Calories Endpoints
```http
POST /api/v1/calories/food
POST /api/v1/calories/workout
GET /api/v1/calories/summary
POST /api/v1/calories/steps
```

Full API documentation available in Swagger format for each service.

## 🏗️ Architecture & Diagrams
### 1System Overview  
- [System Overview](docs/diagrams/high-level-system.png)
- [System Component Diagram](docs/diagrams/system-component.png)

### 2Database Schema  
- [ER Diagram](docs/diagrams/database-entity-relationship.png)

### 3. Frontend Architecture  
- [Frontend](docs/diagrams/frontend-architecture.png)

## Authors
- [@Retr0-46](https://github.com/Retr0-46) - backend
- [@kas-whr](https://github.com/kas-whr) - frontend
- [@1r444444](https://github.com/1r444444) - UI/UX design + frontend
- [@DariaKomzolova](https://github.com/DariaKomzolova) - frontend
- [@dimiyx](https://github.com/dimiyx) - backend

## Implementation checklist

### Technical requirements (20 points)
#### Backend development (8ts)
- [x] Go-based microservices architecture (minimum 3 services) (3 points)
- [x] RESTful API with Swagger documentation (1 point)
- [ ] gRPC implementation for communication between microservices (1 point)
- [x] PostgreSQL database with proper schema design (1t)
- [x] JWT-based authentication and authorization (1 point)
- [ ] Comprehensive unit and integration tests (1 point)

#### Frontend development (8nts)
- [x] Flutter-based cross-platform application (mobile + web) (3 points)
- [x] Responsive UI design with custom [widgets](https://github.com/BeGraceful-Inc/BeGraceful/tree/dev2rontend/lib/src/ui/widgets) (1 point)
- [x] State management implementation (1 point) ([Providers](https://github.com/BeGraceful-Inc/BeGraceful/tree/dev2ontend/lib/src/providers), ChangeNotifier) 
- [ ] Offline data persistence (1 point)
- [x] Unit and widget [tests](https://github.com/BeGraceful-Inc/BeGraceful/tree/dev2/frontend/test) (1 point)
- [x] Support light and dark mode (1 point)

#### DevOps & deployment (4 points)
- [x] Docker compose for all services (1 point) [front](), [back](https://github.com/BeGraceful-Inc/BeGraceful/blob/dev2/backend/docker-compose.yml)
- ine implementation (1 point)
- [ ] Environment configuration management using config files (1 point)
- [ ] GitHub pages for the project (1 point)

### Non-Technical Requirements (10 points)
#### Project management (4 points)
- [x] GitHub organization with well-maintained repository (1 point)
- [x] Regular commits and meaningful pull requests from all team members (1 point)
- [x] [Project board](https://github.com/orgs/BeGraceful-Inc/projects/1) (GitHub Projects) with task tracking (1 point)
- [x] Team member roles and responsibilities documentation (1 point)

#### Documentation (4 points)
- [x] Project overview and setup instructions (1 point)
- [x] [Screenshots](https://github.com/BeGraceful-Inc/BeGraceful/tree/dev2/docs/screenshots) and [GIFs](https://github.com/BeGraceful-Inc/BeGraceful/tree/dev2/docs/gifs) of key features (1 API documentation (1 point)
- [x] [Architecture diagrams](https://github.com/BeGraceful-Inc/BeGraceful/tree/dev2/docs/diagrams) and explanations (1 point)

#### Code quality (2 points)
- [x] Consistent code style and formatting during CI/CD pipeline (1 point)
- [x] Code review participation and resolution (1 point)

### Bonus Features (up to 10 points)
- [ ] Localization for Russian (RU) and English (ENG) languages (2 points)
- [x] Good UI/UX design (up to 3 points)
- [ ] Integration with external APIs (fitness trackers, health devices) (up to 5 points)
-omprehensive error handling and user feedback (up to 2 points)
- [ ] Advanced animations and transitions (up to 3 points)
- [ ] Widget implementation for native mobile elements (up to 2 points)

Total points implemented: XX/30 (excluding bonus points)

`Note: For each implemented feature, provide a brief description or link to the relevant implementation below the checklist.`
