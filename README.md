# Welcome Link Banner - Responsive CSS Styles

This README outlines the structure and purpose of the CSS styles for the **Welcome Link Banner** feature. These styles ensure responsiveness and maintain a consistent design across desktop and mobile devices while supporting both light and dark themes.

---

## Features

- **Responsive Design**: Implements flexible layouts and media queries to adapt to different screen sizes, ensuring compatibility across desktops, tablets, and mobile devices.
- **Dark Theme Support**: Utilizes `@media (prefers-color-scheme: dark)` to adjust border colors and other stylistic elements for better usability in dark mode.
- **Interactive Animations**: Hover effects with smooth transitions (`transform` and `box-shadow`) for an engaging user experience.
- **Scalable Components**: Icons and fonts dynamically scale based on screen size for optimal readability and aesthetics.

---

## File Overview

### Common Styles

- **Purpose**: Shared styles across all screen sizes to ensure consistency.
- **Key Elements**:
  - `.featured-banner-link h3`: Sets font size, flex alignment, and spacing for text and icons.
  - `.welcome-wrapper`: Centers the banner, applies consistent padding and margins, and ensures proper box-shadow styling.

### Desktop Styles

- **Breakpoint**: Applied for screens wider than `768px`.
- **Key Elements**:
  - `.welcome-link-banner-wrapper`: Features a gradient background and inset box-shadow for a visually appealing header.
  - `.welcome-link-banner`: Defines structured padding, margin, and hover transitions for smooth animations.
  - `.featured-banner-link`: Implements a horizontal flexbox layout with consistent spacing and alignment.
  - `.btn.close`: Styled with reduced dimensions and hover effects that highlight interactivity.

### Mobile Styles

- **Breakpoint**: Applied for screens `768px` and below.
- **Key Elements**:
  - `.featured-banner-link`: Adjusts to a columnar flexbox layout for better usability on smaller screens.
  - `.btn.close`: Scales down button size and reduces padding to match compact layouts.
  - `.welcome-wrapper`: Ensures visibility or hides content selectively to optimize screen real estate.

### Small Mobile Styles

- **Breakpoint**: Applied for screens `480px` and below.
- **Key Elements**:
  - `.featured-banner-link a h3`: Reduces font size further for better readability on very small screens.
  - `.btn.close`: Minimizes padding and icon dimensions to accommodate limited space.

---

## Media Queries

- **Dark Theme**:
  ```css
  @media (prefers-color-scheme: dark) {
    .welcome-link-banner {
      border: 1px solid #555; /* Dark theme border */
    }
  }
  ```
- **Responsive Breakpoints**:
  - `@media (min-width: 768px)`: Desktop styles.
  - `@media (max-width: 768px)`: Mobile styles.
  - `@media (max-width: 480px)`: Small mobile styles.

---

## Technical Highlights

- **Transition Effects**:
  - Uses `transition: transform 0.3s ease, box-shadow 0.3s ease` for smooth hover effects.
  - Adds depth perception through hover-based `transform` and `box-shadow` properties.

- **Flexbox Utilization**:
  - Leverages `flexbox` for both horizontal and vertical alignment.
  - Responsive layouts achieved by toggling `flex-direction` between `row` and `column`.

- **CSS Variables**:
  - Custom properties like `--secondary` and `--shadow-card` ensure consistent theming across the stylesheets.

- **Icon Styling**:
  - SVG icons are dynamically resized (`width` and `height`) and recolored (`fill`) based on the screen size and context.

---

## Known Issues

- **Alignment on Small Screens**: Ensure `.welcome-wrapper` adapts properly to avoid overlapping content, especially for edge cases on older browsers.
- **Browser Compatibility**: Extensive testing is recommended on legacy browsers to ensure consistent rendering of gradients, shadows, and transitions.

---

## Suggestions for Improvement

- Implement additional accessibility features such as:
  - **ARIA roles**: Add roles and labels for better screen reader support.
  - **Keyboard Navigation**: Ensure focus states and keyboard operability for interactive elements.
- Add more granular breakpoints for improved tablet support.
- Use CSS Grid for enhanced control over layout structure.

---

## Additional Information

This component is specifically designed for the **Welcome Link Banner** in Discourse. It complements the existing functionality described in the official Discourse plugin:

- **Plugin Details**: [Welcome Link Banner on Meta Discourse](https://meta.discourse.org/t/welcome-link-banner/218743)
- **GitHub Repository**: [Discourse Welcome Link Banner](https://github.com/discourse/discourse-welcome-link-banner)

---

## Conclusion

This stylesheet ensures a visually appealing, responsive, and accessible design for the Welcome Link Banner. The current implementation provides a robust foundation, with potential for future enhancements focused on accessibility and cross-browser consistency.

