# TwendeRide - Setup Guide for IDE Development

## Prerequisites

- Node.js 18.x or later
- npm 9.x or later
- Expo CLI
- Git

## Quick Start

1. **Clone and install dependencies:**
   ```bash
   git clone <repository-url>
   cd twenderide
   npm install --legacy-peer-deps
   ```

2. **Configure environment variables:**
   ```bash
   cp .env.example .env
   ```
   
   Fill in the required environment variables in `.env`:
   
   ```env
   # Clerk Authentication
   EXPO_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_key_here
   
   # Database (Neon)
   DATABASE_URL=your_neon_database_url_here
   
   # Stripe Payment
   STRIPE_SECRET_KEY=your_stripe_secret_key_here
   EXPO_PUBLIC_STRIPE_PUBLISHABLE_KEY=your_stripe_publishable_key_here
   
   # Google Maps & Places
   EXPO_PUBLIC_GOOGLE_API_KEY=your_google_api_key_here
   EXPO_PUBLIC_DIRECTIONS_API_KEY=your_google_directions_api_key_here
   EXPO_PUBLIC_PLACES_API_KEY=your_google_places_api_key_here
   
   # Geoapify (for map images)
   EXPO_PUBLIC_GEOAPIFY_API_KEY=your_geoapify_api_key_here
   ```

3. **Start the development server:**
   ```bash
   npm start
   ```

## IDE Setup

### VS Code Recommended Extensions

- ES7+ React/Redux/React-Native snippets
- Expo Tools
- TypeScript and JavaScript Language Features
- Prettier - Code formatter
- ESLint

### Development Scripts

- `npm start` - Start Expo development server
- `npm run android` - Start on Android emulator
- `npm run ios` - Start on iOS simulator
- `npm run web` - Start web version
- `npm test` - Run tests
- `npm run lint` - Run ESLint

## Project Structure

```
/app                 # Expo Router app directory
  /(api)            # API routes
  /(auth)           # Authentication screens
  /(root)           # Main app screens
/components         # Reusable components
/lib               # Utility functions
/store             # Zustand state management
/assets            # Static assets (fonts, images, icons)
/constants         # App constants
/types             # TypeScript type definitions
```

## Key Technologies

- **React Native** 0.79.5 with **React** 19.0.0
- **Expo** 53.x with Expo Router for navigation
- **TypeScript** for type safety
- **NativeWind** (Tailwind CSS for React Native)
- **Clerk** for authentication
- **Stripe** for payments
- **Neon** database with Drizzle ORM
- **Zustand** for state management
- **React Native Maps** for mapping functionality

## Troubleshooting

### Common Issues

1. **Metro bundler issues:** Clear cache with `npx expo start --clear`
2. **Node modules issues:** Delete `node_modules` and run `npm install --legacy-peer-deps`
3. **Type errors:** Run `npx tsc --noEmit` to check TypeScript issues

### Environment Variables

The app requires several API keys to function properly:
- Clerk for authentication
- Stripe for payments
- Google Maps API for maps and places
- Geoapify for map images
- Neon database for data storage

Make sure all required environment variables are set before running the app.

## Ready for Development

The app is now configured and ready for development in your IDE! 🚀