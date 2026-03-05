# Gestion de Stock - Frontend

This is the frontend application for the Stock Management system, built with React and Vite.

## Features

- Modern React 19 with functional components
- Vite for fast development and building
- Responsive design
- Real-time stock management interface
- 📊 **Dashboard**: Overview of inventory stats, low stock alerts, recent movements
- 📦 **Products**: CRUD operations for products with categories
- 🏷️ **Categories**: Organize products by category
- 🏭 **Suppliers**: Manage supplier information
- 🔄 **Stock Movements**: Track stock in/out and adjustments

## Prerequisites

- Node.js 16+ 
- npm or yarn

## Installation

1. Clone the repository:
```bash
git clone https://github.com/MohamedBouslimi/gestion-de-stock-frontend.git
cd gestion-de-stock-frontend
```

2. Install dependencies:
```bash
npm install
```

3. Configure environment variables:
```bash
cp .env.example .env
```
Edit `.env` and set your backend API URL:
```
VITE_API_BASE_URL=http://localhost:3001/api
```

## Development

Start the development server:
```bash
npm run dev
```

The application will be available at http://localhost:5173

## Production

Build for production:
```bash
npm run build
```

The built files will be in the `dist` directory.

## Configuration

- `VITE_API_BASE_URL`: Backend API base URL (default: http://localhost:3001/api)

## Backend

This frontend connects to the backend API. Make sure to run the backend server:
https://github.com/MohamedBouslimi/gestion-de-stock-backend 
- npm

### Install Dependencies
```bash
npm install
```

### Run in Development Mode
```bash
npm run dev
```
This starts both the Vite dev server and Electron in development mode.

### Build for Production
```bash
npm run build
```

### Create Windows Executable
```bash
npm run dist:win
```
The installer will be created in the `release` folder.

## Scripts

| Script | Description |
|--------|-------------|
| `npm run dev` | Start development mode |
| `npm run build` | Build the React frontend |
| `npm run start` | Run the built app in Electron |
| `npm run dist` | Build distributable package |
| `npm run dist:win` | Build Windows installer (.exe) |

## Project Structure

```
├── src/
│   ├── main/           # Electron main process
│   │   └── main.js
│   ├── backend/        # Express API server
│   │   ├── database.js
│   │   └── server.js
│   └── renderer/       # React frontend
│       ├── App.jsx
│       ├── App.css
│       └── main.jsx
├── assets/             # App icons
├── dist/               # Built frontend
├── release/            # Built executables
├── index.html          # Entry HTML
├── vite.config.js      # Vite configuration
└── package.json
```

## Database

The SQLite database (`stock.db`) is stored in the user data folder:
- Windows: `%APPDATA%/gestion-de-stock/`

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/dashboard/stats` | Get dashboard statistics |
| GET | `/api/products` | List all products |
| POST | `/api/products` | Create product |
| PUT | `/api/products/:id` | Update product |
| DELETE | `/api/products/:id` | Delete product |
| GET | `/api/categories` | List all categories |
| POST | `/api/categories` | Create category |
| PUT | `/api/categories/:id` | Update category |
| DELETE | `/api/categories/:id` | Delete category |
| GET | `/api/suppliers` | List all suppliers |
| POST | `/api/suppliers` | Create supplier |
| PUT | `/api/suppliers/:id` | Update supplier |
| DELETE | `/api/suppliers/:id` | Delete supplier |
| GET | `/api/movements` | List stock movements |
| POST | `/api/movements` | Record stock movement |

## License

ISC
