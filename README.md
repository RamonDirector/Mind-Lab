# 🧠 Mind Games MVP

A cognitive training app with Elo-based adaptive difficulty. Train your memory, flexibility, and verbal fluency through scientifically-inspired mini-games.

![Mind Games](https://img.shields.io/badge/React-18-blue) ![Vite](https://img.shields.io/badge/Vite-5-purple) ![License](https://img.shields.io/badge/License-MIT-green)

## ✨ Features

### 🎮 Three Training Modules

| Game | Domain | Description |
|------|--------|-------------|
| **Pattern Recall** | Working Memory | Watch sequences light up, replicate them perfectly |
| **Task Switcher** | Cognitive Flexibility | Adapt as rules change mid-challenge |
| **Clarity Coach** | Verbal Fluency | Speak without filler words |

### 📊 Elo-Based Adaptive System

- **Dynamic Difficulty**: Games adapt to your skill level in real-time
- **Cognitive Score**: Track your progress across all domains (0-100+)
- **Performance Tiers**: Progress from Beginner to Elite

### 🔥 Engagement Features

- **Streak Tracking**: Build daily training habits
- **Session History**: Review past performance
- **Persistent Progress**: Data saved locally

## 🚀 Quick Start

```bash
# Clone the repository
git clone https://github.com/yourusername/mind-games-mvp.git
cd mind-games-mvp

# Install dependencies
npm install

# Start development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to play.

## 🏗️ Project Structure

```
mind-games-mvp/
├── public/
│   └── favicon.svg
├── src/
│   ├── components/
│   │   ├── Hub.jsx          # Main landing page
│   │   └── Icons.jsx        # Custom SVG icons
│   ├── games/
│   │   ├── PatternRecall.jsx
│   │   ├── TaskSwitcher.jsx
│   │   └── ClarityCoach.jsx
│   ├── styles/
│   │   └── index.css
│   ├── utils/
│   │   ├── elo.js           # Elo rating system
│   │   └── storage.js       # LocalStorage utilities
│   ├── App.jsx
│   └── main.jsx
├── index.html
├── package.json
├── vite.config.js
├── tailwind.config.js
└── README.md
```

## 🎯 Game Details

### Pattern Recall
- **Objective**: Memorize and replicate tile sequences
- **Difficulty**: Sequence length increases with success
- **Scoring**: Beat harder sequences for bigger Elo gains

### Task Switcher
- **Objective**: Sort shapes by COLOR or SHAPE based on current rule
- **Challenge**: Rules switch every 4 trials
- **Scoring**: 75%+ accuracy to win each round

### Clarity Coach
- **Objective**: Speak for 30 seconds without filler words
- **Tracked Fillers**: um, uh, like, you know, basically, actually, literally, so, well
- **Scoring**: Less than 5% filler rate with 20+ words to pass

## 📈 The Elo System

The app uses a modified Elo rating system to adapt difficulty:

```javascript
// Expected score based on ratings
expectedScore = 1 / (1 + 10^((challengeRating - playerRating) / 400))

// Rating update after each round
newRating = oldRating + K * (actualResult - expectedScore)
```

- **K-Factor**: 32 (moderate sensitivity)
- **Starting Rating**: 1000
- **Difficulty Rating**: Scales with level (800 + level × 100)

## 🛠️ Built With

- **React 18** - UI framework
- **Vite** - Build tool
- **Tailwind CSS** - Styling
- **Web Speech API** - Speech recognition for Clarity Coach

## 📱 Browser Support

- ✅ Chrome (recommended)
- ✅ Edge
- ✅ Safari
- ⚠️ Firefox (limited Speech API support)

## 🔮 Roadmap

- [ ] Daily Workout mode (mixed game sessions)
- [ ] More game types (Logic Path, Number Memory)
- [ ] Cloud sync with user accounts
- [ ] Leaderboards
- [ ] Weekly challenges
- [ ] Dark/Light theme toggle

## 📄 License

MIT License - feel free to use and modify for your own projects.

---

Built for cognitive enhancement 🧠
