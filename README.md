# Lubricentro RyM - User Management System

A comprehensive React-based web application for managing auto service center operations, including user authentication, order management, appointment scheduling, and customer feedback.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Available Scripts](#available-scripts)
- [Project Structure](#project-structure)
- [API Documentation](#api-documentation)
- [Component Documentation](#component-documentation)
- [Best Practices](#best-practices)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

Lubricentro RyM is a full-stack web application designed to streamline operations for an auto service center. The application provides:

- **User Management**: Registration, authentication, and profile management
- **Order Management**: Create, view, and manage service orders
- **Appointment Scheduling**: Calendar-based appointment booking system
- **Service Selection**: Choose from available services
- **Feedback System**: Comments and ratings functionality
- **Protected Routes**: Secure access to authenticated features

## ✨ Features

### Authentication & User Management
- User registration with validation
- Secure login with JWT tokens
- Password recovery system
- User profile viewing and editing
- Protected routes for authenticated users

### Order Management
- Create service orders with vehicle information
- View list of user orders with pagination
- Delete orders
- Order status tracking

### Appointment Scheduling
- Service selection interface
- Calendar-based date selection
- Available hours display
- Real-time availability checking

### Feedback System
- Create, edit, and delete comments
- Star-based rating system (1-5 stars)
- User-specific comment management

## 🛠 Tech Stack

### Frontend
- **React 18.3.1** - UI library
- **React Router DOM 6.26.0** - Routing
- **Redux Toolkit 2.3.0** - State management
- **Formik 2.4.6** - Form handling
- **Yup 1.4.0** - Form validation
- **Bootstrap 5.3.3** - UI framework
- **React Bootstrap 2.10.4** - Bootstrap components
- **Axios 1.7.3** - HTTP client
- **JWT Decode 4.0.0** - Token decoding
- **React DatePicker 7.3.0** - Date selection
- **Font Awesome** - Icons

### Build Tools
- **Create React App 5.0.1** - Build configuration
- **React Scripts** - Build scripts

## 📦 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (version 18.x or higher)
- **npm** (version 9.x or higher) or **yarn**
- A backend API server running (see API documentation for endpoints)

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/bacosta30762/ProyectoFinalFidelitasUser.git
   cd ProyectoFinalFidelitasUser
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure environment variables**
   Create a `.env` file in the root directory:
   ```env
   REACT_APP_API_URL=http://localhost:5000
   ```
   Replace with your actual backend API URL.

4. **Start the development server**
   ```bash
   npm start
   ```

5. **Open your browser**
   Navigate to `http://localhost:3000`

## ⚙️ Configuration

### Environment Variables

Create a `.env` file in the root directory with the following variables:

| Variable | Description | Example |
|----------|-------------|---------|
| `REACT_APP_API_URL` | Backend API base URL | `http://localhost:5000` |

**Note**: For production deployment, set `REACT_APP_API_URL_PROD` as a GitHub secret if using GitHub Actions.

### Local Development Setup

1. Create `.env.local` for local development:
   ```env
   REACT_APP_API_URL=http://localhost:5000
   ```

2. Ensure your backend API is running and accessible at the configured URL.

## 📜 Available Scripts

### `npm start`
Runs the app in development mode at `http://localhost:3000`. The page reloads automatically when you make changes.

### `npm test`
Launches the test runner in interactive watch mode. See [Running Tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`
Builds the app for production to the `build` folder. The build is optimized and minified for best performance.

### `npm run eject`
**⚠️ Warning**: This is a one-way operation. Once you eject, you can't go back!

Ejects from Create React App, giving you full control over the build configuration.

## 📁 Project Structure

```
ProyectoFinalFidelitasUser/
├── public/
│   └── index.html          # HTML template
├── src/
│   ├── assets/             # Static assets (images)
│   ├── components/
│   │   ├── api/            # API services
│   │   │   └── horasApi.js # RTK Query API for available hours
│   │   ├── Comentarios/    # Comments and ratings components
│   │   ├── Estilos/        # CSS styles for forms
│   │   ├── HeaderFooter/   # Header and Footer components
│   │   ├── Home/           # Home page component
│   │   ├── Login/          # Authentication components
│   │   ├── orden/          # Order management components
│   │   ├── Perfil/         # User profile components
│   │   ├── Planificacion/  # Appointment scheduling components
│   │   ├── ProtectedRoute/ # Route protection component
│   │   ├── reportes/       # Reports components (if used)
│   │   ├── Servicios/      # Service utilities
│   │   └── Validaciones/   # Form validation components
│   ├── App.jsx             # Main application component
│   ├── index.js            # Application entry point
│   ├── index.css           # Global styles
│   └── store.js            # Redux store configuration
├── .env                    # Environment variables (not in git)
├── .gitignore              # Git ignore rules
├── package.json            # Dependencies and scripts
└── README.md               # This file
```

## 📚 Documentation

For detailed documentation, see:

- **[API Documentation](./docs/API_DOCUMENTATION.md)** - Complete API reference
- **[Component Documentation](./docs/COMPONENT_DOCUMENTATION.md)** - React components guide
- **[Contributing Guidelines](./docs/CONTRIBUTING.md)** - Development best practices

## 🔐 Authentication Flow

1. User registers or logs in
2. Backend returns JWT token
3. Token is stored in `localStorage`
4. Token is included in API requests via `Authorization` header
5. Protected routes check for token existence
6. User can log out, which removes the token

## 🎨 Styling

The application uses:
- **Bootstrap 5** for responsive layout and components
- **Custom CSS** files for component-specific styling
- **React Bootstrap** for pre-styled React components

## 🧪 Testing

Run tests with:
```bash
npm test
```

The project uses:
- **@testing-library/react** for component testing
- **@testing-library/jest-dom** for DOM matchers
- **@testing-library/user-event** for user interaction simulation

## 🚢 Deployment

### GitHub Pages

The project is configured for GitHub Pages deployment using GitHub Actions.

1. Set up GitHub secrets:
   - `REACT_APP_API_URL_PROD`: Production API URL

2. Push to `main` branch to trigger automatic deployment

3. The app will be available at:
   ```
   http://bacosta30762.github.io/ProyectoFinalFidelitasUser
   ```

### Manual Build

1. Build the production bundle:
   ```bash
   npm run build
   ```

2. Deploy the `build` folder to your hosting service

## 🤝 Contributing

Please read [CONTRIBUTING.md](./docs/CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## 📝 License

This project is private and proprietary.

## 👥 Authors

- **bacosta30762** - Initial work

## 🙏 Acknowledgments

- Create React App team
- React community
- Bootstrap team
- All contributors to the open-source libraries used in this project

---

For more detailed information, please refer to the [API Documentation](./docs/API_DOCUMENTATION.md) and [Component Documentation](./docs/COMPONENT_DOCUMENTATION.md).
