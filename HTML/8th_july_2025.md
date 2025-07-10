# Development Diary — `harshdeepportfolio`

This document outlines the development process of a single-page portfolio website created using only HTML and CSS. The project was built by a Computer Science undergraduate student with prior theoretical knowledge of web development and some basic practical experience.

---

## Project Overview

**Objective**  
The goal was to build a clean, modern, and responsive personal portfolio website that showcases:

- A personal introduction
- About Me section
- Technical skills and education
- Projects section
- Contact section with external links
- A personal image

**Technologies Used**  
- HTML5  
- CSS3 (Flexbox, Grid, Media Queries)  
- External resources: Google Fonts, SVG icons

The entire project was developed and completed on **July 7, 2025**.

---

## File Structure

```
/harshdeepportfolio/
├── index.html
├── style.css
├── assets/
│   └── profile.png
└── README.md
```

---

## Design Approach

The primary goal was to build a structured and readable interface with a smooth content flow. The site architecture was kept simple and semantic, ensuring the layout is scalable and understandable.

### Key UI/UX Elements

- **Navigation Bar**: Fixed at the top, with anchor links to each major section. Highlights the active section using CSS.
- **Hero Section**: Includes a greeting, full name, title ("Computer Science Student"), and two action buttons ("View My Work" and "Contact Me").
- **About Section**: Contains a brief background introduction, academic journey, and current focus areas.
- **Skills Section**: Technical skills and education displayed in clean card layouts.
- **Projects Section**: Placeholder cards ready to showcase future project work.
- **Contact Section**: Buttons linking to GitHub, LinkedIn, and email, styled with hover feedback for interactivity.

**Styling Decisions**  
- **Color scheme**: Clean white background with blue and black text
- **Typography**: Bold headings and smooth sans-serif body fonts
- **Layout**: Flexbox and CSS Grid used for positioning
- **Responsiveness**: Mobile-first principles with media queries to adapt layout

---

## Development Process and Challenges

### Initial Setup

- Defined the basic HTML5 boilerplate
- Created `index.html` and `style.css`
- Linked stylesheet and set up font imports
- Structured sections in order of appearance

**Challenge**: Navigation bar overlapping content  
**Solution**: Added padding to the body equal to the navbar height.

```css
body {
  padding-top: 60px;
}
```

---

### Hero Section

This was the first section completed. Centered all content vertically using Flexbox. Included heading text, subtext, and action buttons.

**Challenge**: Buttons wrapping on smaller screens  
**Solution**: Used media queries to stack buttons vertically.

```css
@media (max-width: 600px) {
  .hero-buttons {
    flex-direction: column;
    gap: 12px;
  }
}
```

---

### About Section

Built with two main parts: an image (or placeholder) and text. Highlighted academic background and personal interest in technology.

**Challenge**: Image was not resizing properly  
**Solution**: Applied `max-width` and `object-fit` to ensure scaling.

```css
img {
  max-width: 100%;
  object-fit: cover;
}
```

---

### Skills Section

Skills were listed using a flexible grid layout. Included sections like "Programming", "Web Development", and "Data Structures".

**Approach**: Used reusable card styles with icons and descriptions for clarity.

---

### Projects Section

Created placeholder cards for upcoming project showcases. Each card included a title, short description, and room for links.

**Challenge**: Cards were overflowing and breaking the layout  
**Solution**: Switched to percentage-based width and used `box-sizing: border-box`.

```css
.project-card {
  width: 100%;
  max-width: 300px;
  box-sizing: border-box;
}
```

---

### Contact Section

Included buttons for GitHub, LinkedIn, and email. Styled with simple border and hover transition for interaction.

**Future Idea**: Add a simple contact form using HTML5 or integrate a backend service.

---

## Responsiveness and Testing

Manually tested across devices using browser dev tools. Layout successfully adapted to various screen sizes without breaking content flow.

- Flexbox enabled fluid alignment for section content
- Font sizes were readable across breakpoints
- Buttons maintained spacing and tap areas on touch devices

Basic accessibility considerations were kept in mind (e.g., heading hierarchy, button roles), but additional work such as ARIA roles can be done in future.

---

## Summary of Issues and Fixes

| Issue                          | Cause                              | Fix                                                   |
|-------------------------------|------------------------------------|--------------------------------------------------------|
| Navbar overlapped main content| No space allocated below navbar    | Added padding to `body`                                |
| Buttons breaking layout        | Flexbox without media queries      | Applied mobile-friendly media query styling            |
| Images stretching out of view | Missing constraints on width/fit   | Used `max-width` and `object-fit: cover`               |
| Project cards overflowing      | Fixed width + no box-sizing        | Switched to responsive layout and added `box-sizing`   |

---

## Reflection

This was my first attempt at building a fully structured portfolio site. While I had some foundational knowledge of HTML and CSS from coursework and tutorials, this was my first time applying it to a full webpage.

**What went well**:
- Developed the layout within a single day
- Maintained section consistency and hierarchy
- Ensured a responsive layout across different devices

**Lessons Learned**:
- Planning structure beforehand saves time later
- Small layout bugs are often caused by missing box models or overflow logic
- Responsiveness is best handled by planning from the start (mobile-first)

---

## Future Improvements

- Add downloadable resume link
- Include detailed project cards with demo links
- Add contact form using HTML and connect to a backend (e.g., using Formspree or custom backend)
- Refactor CSS into modular sections or use SCSS for scalability
- Explore hosting options like GitHub Pages

---

**Development completed on: July 7, 2025**
