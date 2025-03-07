# WebRTC with Socket.IO

![GitHub repo size](https://img.shields.io/github/repo-size/jayasuryard31/webrtc)  
![GitHub last commit](https://img.shields.io/github/last-commit/jayasuryard31/webrtc)

A WebRTC-based real-time communication application that enables peer-to-peer video, audio, and screen-sharing capabilities. This project uses [Socket.IO](https://socket.io/) for signaling between peers.

## Features

- Peer-to-peer video and audio streaming
- Screen sharing functionality
- Room-based communication (Lobby and Room support)
- Real-time signaling using Socket.IO
- Cross-browser compatibility (tested on Chrome and Firefox)

## Prerequisites

Before you begin, ensure you have the following installed:
- [Node.js](https://nodejs.org/) (v16.x or later recommended)
- [npm](https://www.npmjs.com/) (comes with Node.js)
- A modern browser with WebRTC support (e.g., Chrome, Firefox, Edge)

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/jayasuryard31/webrtc.git
   cd webrtc
   ```

2. **Install server dependencies:**
   Navigate to the `server` directory and install dependencies.
   ```bash
   cd server
   npm install
   ```

3. **Install client dependencies:**
   Navigate to the `client` directory and install dependencies.
   ```bash
   cd ../client
   npm install
   ```

4. **Start the signaling server:**
   From the `server` directory, run:
   ```bash
   npm start
   ```
   The server will run on `http://localhost:8000` by default (adjust port in `server/index.js` if needed).

5. **Start the client:**
   From the `client` directory, you can open `public/index.html` directly in a browser for development, or set up a local development server:
   ```bash
   npm start
   ```
   Then, navigate to `http://localhost:3000` (or the port specified in your setup).

## Usage

1. Launch the signaling server (`server/index.js`).
2. Open the client app in two separate browser windows or devices.
3. Use the Lobby interface (`Lobby.jsx`) to create or join a room.
4. Allow camera, microphone, and screen-sharing permissions when prompted.
5. Start streaming video/audio or sharing your screen with peers in the same room.

## Folder Structure

```
webrtc/
├── client/                    # Client-side code
│   ├── public/                # Static assets
│   │   ├── index.html         # Main HTML entry point
│   │   ├── index.css          # Main stylesheet
│   │   └── logo.svg           # Application logo
│   ├── src/                   # Source code
│   │   ├── context/           # React context for state management
│   │   │   └── SocketProvider.jsx  # Socket.IO context provider
│   │   ├── screens/           # React components for different screens
│   │   │   ├── Lobby.jsx      # Lobby screen for joining/creating rooms
│   │   │   └── Room.jsx       # Room screen for peer communication
│   │   ├── service/           # Service logic
│   │   │   └── peer.js        # WebRTC peer connection logic
│   │   ├── App.css            # App-specific styles
│   │   ├── App.js             # Main React component
│   │   ├── App.test.js        # Tests for App component
│   │   ├── index.js           # React entry point
│   │   ├── reportWebVitals.js # Web Vitals reporting
│   │   └── setupTests.js      # Test setup configuration
│   ├── .gitignore             # Git ignore file
│   ├── README.md              # Client-specific README (optional)
│   ├── package-lock.json      # Dependency lock file
│   └── package.json           # Client dependencies and scripts
└── server/                    # Server-side code
    ├── index.js               # Signaling server using Socket.IO
    ├── .gitignore             # Git ignore file
    ├── package-lock.json      # Dependency lock file
    └── package.json           # Server dependencies and scripts
```

## Configuration

- **Signaling Server:** Modify `server/index.js` to change the port or add SSL for production use.
- **WebRTC Options:** Adjust STUN/TURN servers in `client/src/service/peer.js` if needed (default uses Google's STUN servers).
- **Socket.IO:** The `SocketProvider.jsx` in `client/src/context` handles Socket.IO connections. Update the server URL there if the server is hosted elsewhere.

## Testing

The client includes basic test setup using Jest and React Testing Library:
- Run tests with:
  ```bash
  cd client
  npm test
  ```

## Contributing

Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m "Add your feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details (if applicable).

## Acknowledgments

- [WebRTC](https://webrtc.org/) for the real-time communication framework.
- [Socket.IO](https://socket.io/) for signaling.
- [React](https://reactjs.org/) for the frontend framework.
- [Node.js](https://nodejs.org/) for the server-side runtime.

## Contact

For questions or feedback, reach out to [jayasuryard31](https://github.com/jayasuryard31) on GitHub.
