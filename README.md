# Collaborative Document Editor

## Overview
A modern, full-stack collaborative document editor built with React 18 and Node.js. Features a rich text editor powered by TipTap, real-time document management, and a clean, responsive interface.

## ✨ Features
- **Rich Text Editing**: Modern WYSIWYG editor with TipTap
- **Document Management**: Create, save, open, and export documents
- **Modern UI**: Clean, responsive design with professional styling
- **Type Safety**: Full TypeScript implementation
- **Security**: Helmet, CORS, and rate limiting
- **Docker Support**: Containerized deployment
- **API Integration**: RESTful backend with proper error handling

## 📸 Demo

### Application Screenshots

*Screenshots will be added here to showcase the application interface and features.*

<!-- Add screenshots here:
![Main Interface](screenshots/main-interface.png)
![Rich Text Editor](screenshots/editor.png)
![File Operations](screenshots/file-menu.png)
-->

## 🛠 Tech Stack

### Frontend
- **React 18** - Latest React with concurrent features
- **TypeScript 5.3** - Type safety and modern JS features
- **TipTap 2.1** - Modern rich text editor
- **Axios** - HTTP client for API calls
- **Modern CSS** - Responsive design with CSS Grid/Flexbox

### Backend
- **Node.js 18+** - Latest LTS runtime
- **Express 4.18** - Web framework
- **TypeScript 5.3** - Type safety
- **Helmet** - Security middleware
- **CORS** - Cross-origin resource sharing
- **Rate Limiting** - API protection

## 📁 Project Structure
```
collaborative-document-editor/
├── frontend/
│   ├── public/
│   │   └── index.html
│   ├── src/
│   │   ├── components/
│   │   │   ├── Editor.tsx          # TipTap rich text editor
│   │   │   ├── Toolbar.tsx         # Formatting toolbar
│   │   │   └── FileMenu.tsx        # File operations
│   │   ├── styles/
│   │   │   └── main.css           # Modern responsive styles
│   │   ├── App.tsx                # Main app component
│   │   └── index.tsx              # React 18 root
│   ├── .env                       # Environment variables
│   ├── package.json               # Dependencies & scripts
│   └── tsconfig.json              # TypeScript config
├── backend/
│   ├── src/
│   │   ├── controllers/
│   │   │   └── documentController.ts  # CRUD operations
│   │   ├── models/
│   │   │   └── Document.ts           # Data models & service
│   │   ├── routes/
│   │   │   └── api.ts               # API routes
│   │   └── app.ts                   # Express server
│   ├── .env                         # Environment variables
│   ├── package.json                 # Dependencies & scripts
│   └── tsconfig.json                # TypeScript config
├── docker-compose.yml               # Multi-container setup
├── Dockerfile.frontend              # Frontend container
├── Dockerfile.backend               # Backend container
├── .gitignore                       # Git ignore rules
└── README.md                        # This file
```

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ and npm
- Docker & Docker Compose (for containerized deployment)

### Local Development

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd collaborative-document-editor
   ```

2. **Backend Setup:**
   ```bash
   cd backend
   npm install
   npm run dev    # Development with hot reload
   ```

3. **Frontend Setup (new terminal):**
   ```bash
   cd frontend
   npm install
   npm start      # Development server
   ```

4. **Access the application:**
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:5000
   - Health Check: http://localhost:5000/api/health

### Docker Deployment

1. **Build and run with Docker Compose:**
   ```bash
   docker-compose up --build
   ```

2. **Access the application:**
   - Frontend: http://localhost:3000
   - Backend: http://localhost:5000

## 📚 API Documentation

### Endpoints
- `GET /api/health` - Health check
- `GET /api/documents` - List all documents
- `GET /api/documents/:id` - Get document by ID
- `POST /api/documents` - Create new document
- `PUT /api/documents/:id` - Update document
- `DELETE /api/documents/:id` - Delete document

### Request/Response Examples

**Create Document:**
```bash
curl -X POST http://localhost:5000/api/documents \
  -H "Content-Type: application/json" \
  -d '{"title": "My Document", "content": "<p>Hello World</p>"}'
```

## 🔧 Development Scripts

### Frontend
- `npm start` - Development server
- `npm run build` - Production build
- `npm test` - Run tests

### Backend
- `npm run dev` - Development with hot reload
- `npm run build` - Compile TypeScript
- `npm start` - Run production build

## 🐳 Docker Commands

```bash
# Build and start services
docker-compose up --build

# Start in background
docker-compose up -d

# Stop services
docker-compose down

# View logs
docker-compose logs -f

# Rebuild specific service
docker-compose build frontend
```

## 🔒 Security Features
- Helmet.js for security headers
- CORS configuration
- Rate limiting (100 requests per 15 minutes)
- Input validation
- Error handling middleware
- Non-root Docker user

## 🎨 UI/UX Features
- Responsive design (mobile-friendly)
- Modern typography and spacing
- Professional color scheme
- Loading states
- Error handling
- Keyboard shortcuts support

## 🚀 Performance Optimizations
- React 18 concurrent features
- Code splitting ready
- Optimized Docker images (Alpine Linux)
- Efficient bundle sizes
- Source maps for debugging

## 🤝 Contributing
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📝 License
MIT License - see LICENSE file for details

## 🐛 Troubleshooting

**Port conflicts:**
```bash
# Check what's using the ports
netstat -tulpn | grep :3000
netstat -tulpn | grep :5000
```

**Docker issues:**
```bash
# Clean up Docker
docker-compose down -v
docker system prune -f
```

**Node modules issues:**
```bash
# Clean install
rm -rf node_modules package-lock.json
npm install
```

---

## 👨‍💻 Author

**Created by [Sushant Sonbarse](https://github.com/sonbarse17/)**

📂 **Repository:** https://github.com/sonbarse17/collaborative-document-editor

⭐ If you found this project helpful, please give it a star!