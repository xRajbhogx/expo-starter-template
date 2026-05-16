# expo-starter

A minimal Expo template to start a new React Native project without any configuration overhead. TypeScript, Expo Router, and a clean folder structure — nothing else.

Use this when you want to build from scratch and add only what you actually need.

---

## What's inside

- Expo SDK 55
- React Native
- TypeScript (strict)
- Expo Router v4 (file-based navigation)
- React Native StyleSheet for styling
- A folder structure ready to scale
- `AGENTS.md` — context file for AI coding assistants (Claude, Cursor, Copilot)
- `.cursor/rules` — Cursor-specific rules for better AI suggestions

No state management, no UI library, no backend. Just a clean starting point.

---

## Requirements

Make sure you have these installed before starting:

- [Node.js](https://nodejs.org/) — v18 or higher
- [Bun](https://bun.sh) — v1.0 or higher
- [Git](https://git-scm.com/)
- **Expo Go for SDK 55** on your phone — download from [expo.dev/go](https://expo.dev/go)

> ⚠️ This project uses Expo SDK 55. The regular Expo Go app from the App Store / Play Store may be on a different SDK version and won't work correctly. Download the right version from the link above.

Install Bun if you don't have it:
```bash
curl -fsSL https://bun.sh/install | bash
```

If you want to run on a simulator:
- **iOS** — Xcode (Mac only)
- **Android** — Android Studio with an emulator set up

---

## Getting started

**1. Use this template**

Click the green **"Use this template"** button on GitHub, give your repo a name, then clone it:

```bash
git clone https://github.com/xRajbhogx/expo-starter-template.git
cd expo-starter-template
```


**2. Install dependencies**

```bash
bun install
```

**3. Start the dev server**

```bash
bunx expo start
```

Scan the QR code with Expo Go on your phone, or press `i` for iOS simulator, `a` for Android emulator.

---

## Folder structure

```
app/
  (auth)/           # Auth screens: sign-in, sign-up
  (tabs)/           # Main tab navigator
  _layout.tsx       # Root layout
  index.tsx         # Entry point — redirects to first screen
components/
  ui/               # Shared components: Button, Card, Input
  [Feature]/        # Feature-specific components
hooks/              # Custom hooks
lib/
  constants.ts      # Colors, spacing, font sizes, route names
  utils.ts          # Helper functions
services/           # API calls and data fetching
assets/
  fonts/
  images/
```

---

## AI-ready out of the box

This template ships with two files that make AI coding assistants significantly more useful:

**`AGENTS.md`** — A context file that tells any AI assistant (Claude, Cursor, Windsurf, Copilot) exactly how this project is structured, what conventions to follow, and what to avoid. Paste it at the start of any AI conversation or let your editor pick it up automatically.

**`.cursor/rules`** — Same context formatted specifically for Cursor. If you use Cursor, this loads automatically and keeps every suggestion consistent with the project's architecture.

Without these, AI assistants make up their own folder structure, naming conventions, and patterns every single session. With them, you get consistent output that actually fits the project from day one.

### Before you start building — update AGENTS.md

Open `AGENTS.md` and fill in the `## Project` section at the top:

```
## Project
Name: Your app name
What it does: One sentence description
Target users: Who is this for
```

Also update the `## Stack` line if you add new libraries (auth, backend, state management, UI library) as the project grows. The more accurate this file is, the better your AI assistant will perform.

---

## TypeScript

The project uses strict TypeScript. Check for errors anytime with:

```bash
bunx tsc --noEmit
```

---

## Building for production

This template uses [EAS Build](https://docs.expo.dev/build/introduction/) for creating production builds.

Install the EAS CLI:

```bash
bun add -g eas-cli
```

Log in and configure:

```bash
eas login
eas build:configure
```

Then build:

```bash
# Android
eas build --platform android

# iOS
eas build --platform ios
```

---

## Adding more

Looking for a version with more already set up?

- **[expo-starter-nativewind] coming soon** — same base with NativeWind (Tailwind for React Native) configured
- **[expo-starter-full] coming soon** — NativeWind + Clerk auth + Zustand + Supabase boilerplates ready to go

---

## Docs

- [Expo SDK 55](https://docs.expo.dev/versions/v55.0.0/)
- [Expo Router](https://docs.expo.dev/router/introduction/)
- [React Native](https://reactnative.dev/docs/getting-started)
- [Bun](https://bun.sh/docs)
- [Expo Go](https://expo.dev/go)
