# 🤖 Smart Rule-Based Chatbot

[![CI/CD](https://github.com/yourusername/rule-based-chatbot/workflows/CI%2FCD%20Pipeline/badge.svg)](https://github.com/yourusername/rule-based-chatbot/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.11+](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org/downloads/)
[![React](https://img.shields.io/badge/react-18.2.0-61dafb.svg)](https://reactjs.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.109.0-009688.svg)](https://fastapi.tiangolo.com/)

A modern, production-ready rule-based chatbot with a stunning UI, built using Python FastAPI backend and React frontend. Features advanced pattern matching, intent classification, conversation analytics, and real-time sentiment analysis.

![Chatbot Demo](https://via.placeholder.com/800x400/667eea/ffffff?text=Smart+Chatbot+Demo)

## ✨ Features

### Core Features
- 🎯 **Advanced Rule-Based Engine** - Pattern matching using regex and keyword detection
- 💬 **Real-time Chat Interface** - Smooth, responsive chat experience
- 🎨 **Modern UI/UX** - Beautiful gradient design with Tailwind CSS
- 🌓 **Dark/Light Mode** - Toggle between themes with smooth transitions
- 📊 **Analytics Dashboard** - Track conversations, intents, and response times
- 💾 **Conversation History** - Persistent storage with SQLite
- 🎭 **Sentiment Analysis** - Basic emotion detection in messages
- 🔄 **Session Management** - Multi-session support with unique IDs
- ⚡ **Fast Response Times** - Optimized for sub-100ms responses
- 📱 **Mobile Responsive** - Works perfectly on all devices

### Advanced Features
- 📈 **Intent Classification** - 15+ pre-configured intents
- 🎪 **Configurable Rules** - Easy-to-edit YAML configuration
- 🔍 **Pattern Matching** - Sophisticated regex-based matching
- 💯 **Confidence Scoring** - Response confidence metrics
- 📥 **Export Chat History** - Download conversations as text
- 🔄 **Hot Reload Rules** - Update rules without restart
- 🏥 **Health Monitoring** - Built-in health checks
- 📝 **Comprehensive Logging** - Detailed application logs
- 🐳 **Docker Support** - Containerized deployment ready
- 🚀 **CI/CD Pipeline** - Automated testing and deployment

## 🛠️ Tech Stack

### Backend
- **Framework**: FastAPI 0.109.0
- **Language**: Python 3.11+
- **Database**: SQLite with async support (SQLAlchemy)
- **API Documentation**: Swagger/OpenAPI
- **Pattern Matching**: Python regex
- **Configuration**: YAML, Python-dotenv

### Frontend
- **Framework**: React 18.2.0
- **Build Tool**: Vite 5.0
- **Styling**: Tailwind CSS 3.4
- **Icons**: Lucide React
- **HTTP Client**: Axios
- **Markdown Support**: React Markdown

### DevOps
- **Containerization**: Docker, Docker Compose
- **CI/CD**: GitHub Actions
- **Deployment**: Railway, Render, Vercel
- **Testing**: Pytest, React Testing Library
- **Linting**: Flake8, ESLint

## 📁 Project Structure

```
rule_based_chatbot/
├── backend/                    # FastAPI backend
│   ├── app/
│   │   ├── api/               # API routes and schemas
│   │   │   ├── endpoints.py   # REST API endpoints
│   │   │   └── schemas.py     # Pydantic models
│   │   ├── core/              # Core functionality
│   │   │   ├── config.py      # Configuration management
│   │   │   ├── database.py    # Database setup
│   │   │   └── rule_engine.py # Rule-based engine
│   │   ├── models/            # Database models
│   │   │   └── conversation.py
│   │   ├── services/          # Business logic
│   │   │   └── conversation_service.py
│   │   └── main.py           # Application entry point
│   ├── Dockerfile            # Backend container config
│   ├── requirements.txt      # Python dependencies
│   └── .env.example         # Environment variables template
│
├── frontend/                  # React frontend
│   ├── src/
│   │   ├── components/       # React components
│   │   │   ├── ChatInterface.jsx
│   │   │   ├── MessageBubble.jsx
│   │   │   ├── Header.jsx
│   │   │   ├── Sidebar.jsx
│   │   │   ├── Analytics.jsx
│   │   │   └── TypingIndicator.jsx
│   │   ├── services/         # API service layer
│   │   │   └── api.js
│   │   ├── styles/           # CSS styles
│   │   │   └── index.css
│   │   ├── App.jsx           # Main app component
│   │   └── main.jsx         # Entry point
│   ├── public/              # Static assets
│   ├── Dockerfile          # Frontend container config
│   ├── nginx.conf          # Nginx configuration
│   ├── package.json        # Node dependencies
│   └── vite.config.js      # Vite configuration
│
├── rules/                   # Chatbot rules configuration
│   └── chatbot_rules.yaml  # Intent patterns and responses
│
├── tests/                  # Unit tests
│   ├── test_rule_engine.py
│   └── __init__.py
│
├── deployment/            # Deployment configurations
│   ├── railway.json      # Railway deployment
│   ├── render.yaml       # Render deployment
│   └── vercel.json       # Vercel deployment
│
├── .github/
│   └── workflows/
│       └── ci.yml        # GitHub Actions CI/CD
│
├── docker-compose.yml    # Multi-container orchestration
├── .gitignore           # Git ignore rules
└── README.md           # This file
```

## 🚀 Quick Start

### Prerequisites
- Python 3.11 or higher
- Node.js 18 or higher
- npm or yarn
- Git

### Local Development Setup

#### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/rule-based-chatbot.git
cd rule-based-chatbot
```

#### 2. Backend Setup
```bash
# Navigate to backend directory
cd backend

# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Copy environment variables
cp .env.example .env

# Run the backend server
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```

Backend will be available at: `http://localhost:8000`
API Documentation: `http://localhost:8000/api/docs`

#### 3. Frontend Setup
```bash
# Open a new terminal
# Navigate to frontend directory
cd frontend

# Install dependencies
npm install

# Copy environment variables
cp .env.example .env

# Run the development server
npm run dev
```

Frontend will be available at: `http://localhost:5173`

### Using Docker (Recommended for Production)

```bash
# Build and run both services
docker-compose up -d

# View logs
docker-compose logs -f

# Stop services
docker-compose down
```

Access the application:
- Frontend: `http://localhost:80`
- Backend API: `http://localhost:8000`
- API Docs: `http://localhost:8000/api/docs`

## 📖 Usage Guide

### Starting a Conversation
1. Open the application in your browser
2. A new session is automatically created
3. Type your message in the input box
4. Press Enter or click the Send button

### Available Commands & Intents
- **Greetings**: "hello", "hi", "hey"
- **Help**: "help", "what can you do"
- **Products**: "show me products", "what do you offer"
- **Pricing**: "how much", "pricing", "cost"
- **Contact**: "contact", "support", "email"
- **Technical Support**: "not working", "error", "bug"
- **Business Hours**: "when are you open", "business hours"
- **Jokes**: "tell me a joke", "make me laugh"
- **Farewell**: "bye", "goodbye", "exit"

### Customizing Rules

Edit `rules/chatbot_rules.yaml` to add or modify intents:

```yaml
intents:
  - intent: custom_intent
    patterns:
      - "\\bcustom pattern\\b"
      - "another pattern"
    responses:
      - "Response 1"
      - "Response 2"
    sentiment: positive
```

After editing, reload rules via API:
```bash
curl -X POST http://localhost:8000/api/v1/reload-rules
```

### Analytics

View conversation analytics by clicking the "Analytics" button in the header. Metrics include:
- Total interactions
- Average response time
- Intent distribution
- Session information

### Export Chat History

Click the download icon in the chat header to export your conversation as a text file.

## 🌐 Deployment

### Deploy to Railway

1. **Sign up** at [Railway](https://railway.app)
2. **Connect your GitHub** repository
3. **Create new project** from repo
4. **Configure environment variables**:
   ```
   DEBUG=False
   LOG_LEVEL=INFO
   ```
5. **Deploy** - Railway auto-detects and deploys!

### Deploy to Render

1. **Sign up** at [Render](https://render.com)
2. **Create new Web Service**
3. **Connect repository**
4. **Configure build settings**:
   - Build Command: `pip install -r backend/requirements.txt`
   - Start Command: `cd backend && uvicorn app.main:app --host 0.0.0.0 --port $PORT`
5. **Deploy**

### Deploy Frontend to Vercel

1. **Sign up** at [Vercel](https://vercel.com)
2. **Import project** from GitHub
3. **Configure**:
   - Framework: Vite
   - Root Directory: `frontend`
   - Build Command: `npm run build`
   - Output Directory: `dist`
4. **Set environment variable**:
   ```
   VITE_API_BASE_URL=https://your-backend-url.railway.app
   ```
5. **Deploy**

### Deploy Frontend to Netlify

```bash
cd frontend
npm run build
# Upload 'dist' folder to Netlify
```

## 🧪 Testing

### Run Backend Tests
```bash
cd backend
pytest tests/ -v
```

### Run with Coverage
```bash
pytest tests/ -v --cov=app --cov-report=html
```

### Test API Endpoints
```bash
# Health check
curl http://localhost:8000/api/v1/health

# Send message
curl -X POST http://localhost:8000/api/v1/chat \
  -H "Content-Type: application/json" \
  -d '{"message": "hello"}'
```

## 📊 API Documentation

### Endpoints

#### POST /api/v1/chat
Send a message to the chatbot
```json
Request:
{
  "message": "hello",
  "session_id": "optional-session-id"
}

Response:
{
  "response": "Hello! How can I help you?",
  "session_id": "uuid",
  "intent": "greeting",
  "sentiment": "positive",
  "confidence": 0.95
}
```

#### POST /api/v1/session
Create a new conversation session
```json
Response:
{
  "session_id": "uuid",
  "created_at": "2024-01-01T00:00:00"
}
```

#### GET /api/v1/history/{session_id}
Get conversation history
```json
Response:
{
  "session_id": "uuid",
  "messages": [...],
  "total_messages": 10
}
```

#### GET /api/v1/analytics/{session_id}
Get session analytics
```json
Response:
{
  "total_interactions": 20,
  "avg_response_time_ms": 45.5,
  "intent_distribution": {
    "greeting": 5,
    "help": 3
  }
}
```

Full API documentation available at: `http://localhost:8000/api/docs`

## 🎨 Customization

### Changing Colors
Edit `frontend/tailwind.config.js`:
```javascript
theme: {
  extend: {
    colors: {
      primary: {...},
      secondary: {...}
    }
  }
}
```

### Adding New Intents
1. Edit `rules/chatbot_rules.yaml`
2. Add your intent with patterns and responses
3. Reload rules or restart the backend

### Custom Welcome Message
Modify `frontend/src/components/ChatInterface.jsx`:
```javascript
setMessages([{
  message: "Your custom welcome message!",
  is_user: false,
  ...
}])
```

## 🔧 Configuration

### Environment Variables

**Backend (.env)**
```env
APP_NAME=Rule-Based Chatbot
DEBUG=True
HOST=0.0.0.0
PORT=8000
CORS_ORIGINS=["http://localhost:3000"]
DATABASE_URL=sqlite+aiosqlite:///./chatbot.db
LOG_LEVEL=INFO
```

**Frontend (.env)**
```env
VITE_API_BASE_URL=http://localhost:8000
VITE_APP_NAME=Smart Chatbot
```

## 🐛 Troubleshooting

### Backend won't start
- Ensure Python 3.11+ is installed
- Check virtual environment is activated
- Verify all dependencies installed: `pip install -r requirements.txt`

### Frontend build fails
- Clear node_modules: `rm -rf node_modules && npm install`
- Check Node.js version: `node --version` (should be 18+)

### Database errors
- Delete `chatbot.db` and restart to recreate database
- Check write permissions in the backend directory

### CORS errors
- Update `CORS_ORIGINS` in backend `.env`
- Add frontend URL to allowed origins

## 🔮 Future Improvements

- [ ] Multi-language support (i18n)
- [ ] Voice input/output integration
- [ ] User authentication and authorization
- [ ] Advanced NLP with spaCy or transformers
- [ ] Integration with external APIs
- [ ] Rich media support (images, videos)
- [ ] Conversation branching and context
- [ ] A/B testing for responses
- [ ] Admin dashboard for rule management
- [ ] WebSocket support for real-time updates
- [ ] PostgreSQL/MySQL support
- [ ] Redis caching layer
- [ ] Prometheus metrics
- [ ] Grafana dashboards

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

Please ensure:
- Code follows project style guidelines
- All tests pass
- New features include tests
- Documentation is updated

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Your Name**
- GitHub: [@yourusername](https://github.com/chittesh24)
- LinkedIn: [Your LinkedIn](https://linkedin.com/in/chittesh-s)
- Email: chittesh.work@gmail.com

## 🙏 Acknowledgments

- [FastAPI](https://fastapi.tiangolo.com/) - Modern Python web framework
- [React](https://reactjs.org/) - UI library
- [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS
- [Lucide](https://lucide.dev/) - Beautiful icons
- [Vite](https://vitejs.dev/) - Next generation frontend tooling

## 📸 Screenshots

### Light Mode
![Light Mode](https://via.placeholder.com/800x500/ffffff/333333?text=Light+Mode+Screenshot)

### Dark Mode
![Dark Mode](https://via.placeholder.com/800x500/1a1a2e/ffffff?text=Dark+Mode+Screenshot)

### Analytics Dashboard
![Analytics](https://via.placeholder.com/800x500/667eea/ffffff?text=Analytics+Dashboard)

### Mobile View
![Mobile](https://via.placeholder.com/400x700/764ba2/ffffff?text=Mobile+Responsive)

---

⭐ **Star this repository** if you find it helpful!

📢 **Share** with others who might benefit from this project!

🐛 **Report bugs** via [GitHub Issues](https://github.com/yourusername/rule-based-chatbot/issues)

💬 **Questions?** Open a [Discussion](https://github.com/yourusername/rule-based-chatbot/discussions)
