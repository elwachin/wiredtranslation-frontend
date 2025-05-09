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
