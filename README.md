# 🎨 Collaborative Drawing Board - WebSocket Application

A real-time collaborative drawing application built with WebSockets and Node.js, ready to be deployed on Azure App Service. Multiple users can draw together simultaneously and see each other's drawings in real-time!



## Features

- ✏️ **Real-time collaborative drawing** - See others draw as it happens
- 🎨 **Color picker** - Choose any color for drawing
- 🖌️ **Adjustable brush size** - From 1px to 20px
- 👥 **User counter** - See how many people are drawing
- 🔄 **Auto-reconnection** - Automatically reconnects if connection drops
- 📱 **Mobile support** - Works on phones and tablets with touch
- 🧹 **Clear canvas** - Clear the entire canvas for everyone
- 💾 **Drawing history** - New users see previous drawings when they join


## 🛠️ Technology Stack

- **Backend:** Node.js with Express.js
- **WebSocket Library:** ws (WebSocket)
- **Frontend:** Vanilla JavaScript, HTML5 Canvas
- **Styling:** CSS3 with responsive design
- **Cloud Platform:** Azure App Service
- **Protocol:** WebSocket (wss:// for secure connections)

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- ✅ Node.js (v14.0.0 or higher)
- ✅ npm (comes with Node.js)
- ✅ Git
- ✅ Azure account (free tier works)
- ✅ Code editor (VS Code recommended)

## 🔧 Installation & Setup

### 1. Clone the Repository

```bash
# Clone this repository
git clone https://github.com/ramymohamed10/25F_Websocket-Drawing-App.git

# Navigate to project directory
cd 25F_Websocket-Drawing-App
```

### 2. Install Dependencies

```bash
# Install required packages
npm install
```

### 3. Run Locally

```bash
# Start the development server
npm run dev

# Or for production
npm start
```

### 4. Open in Browser

```
http://localhost:3000
```

Open multiple browser windows to test real-time synchronization!

## 📁 Project Structure

```
websocket-drawing-app/
├── 📄 server.js           # WebSocket server implementation
├── 📄 package.json        # Dependencies and scripts
├── 📄 package-lock.json   # Locked dependency versions
├── 📄 .gitignore         # Git ignore rules
├── 📄 README.md          # This file
└── 📁 public/            # Static files (frontend)
    ├── 📄 index.html     # Main HTML page
    ├── 📄 app.js        # Client-side JavaScript
    └── 📄 styles.css    # Styling
```

## 🚀 Future Enhancements

- [ ] **User Authentication** - Add login system
- [ ] **Named Cursors** - Show who is drawing
- [ ] **Drawing Rooms** - Separate canvases for different groups
- [ ] **Save/Load** - Persist drawings to database
- [ ] **Drawing Tools** - Add shapes, eraser, undo/redo
- [ ] **Chat Feature** - Add text chat alongside drawing
- [ ] **Drawing Replay** - Play back drawing history
- [ ] **Export Image** - Save canvas as PNG/JPG