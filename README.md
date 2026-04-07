# 🐾 Tepetaps

Tepetaps is a pet adoption web platform where users can browse animals available for adoption, post adoption listings, manage their personal profile, and interact with a community of animal lovers.

## 🌐 Live Demo

The project is deployed and available at:

| Environment | URL |
|---|---|
| Custom Domain | [http://tepetaps.jaimegv.dev/](http://tepetaps.jaimegv.dev/) |
| Vercel | [https://tepetaps.vercel.app/](https://tepetaps.vercel.app/) |

---

## 🛠️ Tech Stack

### Backend
| Technology | Purpose |
|---|---|
| [Node.js](https://nodejs.org/) | JavaScript runtime |
| [Express.js](https://expressjs.com/) | Web framework and REST API |
| [Mongoose](https://mongoosejs.com/) | MongoDB ODM |
| [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) | Cloud-hosted NoSQL database |
| [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken) | JWT-based authentication |
| [bcrypt](https://github.com/kelektiv/node.bcrypt.js) | Password hashing |
| [Multer](https://github.com/expressjs/multer) | File/image upload handling |
| [cookie-parser](https://github.com/expressjs/cookie-parser) | Cookie management |
| [Nodemon](https://nodemon.io/) | Development auto-restart |

### Frontend
| Technology | Purpose |
|---|---|
| HTML5 | Page structure |
| CSS3 | Custom styling |
| [Bootstrap 5](https://getbootstrap.com/) | Responsive UI framework |
| [Bootstrap Icons](https://icons.getbootstrap.com/) | Icon library |
| [Font Awesome](https://fontawesome.com/) | Additional icons |
| Vanilla JavaScript | Client-side logic |

### DevOps & Deployment
| Technology | Purpose |
|---|---|
| [Vercel](https://vercel.com/) | Serverless deployment |
| [Azure Pipelines](https://azure.microsoft.com/en-us/products/devops/pipelines) | CI/CD pipeline (build, test, deploy) |
| [Azure Web Apps](https://azure.microsoft.com/en-us/products/app-service/web) | Cloud hosting (dev & prod environments) |

---

## 📁 Project Structure

```
tepetaps/
├── controllers/         # Business logic and route handlers
│   ├── router.js        # Main Express router
│   ├── data_handler.js  # Core data operations (login, register, etc.)
│   ├── animal.js        # Animal-related logic
│   ├── usuario.js       # User-related logic
│   ├── publicacion.js   # Post-related logic
│   ├── token_utils.js   # JWT verification utilities
│   └── login_router.js  # Login routing
├── models/              # Mongoose schemas and models
│   ├── animals.js       # Animal schema
│   ├── users.js         # User schema
│   ├── publicaciones.js # Post schema
│   └── admins.js        # Admin schema
├── routes/              # Express route definitions
│   ├── peluditos.js     # Animal listing routes
│   ├── perfilPersonal.js# User profile routes
│   ├── publicaciones.js # Community posts routes
│   ├── darAdopcion.js   # Adoption listing routes
│   └── admin.js         # Admin panel routes
├── views/               # Frontend HTML pages and assets
│   ├── home.html        # Landing page
│   ├── adoptar.html     # Adoption browsing page
│   ├── darAdopcion.html # Post an animal for adoption
│   ├── publicaciones.html # Community posts
│   ├── perfilPersonal.html# User profile page
│   ├── admin.html       # Admin panel
│   └── css/             # Stylesheets
├── data/                # Seed/sample JSON data
├── server.js            # Application entry point
├── vercel.json          # Vercel deployment configuration
└── azure-pipelines.yml  # Azure CI/CD pipeline configuration
```

---

## ✨ Features

- **User Authentication** – Register and log in with JWT-based sessions stored in cookies
- **Animal Listings** – Browse animals available for adoption with details such as breed, age, location, coat, vaccinations, and more
- **Post an Animal** – Submit animals for adoption with photo uploads
- **Community Posts** – Read and create community posts/publications
- **Personal Profile** – Manage your account and track your animals and posts
- **Admin Panel** – Administrative interface for platform management
- **Role-Based Access** – Separate `USER` and `ADMIN` roles with protected routes

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) v20+
- A MongoDB Atlas connection string (or local MongoDB instance)

### Installation

```bash
# Clone the repository
git clone https://github.com/JaimeGalindoV/tepetaps.git
cd tepetaps

# Install dependencies
npm install
```

### Running the App

```bash
# Production
npm start

# Development (with auto-reload)
npm run dev
```

The app will be available at `http://localhost:3000`.

---

## 🔄 CI/CD Pipeline

The project uses **Azure Pipelines** with three stages:

1. **Build** – Installs dependencies, runs build and tests, and archives the artifact.
2. **Deploy Dev** – Deploys every branch/PR to the `Tepetaps-dev` Azure Web App.
3. **Deploy Prod** – Deploys the `master` branch only to the `Tepetaps` Azure Web App.

---

## 📄 License

ISC
