# VREC — Voice Recognition & Recording AI

A modern web application for recording audio and getting AI-powered transcriptions.

**Frontend:** React + TypeScript + Vite + Tailwind CSS + shadcn/ui  
**Backend:** Python Flask (mock transcription API)

## Features

- ✨ Modern UI with gradient backgrounds and animations
- 🎤 Real-time voice recording with visualizer
- 🎵 Audio playback controls
- 🧠 AI-powered transcription (mock implementation)
- 📄 Download transcriptions as text files
- 📱 Fully responsive design
- 🔊 Real-time audio visualization

## Getting Started

### 1) Install and run the backend (Flask)

```bash
# From project root, navigate to server directory:
cd server

# Create and activate a virtual environment (recommended)
# Windows (PowerShell):
python -m venv .venv
.\.venv\Scripts\Activate.ps1

# macOS/Linux:
# python3 -m venv .venv
# source .venv/bin/activate

# Install Python dependencies
pip install -r requirements.txt

# Note: If you get PyAudio installation errors on Windows:
# pip install pipwin
# pipwin install pyaudio

# Run the Flask server
python app.py
# Backend runs on http://localhost:5000
```

### 2) Run the frontend (Vite + React)

```bash
# In another terminal, from project root:
npm install

# Start the development server
npm run dev
# Frontend runs on http://localhost:8080
# API calls are proxied to http://localhost:5000 via /api/*
```

## Usage

1. **Start Recording**: Click the microphone button to begin recording
2. **Stop Recording**: Click the stop button to end the recording
3. **View Transcription**: AI transcription will appear automatically
4. **Download**: Save your transcription as a text file
5. **Playback**: Use the play/pause controls to listen to your recording

## Development

### Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run lint` - Run ESLint
- `npm run preview` - Preview production build

### Project Structure

```
├── src/
│   ├── components/          # React components
│   ├── hooks/              # Custom React hooks
│   ├── lib/                # Utility functions
│   ├── pages/              # Page components
│   └── index.css           # Global styles
├── server/
│   ├── app.py              # Flask API server
│   └── requirements.txt    # Python dependencies
└── README.md
```

## Customization

### Integrating Real Speech Recognition

The current backend returns mock transcriptions. To integrate real speech recognition:

1. **OpenAI Whisper**: Replace the transcription logic in `server/app.py` with Whisper API calls
2. **Google Speech-to-Text**: Use Google Cloud Speech API
3. **AssemblyAI**: Integrate with AssemblyAI's transcription service
4. **Azure Speech Services**: Use Microsoft's speech recognition API

### Styling

The app uses Tailwind CSS with custom animations and gradients. Key styling files:
- `src/index.css` - Global styles and CSS variables
- `tailwind.config.ts` - Tailwind configuration with custom animations

## Browser Support

- Chrome/Edge: Full support with MediaRecorder API
- Firefox: Full support
- Safari: Supported (may require HTTPS in production)

## Production Deployment

1. Build the frontend: `npm run build`
2. Deploy the `dist` folder to your web server
3. Deploy the Flask backend to a Python hosting service
4. Update API endpoints in production configuration

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is open source and available under the MIT License.