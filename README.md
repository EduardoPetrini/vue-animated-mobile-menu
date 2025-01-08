# Vue Animated Mobile Menu

A responsive and animated header component built with Vue 3, Vite, and Tailwind CSS. The header automatically adapts to different screen sizes, featuring a hamburger menu on mobile devices and a horizontal navigation bar on desktop views.

## Features

- Responsive design with mobile-first approach
- Smooth animations for menu transitions
- Click-outside detection to close mobile menu
- Built with Vue 3 Composition API
- Styled with Tailwind CSS
- Bundled with Vite for optimal development experience

## Tech Stack

- Vue 3.5.13
- Vite 6.0.5
- Tailwind CSS 3.4.17
- PostCSS 8.4.49
- Autoprefixer 10.4.20

## Installation

1. Clone the repository:
```bash
git clone https://github.com/EduardoPetrini/vue-animated-mobile-menu.git
cd vue-animated-mobile-menu
```

2. Install dependencies:
```bash
npm install
```

3. Run the development server:
```bash
npm run dev
```

4. Build for production:
```bash
npm run build
```

## Usage

The header component can be imported and used in any Vue component:

```vue
<script setup>
import Header from './components/Header.vue';
</script>

<template>
  <Header />
</template>
```

### Features Breakdown

#### Desktop View
- Horizontal navigation menu
- Clean, minimal design
- No hamburger menu

#### Mobile View
- Hamburger menu icon
- Animated dropdown menu
- Click-outside detection to close menu
- Staggered animation for menu items
- Smooth transition effects

## Component Structure

The header consists of two main parts:
1. Main header bar with logo/title and navigation
2. Mobile menu that appears when the hamburger icon is clicked

Key classes:
- `md:hidden` / `md:block` for responsive visibility
- `transform` and `transition-all` for smooth animations
- Tailwind utility classes for styling and layout

## Customization

The component can be customized by:
1. Modifying the menu items array in the template
2. Adjusting Tailwind classes for styling
3. Changing transition timings in the duration classes
4. Modifying the animation properties in the style bindings

## License

MIT

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
