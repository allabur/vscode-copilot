---
description: "Frontend development guidelines for modern web applications"
applyTo: "**/*.{html,css,scss,jsx,tsx,vue,svelte}"
---

# Frontend Development Instructions

## HTML Best Practices
- Use semantic HTML5 elements (header, nav, main, article, section, footer)
- Implement proper heading hierarchy (h1-h6)
- Use appropriate ARIA labels and roles for accessibility
- Include meta tags for SEO and social sharing
- Optimize images with proper alt text and responsive sizes
- Use proper form validation and user feedback

## CSS and Styling
- Use CSS Grid and Flexbox for modern layouts
- Implement mobile-first responsive design
- Use CSS custom properties (variables) for theming
- Follow BEM or similar naming conventions
- Optimize CSS for performance (minimize reflows/repaints)
- Use CSS preprocessors (Sass/SCSS) for better organization

## Modern JavaScript/TypeScript
- Use ES6+ features and modern syntax
- Implement proper error boundaries and error handling
- Use async/await for asynchronous operations
- Implement proper state management (Redux, Zustand, etc.)
- Use TypeScript for type safety in larger applications
- Optimize bundle size with code splitting and lazy loading

## React Best Practices
- Use functional components with hooks
- Implement proper prop validation with TypeScript or PropTypes
- Use React.memo for performance optimization when needed
- Implement proper key props for lists
- Use custom hooks for reusable logic
- Follow React patterns (compound components, render props, etc.)

## Performance Optimization
- Implement lazy loading for images and components
- Use service workers for caching strategies
- Optimize Core Web Vitals (LCP, FID, CLS)
- Implement proper image optimization and WebP format
- Use CDN for static assets
- Minimize and compress JavaScript and CSS bundles

## Accessibility (a11y)
- Ensure keyboard navigation support
- Implement proper color contrast ratios
- Use ARIA labels and descriptions appropriately
- Test with screen readers
- Implement skip links for navigation
- Ensure focus management in SPAs

## SEO and Meta Data
- Implement proper meta tags for search engines
- Use structured data (JSON-LD) when appropriate
- Optimize page titles and descriptions
- Implement proper URL structure
- Use canonical URLs to prevent duplicate content
- Optimize for social media sharing (Open Graph, Twitter Cards)

## Testing Frontend Applications
- Write unit tests for components and utilities
- Implement integration tests for user workflows
- Use visual regression testing for UI consistency
- Test accessibility with automated tools
- Implement end-to-end testing for critical paths
- Test across different browsers and devices

## Build Tools and Bundling
- Use modern build tools (Vite, Webpack, Rollup)
- Implement proper code splitting strategies
- Optimize for production with minification and compression
- Use proper source maps for debugging
- Implement hot module replacement for development
- Configure proper linting and formatting tools
