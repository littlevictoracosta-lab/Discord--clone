# Discord Clone

A real-time communication platform with 3D avatar support and multiplayer networking capabilities.

## 🎮 Features

- **Real-time Messaging**: Instant message delivery and updates
- **3D Avatars**: Three.js-based 3D player models with network synchronization
- **Multiplayer Support**: Real-time position updates for connected players
- **Chrome Debugging**: Built-in VS Code debugging configuration for seamless development

## 🛠️ Technology Stack

- **Frontend**: Chrome-based web application
- **3D Graphics**: Three.js for 3D avatar rendering
- **Real-time Communication**: Network-based player position synchronization
- **Development**: VS Code with Chrome DevTools integration

## 🚀 Getting Started

### Prerequisites
- Node.js and npm installed
- VS Code (recommended for debugging)
- Google Chrome browser

### Installation

1. Clone the repository:
```bash
git clone https://github.com/littlevictoracosta-lab/Discord--clone.git
cd Discord--clone
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm start
```

The application will be available at `http://localhost:3000`

### Debugging

Use the included VS Code launch configuration to debug in Chrome:

1. Press `F5` or go to Run → Start Debugging
2. This will launch Chrome pointing to localhost:3000
3. Set breakpoints and use Chrome DevTools as needed

## 📋 Project Structure

- `launch.json` - VS Code debugging configuration
- Player networking and 3D avatar synchronization code

## 🔄 Network Player Updates

The application uses real-time network updates to synchronize player positions across clients:

```javascript
function updateNetworkPlayer(jsonData) {
    const playerData = JSON.parse(jsonData);
    let playerModel = gameScene.getObjectByName(playerData.playerId);
    
    if (playerModel) {
        playerModel.position.set(
            playerData.position.x, 
            playerData.position.y, 
            playerData.position.z
        );
    }
}
```

## 📝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is open source and available under the MIT License.

## 👤 Author

[littlevictoracosta-lab](https://github.com/littlevictoracosta-lab)

---

**Last Updated**: June 20, 2026
