# 🎨 Collaborative Drawing Board - WebSocket Application

A real-time collaborative drawing application built with WebSockets and Node.js, deployed on Azure App Service. Multiple users can draw together simultaneously and see each other's drawings in real-time!

![WebSocket Drawing App](https://img.shields.io/badge/WebSocket-Enabled-green)
![Node.js](https://img.shields.io/badge/Node.js-18.x-brightgreen)
![Azure](https://img.shields.io/badge/Azure-Ready-blue)
![License](https://img.shields.io/badge/License-MIT-yellow)

## 🌟 Features

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
git clone https://github.com/yourusername/websocket-drawing-app.git

# Navigate to project directory
cd websocket-drawing-app
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
├── 📄 web.config         # Azure IIS configuration
├── 📄 .gitignore         # Git ignore rules
├── 📄 README.md          # This file
└── 📁 public/            # Static files (frontend)
    ├── 📄 index.html     # Main HTML page
    ├── 📄 app.js        # Client-side JavaScript
    └── 📄 styles.css    # Styling
```

## 🌐 Azure Deployment Guide

### Step 1: Create Azure Resources

Using Azure CLI:
```bash
# Login to Azure
az login

# Create resource group
az group create --name websocket-exercise-rg --location eastus

# Create app service plan
az appservice plan create \
  --name websocket-plan \
  --resource-group websocket-exercise-rg \
  --sku F1

# Create web app
az webapp create \
  --resource-group websocket-exercise-rg \
  --plan websocket-plan \
  --name websocket-drawing-[yourname] \
  --runtime "NODE:18-lts"

# Enable WebSockets (IMPORTANT!)
az webapp config set \
  --resource-group websocket-exercise-rg \
  --name websocket-drawing-[yourname] \
  --web-sockets-enabled true
```

### Step 2: Deploy Your Code

```bash
# Add Azure remote
git remote add azure https://[yourname]@websocket-drawing-[yourname].scm.azurewebsites.net/websocket-drawing-[yourname].git

# Push to Azure
git push azure master
```

### Step 3: Verify Deployment

Visit: `https://websocket-drawing-[yourname].azurewebsites.net`

## 🧪 Testing

### Local Testing Checklist

- [ ] Start server with `npm run dev`
- [ ] Open http://localhost:3000 in browser
- [ ] Check "Connected" status appears
- [ ] Open second browser window
- [ ] Draw in one window, verify it appears in other
- [ ] Test color picker
- [ ] Test brush size slider
- [ ] Test clear canvas button
- [ ] Check user count updates

## 🚀 Future Enhancements

- [ ] **User Authentication** - Add login system
- [ ] **Named Cursors** - Show who is drawing
- [ ] **Drawing Rooms** - Separate canvases for different groups
- [ ] **Save/Load** - Persist drawings to database
- [ ] **Drawing Tools** - Add shapes, eraser, undo/redo
- [ ] **Chat Feature** - Add text chat alongside drawing
- [ ] **Drawing Replay** - Play back drawing history
- [ ] **Export Image** - Save canvas as PNG/JPG