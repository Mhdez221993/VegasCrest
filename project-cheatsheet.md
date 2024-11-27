# Quick Reference for Web Development

### Variables

* Define reusable variables for consistency and maintainability.

```CSS
:root {
  --body-bg: #f2f2f2;
  --dark-bg: #333;
  --white: #fff;
  --card-border: #dddddd;
  --button-bg: #ff9800;
  --button-hover: #fcb055;
  --text-color: #000;
  --span-style: italic;
  --card-paragraph-color: #333333;
}
```

### Page Layout with CSS Grid

* Structure the page with a grid layout for better organization.

```CSS
body {
  display: grid;
  grid-template-rows: 80px 1fr 50px; /* Header, main content, footer */
  background-color: var(--body-bg);
  color: var(--card-paragraph-color);
  font-family: sans-serif;
  min-height: 100vh; /* Ensures main content fills the viewport */
}
```

### Responsive Grid System for Cards

* Adapt card layouts to different screen sizes using media queries.

```CSS
.content {
  padding: 10px;
  display: grid;
  grid-template-rows: auto;
  gap: 20px;
}

@media (min-width: 641px) {
  .content {
    grid-template-columns: 1fr 1fr;
  }
}

@media (min-width: 961px) {
  .content {
    grid-template-columns: 1fr 1fr 1fr;
  }
}

@media (min-width: 1281px) {
  .content {
    width: 1281px;
    margin: 0 auto;
    grid-template-columns: 1fr 1fr 1fr 1fr;
  }
}

```

### Card Design

* Style individual cards with a clean and flexible design.

```CSS
.card {
  display: flex;
  flex-direction: column;
  text-align: center;
  padding: 0 0 10px 0;
  background-color: var(--white);
  border: solid 1px var(--card-border);
  border-radius: 0 0 8px 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  overflow: hidden;
}

.card-header { /* Reserves space for the image */
  height: 200px;
  background-color: var(--body-bg);
  margin-bottom: 10px;
}

  #welcome-card {
    grid-area: 1/1/3/3; /* Custom card: occupies a 2x2 area, equivalent to 4 standard grid cells */
  }
```
