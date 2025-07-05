# PartyMode - Setup Guide
## 🏆 UIUC Research Park 2025 Hackathon Winner (1st Place)

PartyMode is a real-time collaborative music queue app built for events, parties, and gatherings. Users can join a shared Spotify session using a unique code, request songs, and upvote or downvote tracks to shape the playlist  — all powered by the Spotify Web API.

![Screenshot 2025-07-04 at 15 04 04](https://github.com/user-attachments/assets/0a082abb-e9bc-47c9-8644-99abae2b022d)


### What It Does:
- Collaborative DJing: Let everyone at the party contribute to the vibe.

- Join with a Code: Users join sessions via a unique code on any device.

- Vote-Based Queue: Songs move up or down based on real-time votes.

- Live Sync: Queue updates instantly using WebSocket.

- Spotify Playback: Control playback via a connected Spotify Premium account.

<img width="1589" alt="Screenshot 2025-07-02 at 16 10 48" src="https://github.com/user-attachments/assets/00c6b46d-455d-4344-84b1-2e31bcb0c300" />

## Quick Start (5 minutes)

### 1. Install Dependencies
```bash
npm install
```

### 2. Spotify API Setup
1. Go to [Spotify Developer Dashboard](https://developer.spotify.com/dashboard)
2. Create a new app
3. Add redirect URI: `http://127.0.0.1:3001/auth/spotify/callback`
4. Copy Client ID and Client Secret

### 3. Environment Configuration
```bash
cp env.example .env
```
Edit `.env` with your Spotify credentials:
```
SPOTIFY_CLIENT_ID=your_client_id_here
SPOTIFY_CLIENT_SECRET=your_client_secret_here
SPOTIFY_REDIRECT_URI=http://127.0.0.1:3001/auth/spotify/callback
PORT=3001
```

### 4. Run the Application
```bash
npm run dev
```

Visit `http://127.0.0.1:3001` and start voting!

### Key Points
- Real-time voting updates
- Spotify Web API integration
- Mobile-responsive design
- Session management with unique codes
- Live participant tracking using WebSocket

![Screenshot 2025-07-04 at 15 03 30](https://github.com/user-attachments/assets/b805163c-4989-4730-8e43-454118cf22dd)

## Business Viability Points

### Market Size
- **Corporate Events**: $2B market
- **Bars & Venues**: $25B market
- **Social Gatherings**: Massive untapped market

### Revenue Model
1. **Freemium**: Free for small groups, premium for larger events
2. **B2B**: White-label for venues and corporate clients
3. **API Licensing**: For other music apps

### Competitive Advantage
- **Real-time collaboration** (vs. static playlists)
- **Democratized selection** (vs. one person controlling)
- **Social engagement** (vs. passive listening)

## Technical Architecture

### Backend (Node.js/Express)
- **Spotify Web API integration**
- **Socket.IO for real-time updates**
- **Session management**
- **Vote tracking and conflict resolution**

### Frontend (Vanilla JS + Tailwind)
- **Responsive design**
- **Real-time UI updates**
- **Spotify authentication flow**
- **Mobile-first approach**

## Troubleshooting

### Common Issues
1. **Spotify API errors**: Check credentials and redirect URI
2. **WebSocket disconnections**: Check network stability
3. **Vote sync issues**: Refresh page to reconnect

### Debug Mode
```bash
DEBUG=* npm run dev
```
