# MockMate - AI-Powered Mock Interview Simulator

MockMate is an AI-powered mock interview simulator that provides real-time interview practice with role-tailored questions, audio evaluation, camera feed support, and instant feedback.

---

## 🚀 Features

- **Personalized Interview Setup**: Choose your job role, experience level, and tech stack tags.
- **AI-Generated Questions & Evaluation**: Dynamic questions and intelligent performance analysis powered by Google Gemini.
- **Audio & Video Integration**: Real-time microphone audio visualizer and live camera preview.
- **Session History & Analytics**: Review past interview scores and detailed feedback.
- **Pre-seeded Demo Account**: Quick login with demo credentials (`demo@mockmate.com` / `password123`).

---

## 🛠️ Project Structure

```text
mockmatee-main/
├── public/                 # Static assets (favicon, etc.)
├── server/                 # Express backend API
│   ├── data/               # Local JSON database (users & interviews)
│   └── index.js            # Backend server entry point
├── src/                    # Frontend React application
│   ├── components/         # UI components (AudioVisualizer, CameraFeed, SetupForm, etc.)
│   ├── App.jsx             # Main application component
│   ├── config.js           # API and client configurations
│   ├── index.css           # Global application styles
│   ├── main.jsx            # React root entry point
│   └── questions.json      # Offline fallback question bank
├── index.html              # Frontend HTML entry point
├── package.json            # Project dependencies and npm scripts
└── vite.config.js          # Vite configuration
```

---

## ⚙️ Environment Configuration

The application works out of the box with default settings. You can optionally configure environment variables by creating a `.env` file in the project directory:

```env
# Port for the backend API server (defaults to 5000 if not set)
PORT=5000

# Optional Google Gemini API Key for server-side evaluation
GEMINI_API_KEY=your_gemini_api_key_here
```

> **Note:** `.env` files are ignored by git to protect sensitive credentials. If no API key is provided, the simulator gracefully falls back to the pre-packaged offline question bank (`src/questions.json`).

---

## 📦 Installation & Setup

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Run both frontend and backend concurrently:**
   ```bash
   npm run dev
   ```

3. **Or run individually:**
   - **Frontend:** `npm run dev:frontend` (starts Vite dev server)
   - **Backend:** `npm run dev:backend` (starts Express server on `http://localhost:5000`)
