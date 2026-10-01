Read design/Velour Beauty App v4.dc.html completely — it's a Claude Design export
containing every screen, flow, color, font and component of a mobile app called
Velour Beauty. Grep through it if it's large; do not skip screens.

Build this as a production-quality React Native app with Expo in this directory.

Stack (use the latest stable versions of everything, verify with npm before
installing): Expo SDK (npx create-expo-app@latest, blank TypeScript template),
Expo Router for file-based navigation, TypeScript strict, NativeWind for styling,
expo-image, react-native-reanimated, react-native-gesture-handler, expo-linear-gradient,
expo-font with the fonts from the design, Zustand for state, and mock JSON data
for products/services. Use `npx expo install` for every Expo-managed package so
versions match the SDK.

Rules:

- First list every screen, navigation flow, and design token you found in the
  file, then build. Match the design pixel-for-pixel: exact hex colors, font
  sizes, spacing, radii, shadows, icons, tab bar, headers, cards, buttons, inputs.
- Extract all tokens into a single theme file (constants/theme.ts + tailwind.config).
- Reusable components in /components, screens in /app using Expo Router groups
  (auth, tabs, modals as they appear in the design).
- Every screen must be reachable via real navigation, with working interactions
  (tabs, back, cart/favorites/booking state, forms with validation).
- Handle safe areas, keyboard, loading/empty states, and dark mode if the design
  shows it.
- No placeholder screens, no TODOs. If a screen is in the design, it exists and
  works.
- When done, run `npx expo-doctor` and `npx tsc --noEmit` and fix all issues,
  then give me a screen-by-screen summary of what was built and how to run it
  with `npx expo start`.
