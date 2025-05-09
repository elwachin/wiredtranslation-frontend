# LanguageWire Translation UI

Frontend application for the LanguageWire Full Stack ML Engineer Challenge that provides:

- A modern UI for translating text into 5 supported languages
- Real-time translation that updates after typing pauses for 1 second
- Support for Jeringoza translation

## 🚀 Setup & Installation

### Prerequisites
- Node.js 16+
- npm

### Installation

```bash
npm install
```

## 🏃‍♂️ Running the Application

```bash
npm run dev
```

The application will be available at http://localhost:5173

### API Configuration for Local Development

Before running the application locally, you need to update the API URL in `frontend/src/constants.js`:

1. Open `frontend/src/constants.js`
2. Comment out the production API URL and uncomment the local development URL:
   ```javascript
   // API configuration
   // export const API_URL = 'https://wiredtranslation-backend.onrender.com'
   // For local development, uncomment the line below and comment out the line above
   export const API_URL = 'http://localhost:8000'
   ```

## 🔧 Features

- Translates text into Spanish, German, French, Italian, and Danish
- Translates any input text into Jeringoza
- Real-time translation after 1 second typing pause
- Responsive design

## 📝 Backend Integration

This frontend application communicates with the translation API backend which should be running on http://localhost:8000.

Make sure the backend server is running before using the translation features.

## 🛠️ Development

This project is built with:
- Vue 3
- Vite
- Axios for API communication
