# Quick Start Guide - Get Building in 30 Minutes

**Goal:** Go from nothing to a working development environment where you can start building.

---

## Prerequisites Check (5 minutes)

Before you start, verify you have:

### Required
- [ ] A computer (Mac, Windows, or Linux)
- [ ] Internet connection
- [ ] GitHub account (create at github.com if needed)
- [ ] Claude API key (get at console.anthropic.com)

### Will Install
- [ ] Git
- [ ] Node.js 18+
- [ ] VS Code (or your preferred editor)

---

## Step 1: Install Development Tools (10 minutes)

### Install Git

**Mac:**
```bash
# Check if already installed
git --version

# If not installed, install via Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew install git
```

**Windows:**
1. Download from: https://git-scm.com/download/win
2. Run installer with default options
3. Verify: Open Command Prompt, type `git --version`

**Linux:**
```bash
sudo apt-get update
sudo apt-get install git
```

### Install Node.js

**All Platforms:**
1. Go to: https://nodejs.org/
2. Download LTS version (left button)
3. Run installer with default options
4. Verify: Open terminal/command prompt
   ```bash
   node --version  # Should show v18 or higher
   npm --version   # Should show 9 or higher
   ```

### Install VS Code (Recommended)

1. Go to: https://code.visualstudio.com/
2. Download for your platform
3. Install with default options
4. Launch VS Code

**Recommended Extensions:**
- Open VS Code
- Click Extensions icon (left sidebar)
- Search and install:
  - "ESLint"
  - "Prettier"
  - "Tailwind CSS IntelliSense"

---

## Step 2: Set Up GitHub Repository (10 minutes)

### Create Repository on GitHub

1. Go to: https://github.com/new
2. Repository name: `personal-cos`
3. Description: "AI-powered personal chief of staff"
4. Set to: **Public** (or Private if you prefer)
5. ✅ Initialize with README
6. Add .gitignore: **Node**
7. License: **MIT** (recommended)
8. Click **Create repository**

### Clone to Your Computer

1. On your new repo page, click green **Code** button
2. Copy the HTTPS URL (should look like: `https://github.com/YOUR_USERNAME/personal-cos.git`)
3. Open terminal/command prompt
4. Navigate to where you want the project:
   ```bash
   cd ~/Documents  # Mac/Linux
   cd C:\Users\YourName\Documents  # Windows
   ```
5. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/personal-cos.git
   cd personal-cos
   ```

---

## Step 3: Initialize React Project (5 minutes)

### Create Vite Project

```bash
# Inside your personal-cos directory
npm create vite@latest . -- --template react

# Install dependencies
npm install

# Install additional packages we'll need
npm install @anthropic-ai/sdk date-fns lucide-react

# Install Tailwind CSS
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

### Configure Tailwind

1. Open `tailwind.config.js` and replace contents with:
```javascript
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

2. Open `src/index.css` and replace contents with:
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### Test It Works

```bash
npm run dev
```

You should see:
```
VITE v5.x.x  ready in xxx ms

➜  Local:   http://localhost:5173/
```

Open browser to http://localhost:5173/ - you should see Vite + React logo!

Press `Ctrl+C` in terminal to stop the server.

---

## Step 4: Set Up Environment (5 minutes)

### Create Environment Files

1. Create `.env.example` in project root:
```
# Claude API Configuration
VITE_ANTHROPIC_API_KEY=your_api_key_here

# App Configuration
VITE_APP_NAME="Personal CoS"
VITE_APP_VERSION="0.1.0"
```

2. Create `.env.local` in project root:
```
# Get your API key from: https://console.anthropic.com/
VITE_ANTHROPIC_API_KEY=sk-ant-api03-...your-actual-key...
```

3. Verify `.env.local` is in `.gitignore` (it should be already)

### Get Your Claude API Key

1. Go to: https://console.anthropic.com/
2. Sign up or log in
3. Go to: API Keys (in sidebar)
4. Click **Create Key**
5. Copy the key (starts with `sk-ant-api03-`)
6. Paste into `.env.local` file

---

## Step 5: Create Initial Project Structure (3 minutes)

### Create Directories

```bash
# In project root
mkdir -p src/components src/lib src/hooks docs
```

### Create First Component

Create `src/components/CheckIn.jsx`:
```jsx
export default function CheckIn() {
  return (
    <div className="p-6 max-w-2xl mx-auto">
      <h1 className="text-3xl font-bold mb-4">Morning Check-In</h1>
      <p className="text-gray-600">
        Your personal Chief of Staff is ready to help you plan your day.
      </p>
    </div>
  );
}
```

### Update App Component

Replace `src/App.jsx` with:
```jsx
import CheckIn from './components/CheckIn';

function App() {
  return (
    <div className="min-h-screen bg-gray-50">
      <CheckIn />
    </div>
  );
}

export default App;
```

### Test Again

```bash
npm run dev
```

Visit http://localhost:5173/ - you should see "Morning Check-In" heading!

---

## Step 6: Commit Your Work (2 minutes)

```bash
# Stage all files
git add .

# Commit
git commit -m "Initial project setup with Vite, React, and Tailwind"

# Push to GitHub
git push origin main
```

Visit your GitHub repo - you should see your code there!

---

## You're Ready! 🎉

You now have:
- ✅ Git installed and configured
- ✅ Node.js and npm working
- ✅ VS Code set up with extensions
- ✅ GitHub repository created
- ✅ React + Vite project initialized
- ✅ Tailwind CSS configured
- ✅ Claude API key ready
- ✅ First component working
- ✅ Code committed to GitHub

---

## Next Steps

### Option A: Build MVP with Claude Artifacts (Recommended)

1. Open Claude (claude.ai)
2. Start a conversation: "I want to build an MVP artifact of the Personal CoS morning check-in flow. Let's start with a simple form that collects user's priorities for the day."
3. Iterate on the artifact until it works
4. Then convert artifact code to your React project

### Option B: Start Building Directly

1. Read the Development_Plan.md for full roadmap
2. Start with onboarding flow
3. Build incrementally
4. Test often

### Option C: Work Through Tutorial

Create `docs/TUTORIAL.md` and start with basics:
- How to create a new component
- How to add state
- How to call Claude API
- How to persist data to localStorage

---

## Troubleshooting

### "npm: command not found"
- Node.js not installed correctly
- Restart terminal after installing Node.js
- Check PATH environment variable

### "git: command not found"
- Git not installed correctly
- Restart terminal after installing Git
- On Windows: make sure to use Git Bash or add Git to PATH

### "Permission denied" errors
- On Mac/Linux: might need `sudo` for some commands
- Or use `nvm` (Node Version Manager) instead

### Vite won't start
- Check port 5173 isn't already in use
- Try `npm run dev -- --port 3000` to use different port

### Can't see Tailwind styles
- Make sure `tailwind.config.js` content array includes your files
- Make sure `index.css` has @tailwind directives
- Restart dev server after Tailwind config changes

---

## Quick Reference Commands

### Development
```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run preview      # Preview production build
```

### Git
```bash
git status           # See what's changed
git add .            # Stage all changes
git commit -m "msg"  # Commit with message
git push             # Push to GitHub
git pull             # Pull latest from GitHub
```

### Troubleshooting
```bash
npm install          # Reinstall dependencies
rm -rf node_modules  # Delete node_modules
npm install          # Fresh install
```

---

## Getting Help

1. **Claude** - Ask me anything about the code!
2. **GitHub Issues** - Check if others had same problem
3. **Documentation**:
   - Vite: https://vitejs.dev/
   - React: https://react.dev/
   - Tailwind: https://tailwindcss.com/
4. **Stack Overflow** - Search for error messages

---

## Time Check

If you followed this guide, you should have spent:
- ✅ 5 min: Prerequisites check
- ✅ 10 min: Install tools
- ✅ 10 min: GitHub setup
- ✅ 5 min: React project
- ✅ 5 min: Environment setup
- ✅ 3 min: Project structure
- ✅ 2 min: First commit

**Total: ~40 minutes**

You're now ready to start building your Personal Chief of Staff application!

**Celebrate this milestone** - you've gone from zero to a working development environment. That's the hardest part for many people. Everything from here is incremental progress.

Now go build something amazing! 🚀
