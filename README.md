🎨 Color Clubs: The Immersive Palette Explorer
Color Clubs is a feature-rich, single-file React application designed to revolutionize how developers and designers discover, save, and create color palettes.

Instead of treating colors as simple utility data, this application presents palettes as curated products. Using an "editorial brutalist" design system—characterized by heavy typography, stark black-and-white UI elements, and sharp squircles—the interface acts as a neutral frame that allows the vibrant, user-generated color palettes to command the visual hierarchy.

Built entirely without a build step (no Webpack, no Vite, no Node.js required locally), it leverages React via CDN, in-browser Babel transpilation, and a Supabase backend to deliver a blazing-fast, highly interactive experience directly from a single index.html file.

🚀 Core Features & Architecture
1. The "E-Commerce" Discovery Engine
The Explore page functions like a high-end storefront for colors. Users can sift through the database using a robust, multi-layered filtering system:

Color Match Panel: Users can interact with a custom-built HSL/RGB spectrum or pick from curated swatches to filter the gallery, returning only palettes that contain closely matching hex codes.

Tag & Theme Routing: A smart search bar that auto-suggests themes (e.g., "cyber", "vintage", "warm") and specific colors, rendering them as filterable chips.

Property Sorting: Instantly filter palettes by their exact color count or sort the gallery by Newest, Most Popular, or Random.

2. Dynamic Theming & Immersion
Clicking a palette doesn't just open a modal; it transforms the entire application.

Contextual UI: The application reads the selected palette's colors and dynamically injects them into the global CSS, altering the background gradients and UI borders.

Smart Contrast: The app calculates the luminosity of the dominant background color and automatically switches text and UI elements between pure black and stark white to ensure WCAG-compliant readability.

Recommendation Engine: A "Similar Vibes" algorithm analyzes the active palette's themes and suggests related color clubs at the bottom of the page.

3. The Palette Palace (Local Storage Cart)
We replaced the standard "Favorites" list with the Palette Palace—a slide-out drawer that acts as a shopping cart for designers. Palettes are seamlessly saved to the browser's localStorage, allowing users to build a personal mood board that persists across sessions.

4. The Creator Studio & Generator
A built-in studio allows users to contribute to the Supabase database.

Smart Generator: Users can randomly generate hex codes, lock their favorite colors in place, and reroll the rest until they find the perfect combination.

Custom Builder: A custom-built mini color picker allows users to manually dial in HSL values, name their palette, and submit it directly to the live PostgreSQL database.

Auto-Theming: When a user creates a new palette, a custom algorithm analyzes the HSL values and luminosity to automatically assign relevant tags (e.g., categorizing high-saturation/mid-luminosity colors as "neon" or low-saturation colors as "minimal").
