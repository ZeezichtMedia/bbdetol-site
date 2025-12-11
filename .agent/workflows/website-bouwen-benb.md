---
description: dit is een plan waarmee we een B&B website bouwen.
---

Reusable Implementation Plan: Multilingual Astro Website
This document serves as a "Master Plan" for building a high-performance, 5-page multilingual website using Astro and TailwindCSS. It is designed to be reusable: you can provide this entire document along with specific business details (content, images, branding) to an AI developer to generate a fully functional site.

1. Project Overview
Goal: Build a 5-page responsive website for a B&B/Hotel/Holiday Home.
Languages: 3 (e.g., Dutch, English, German).
Tech Stack:
Framework: Astro (v5+ recommended).
Styling: TailwindCSS.
Language: TypeScript.
Routing/i18n: Built-in astro:i18n.
Icons: lucide-react or astro-icon.
Maps: Google Maps Embed (iframe) or Leaflet (if interactive needed).
Forms: Netlify Forms or simple PHP mailer / API endpoint.
2. Page Architecture
The website consists of the following 5 pages, replicated for each language:

Homepage (/nl, /en, /de)
Root (/): Redirects to /nl (or preferred language).
Hero Section: High-quality background image, welcome title, CTA button ("Book Now").
Introduction: Brief "About Us" text.
Highlights: 3-4 key features (icons + text).
Mini Gallery/Slider: A preview of the best photos (3-5 slides).
Testimonials: (Optional but recommended).
Accommodation (/accommodatie, /en/accommodation, /de/unterkunft)
Detailed description of the rooms/house.
Amenities list (Wifi, Kitchen, etc.).
Pricing/Rates table or info.
"Book Now" CTA.
Surroundings (/omgeving, /en/surroundings, /de/umgebung)
Information about the local area (beach, city, nature).
"Things to do" list.
Photo grid of the surroundings.
Gallery (/gallerij, /en/gallery, /de/galerie)
Full masonry or grid layout of all images.
Lightbox functionality (click to enlarge).
Contact (/contact, /en/contact, /de/kontakt)
Contact details (Address, Phone, Email).
Google Maps Embed: Visual location.
Contact Form: Name, Email, Message.
3. Project Structure
src/
├── assets/             # Local images, fonts
├── components/
│   ├── common/         # Header, Footer, LanguagePicker, SEOHead
│   ├── home/           # Hero, Intro, MiniGallery
│   ├── ui/             # Buttons, Cards, Modal
│   └── ContactForm.astro
├── layouts/
│   └── Layout.astro    # Main html structure with <slot />
├── pages/
│   ├── index.astro     # Redirect to default lang or landing
│   ├── [lang]/
│   │   ├── index.astro
│   │   ├── accommodatie.astro
│   │   ├── omgeving.astro
│   │   ├── gallerij.astro
│   │   └── contact.astro
├── i18n/
│   ├── ui.ts           # UI strings (nav items, buttons)
│   └── utils.ts        # Helper functions for translation
└── styles/
    └── global.css      # Tailwind imports & custom fonts
astro.config.mjs        # i18n configuration
tailwind.config.mjs     # Theme colors & fonts
4. Implementation Steps
Step 1: Setup & Configuration
Initialize Astro project: npm create astro@latest.
Add Tailwind: npx astro add tailwind.
Configure astro.config.mjs for i18n:
export default defineConfig({
  i18n: {
    defaultLocale: "nl",
    locales: ["nl", "en", "de"],
    routing: {
      prefixDefaultLocale: true // Forces /nl for the default language
    }
  }
})
Step 2: Design System & Shared Components
Colors: Define primary (brand), secondary, and accent colors in tailwind.config.mjs.
Typography: Select a header font (e.g., 'Playfair Display') and body font (e.g., 'Inter' or 'Lato').
Layout: Create Layout.astro that handles the <html> lang attribute, <head> metadata, Navbar, and Footer.
Navbar: Responsive menu with Hamburger icon for mobile. Includes LanguagePicker component.
Step 3: Content Strategy (The "Reusable" Part)
To make this plan reusable, we separate content from code.

Create a src/i18n/ui.ts for navigation labels and common UI text (e.g., "Read More", "Send").
For page content, use Astro Content Collections or simple JSON files if the structure is simple.
Example: src/content/pages/nl/home.json, src/content/pages/en/home.json.
Step 4: Page Implementation
Homepage: Implement the Slider using a lightweight library like Embla Carousel or pure CSS scroll snap.
Gallery: Use a CSS Grid for the layout and a simple script for the Lightbox overlay.
Contact: Ensure the form has proper validation and accessible labels.
Step 5: SEO & Performance
Add <meta name="description"> and Open Graph tags in SEOHead.astro.
Use Astro's <Image /> component for automatic optimization.
Ensure 100/100 Lighthouse score by lazy loading off-screen images and the Google Map.
5. Prompt for AI Developer (Copy & Paste this)
Instructions for the AI: Use the plan above to build the website. Here is the specific content for this project:

1. Business Details:

Name: [Business Name, e.g., B&B Zeezicht]
Domain: [e.g., zeezicht.nl]
Colors: [e.g., Navy Blue #0A192F, Gold #D4AF37]
Fonts: [e.g., Headings: Playfair Display, Body: Lato]
2. Languages:

Default: Dutch (nl)
Others: English (en), German (de)
3. Content Brief:

Home: [Intro text...]
Accommodation: [Room details...]
Surroundings: [Area info...]
Contact Info: [Address, Phone, Email]
4. Assets:

Images are located in: [Folder Path] (or use placeholders from Unsplash).
Action: Please generate the full Astro project code following the "Reusable Implementation Plan" structure. Start by setting up the astro.config.mjs and the main Layout.astro.