# 🎧 Lyricly — Real-Time Song Recognition & Lyrics Sync Web App

**Lyricly** is a sleek, AI-powered web app that listens to any song playing around you, instantly identifies it, and displays synced karaoke-style lyrics — all within a modern, responsive UI.

Built using the latest **Next.js App Router**, **Mistral AI**, **Tailwind CSS**, **ShadCN UI**, and more. Designed for music lovers who hear a random song they like and want lyrics _now_, without searching.

---

## 🚀 Features

- 🎙️ **Tap to Listen** – Mic button to listen to ambient audio and identify the song
- 🔍 **AI-Powered Song Recognition** – Uses `@ai-sdk/mistral` to detect the song
- 🎤 **Live Synced Lyrics** – Line-by-line lyrics displayed in real-time
- 🔗 **One-Click Platform Links** – Instantly open the song in Spotify, YouTube, Apple Music, etc.
- 📜 **Full Lyrics View** – Expand to see complete song lyrics
- 🌙 **Modern UI/UX** – Clean, mobile-first, with animations and dark mode support

---

## 🧱 Tech Stack

| Tech              | Usage                                |
| ----------------- | ------------------------------------ |
| **Next.js**       | App Router, Server Components        |
| **TypeScript**    | Type-safe coding                     |
| **Tailwind CSS**  | Utility-first styling                |
| **ShadCN UI**     | Reusable UI components               |
| **Framer Motion** | Smooth animations and transitions    |
| **Mistral AI**    | `@ai-sdk/mistral` for song detection |
| **Prisma**        | ORM for PostgreSQL                   |
| **PostgreSQL**    | Database for storing song/lyrics     |
| **Zod / Jotai**   | (Optional) for state validation/mgmt |

---

## 💡 How It Works

1. User opens the app and taps the **“Listen”** mic button.
2. The app listens to the background audio for a few seconds.
3. AI identifies the song and fetches:
   - Title, Artist, Album Art
   - Synced Lyrics (real-time)
   - Streaming links (Spotify, YouTube, etc.)
4. Option to **expand full lyrics** or **save/share** in later phases.

---

## 📦 Installation

### Prerequisites

- Node.js (v18 or higher)
- PostgreSQL database
- npm or yarn or pnpm or bun package manager

### Setup

1. **Clone the repository**

   ```bash
   git clone https://github.com/blazedglimmer/lyricly.git
   cd lyricly
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Environment Configuration**

   Create a `.env` file in the root directory:

   ```env
   DATABASE_URL=postgresql://your-db-url
   NEXT_PUBLIC_BASE_URL=http://localhost:3000
   # Add any other required API keys or tokens
   ```

4. **Database Setup**

   ```bash
   npx prisma generate
   npx prisma db push
   ```

5. **Start the development server**
   ```bash
   npm run dev
   ```

The app will be available at `http://localhost:3000`

## 🛠️ Project Structure

```
lyricly/
├── app/              # App Router pages and layouts
├── components/       # Reusable UI components (ShadCN + custom)
├── lib/             # Utility functions (AI, DB, lyrics sync)
├── prisma/          # Database schema and migrations
├── styles/          # Global Tailwind CSS styles
├── public/          # Static assets
└── package.json     # Project dependencies
```

## 🎨 Design Philosophy

### Visual Aesthetics

- **Glassmorphism/Neumorphism** - Subtle gradients and glow effects
- **Dynamic Typography** - Responsive font highlighting for current lyrics
- **Smooth Animations** - Powered by Framer Motion for fluid transitions
- **Theme Support** - Seamless dark/light mode switching

### User Experience

- **Micro-interactions** - Delightful hover effects and button animations
- **Performance** - Shimmer loaders and optimized rendering
- **Accessibility** - Full keyboard navigation and screen reader support
- **Mobile-first** - Responsive design with haptic feedback

## 🤖 AI Integration

Currently powered by:

- **Mistral AI** (`@ai-sdk/mistral`) for intelligent song identification
- **Audio Processing** - Advanced algorithms for music recognition
- **Lyrics Analysis** - AI-driven sentiment and vibe detection

_Extensible architecture supports additional audio fingerprinting APIs_

## 🚀 Available Scripts

```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run start        # Start production server
npm run lint         # Run ESLint
npm run type-check   # TypeScript type checking
```

## 🧪 Roadmap & Future Enhancements

- [x] **Personal Profiles** - Save favorite lyrics and build collections
- [x] **Listening History** - Track and revisit identified songs
- [x] **Social Features** - Share lyric snippets across platforms
- [x] **AI Translation** - Multi-language lyrics support
- [x] **Vibe Detection** - AI-powered mood and genre analysis
- [x] **PWA Support** - Full mobile app experience
- [ ] **Offline Mode** - Cache lyrics for offline listening
- [ ] **Spotify Integration** - Connect with music streaming services
- [ ] **Collaborative Playlists** - Share and discover with community

## 🛡️ Tech Stack

- **Framework:** Next.js 14 with App Router
- **Styling:** Tailwind CSS + ShadCN UI
- **Database:** PostgreSQL with Prisma ORM
- **AI/ML:** Mistral AI SDK
- **Animations:** Framer Motion
- **TypeScript:** Full type safety
- **Deployment:** Vercel-ready

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Created with ❤️ by [Akshay Shinde](https://github.com/blazedglimmer)**
- Thanks to the open-source community for the amazing tools and libraries
- Special thanks to all contributors and users who make this project possible

## 📞 Support

- 🐛 **Found a bug?** [Open an issue](https://github.com/blazedglimmer/lyricly/issues)
- 💡 **Have a feature request?** [Start a discussion](https://github.com/blazedglimmer/lyricly/discussions)
- 📧 **Need help?** Contact us at [support@lyricly.app](mailto:support@lyricly.app)

---

<div align="center">
  <strong>🎵 Discover music through the power of AI 🎵</strong>
  <br><br>
  <a href="https://lyricly.app">Live Demo</a> • 
  <a href="#installation">Get Started</a> • 
  <a href="https://github.com/blazedglimmer/lyricly/issues">Report Bug</a>
</div>
