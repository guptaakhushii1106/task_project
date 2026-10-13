# Product Landing Page — Project Report

**Difficulty Level:** Beginner
**Primary Skills:** HTML, CSS Flexbox, Media Queries, Git
**Dataset Source:** Self-Created Content

---

## 1. Introduction

A landing page is the first page a visitor sees when they arrive at a product's website. Its job is simple: explain what the product is, show why it is useful, and persuade the visitor to take an action such as signing up or buying.

This project builds a modern, responsive **Product Landing Page** using only **HTML** and **CSS**. The layout is handled with **CSS Flexbox**, and the page adapts to different screen sizes with **media queries**. The project is tracked with **Git** and published to **GitHub**.

---

## 2. Problem Statement

Design a landing page for a product that includes:

- A **hero section** that introduces the product
- A **features section** that highlights key benefits
- A **pricing section** that compares plans
- A **call-to-action (CTA) section** that encourages the visitor to act

The page must use Flexbox for alignment and must look good on desktop, tablet, and mobile screens.

---

## 3. Project Objective

The objective of this project is to enable students to:

1. Create a modern product landing page using HTML and CSS.
2. Use Flexbox to align and distribute content in rows and columns.
3. Build reusable UI components such as cards and buttons.
4. Make a layout responsive using media queries.
5. Use Git to track changes and push the project to GitHub.

---

## 4. Design Overview

### 4.1 Purpose and Sections

| Section | Purpose |
|---|---|
| Navbar | Brand name and navigation links |
| Hero | Headline, short description, main button |
| Features | Three cards describing key benefits |
| Pricing | Three plan cards (Basic, Pro, Premium) |
| CTA | Final push to sign up |
| Footer | Copyright and links |

### 4.2 Layout Plan

```
+--------------------------------------+
| Logo                 Home Features...|   <- Navbar (flex, space-between)
+--------------------------------------+
|        Headline + Subtext            |
|          [ Get Started ]             |   <- Hero (flex column, centered)
+--------------------------------------+
|  [Card]     [Card]     [Card]        |   <- Features (flex row, wrap)
+--------------------------------------+
|  [Basic]    [Pro]      [Premium]     |   <- Pricing (flex row, wrap)
+--------------------------------------+
|     Ready to start? [ Join Now ]     |   <- CTA (flex column, centered)
+--------------------------------------+
|              Footer                  |
+--------------------------------------+
```

### 4.3 Colors and Fonts

| Item | Choice |
|---|---|
| Primary color | `#4f46e5` (indigo) |
| Dark text | `#1f2937` |
| Light background | `#f9fafb` |
| Accent / highlight | `#f59e0b` (amber) |
| Font | `Poppins`, with `Arial, sans-serif` as fallback |

### 4.4 Folder Structure

```
product-landing-page/
├── index.html
├── style.css
├── README.md
└── Product_Landing_Page_Report.md
```

---

## 5. Implementation

The project follows the ten required steps.

### Step 1: Create HTML Layout

Create `index.html` with a semantic structure.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>FlowPad – Product Landing Page</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <header class="navbar">...</header>
  <section class="hero">...</section>
  <section class="features" id="features">...</section>
  <section class="pricing" id="pricing">...</section>
  <section class="cta">...</section>
  <footer class="footer">...</footer>

</body>
</html>
```

The `viewport` meta tag is required for media queries to work properly on phones.

### Step 2: Add Hero Section

```html
<section class="hero">
  <h1>Organize Your Work, Effortlessly</h1>
  <p>FlowPad helps you plan tasks, track progress, and stay focused.</p>
  <a href="#pricing" class="btn btn-primary">Get Started</a>
</section>
```

### Step 3: Create Feature Cards

```html
<section class="features" id="features">
  <h2>Features</h2>
  <div class="card-container">
    <div class="card">
      <h3>Easy to Use</h3>
      <p>Clean interface that anyone can learn in minutes.</p>
    </div>
    <div class="card">
      <h3>Fast &amp; Reliable</h3>
      <p>Works smoothly on every device without delays.</p>
    </div>
    <div class="card">
      <h3>Secure</h3>
      <p>Your data stays private and protected.</p>
    </div>
  </div>
</section>
```

### Step 4: Use Flexbox for Alignment

```css
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.card-container {
  display: flex;
  justify-content: center;
  gap: 24px;
  flex-wrap: wrap;
}
```

Key Flexbox properties used:

| Property | Use |
|---|---|
| `display: flex` | Turns a container into a flex container |
| `flex-direction` | Row or column layout |
| `justify-content` | Alignment along the main axis |
| `align-items` | Alignment along the cross axis |
| `gap` | Space between items |
| `flex-wrap` | Lets items move to the next line |
| `flex: 1` | Lets items share space equally |

### Step 5: Design Pricing Section

```html
<section class="pricing" id="pricing">
  <h2>Pricing Plans</h2>
  <div class="pricing-container">
    <div class="plan">
      <h3>Basic</h3>
      <p class="price">$0<span>/month</span></p>
      <ul>
        <li>1 Project</li>
        <li>Basic Support</li>
      </ul>
      <a href="#" class="btn btn-outline">Choose Plan</a>
    </div>

    <div class="plan featured">
      <h3>Pro</h3>
      <p class="price">$12<span>/month</span></p>
      <ul>
        <li>10 Projects</li>
        <li>Priority Support</li>
      </ul>
      <a href="#" class="btn btn-primary">Choose Plan</a>
    </div>

    <div class="plan">
      <h3>Premium</h3>
      <p class="price">$25<span>/month</span></p>
      <ul>
        <li>Unlimited Projects</li>
        <li>24/7 Support</li>
      </ul>
      <a href="#" class="btn btn-outline">Choose Plan</a>
    </div>
  </div>
</section>
```

### Step 6: Add CTA Buttons

```html
<section class="cta">
  <h2>Ready to get started?</h2>
  <p>Join thousands of users who already work smarter.</p>
  <a href="#" class="btn btn-light">Join Now</a>
</section>
```

### Step 7: Style with CSS

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Poppins', Arial, sans-serif;
  color: #1f2937;
  background: #f9fafb;
  line-height: 1.6;
}

.btn {
  display: inline-block;
  padding: 12px 28px;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  transition: transform 0.2s, background 0.2s;
}

.btn:hover { transform: translateY(-2px); }

.btn-primary { background: #4f46e5; color: #fff; }
.btn-outline { border: 2px solid #4f46e5; color: #4f46e5; }
.btn-light   { background: #fff; color: #4f46e5; }

.card, .plan {
  background: #fff;
  padding: 28px;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
}

.cta {
  background: #4f46e5;
  color: #fff;
}
```

### Step 8: Apply Spacing and Alignment

```css
section {
  padding: 80px 24px;
}

.card { flex: 1 1 260px; max-width: 320px; }

.pricing-container {
  display: flex;
  justify-content: center;
  align-items: stretch;
  gap: 24px;
  flex-wrap: wrap;
}

.plan { flex: 1 1 260px; max-width: 320px; text-align: center; }
.plan.featured { border: 2px solid #4f46e5; transform: scale(1.05); }

.cta {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  gap: 16px;
}
```

### Step 9: Make Responsive Using Media Queries

```css
/* Tablet */
@media (max-width: 992px) {
  .hero h1 { font-size: 2.4rem; }
  section { padding: 60px 20px; }
}

/* Mobile */
@media (max-width: 600px) {
  .navbar { flex-direction: column; gap: 12px; }
  .card-container,
  .pricing-container { flex-direction: column; align-items: center; }
  .plan.featured { transform: none; }
  .hero h1 { font-size: 1.8rem; }
}
```

### Step 10: Push Project Using Git

```bash
# Initialize repository
git init

# Stage and commit
git add .
git commit -m "Add HTML structure and hero section"

# Continue committing progress
git add .
git commit -m "Add features, pricing and CTA sections"
git commit -am "Add media queries for responsiveness"

# Connect to GitHub and push
git branch -M main
git remote add origin https://github.com/<your-username>/product-landing-page.git
git push -u origin main
```

Suggested commit history:

1. `Add HTML layout`
2. `Add hero section`
3. `Add feature cards`
4. `Add pricing section and CTA`
5. `Style page with CSS and Flexbox`
6. `Add responsive media queries`

---

## 6. Features

- **Hero section** with a clear headline and a main call-to-action button
- **Feature cards** that align evenly using Flexbox
- **Pricing section** with three plans and a highlighted recommended plan
- **CTA section** with a contrasting background to draw attention
- **Flexbox layout** for navbar, cards, pricing, and CTA alignment
- **Responsive design** for desktop, tablet, and mobile screens
- **Hover effects** on buttons for better interaction
- **Clean, semantic HTML** and organized CSS
- **Version control** with Git and GitHub

---

## 7. Challenges

| Challenge | Solution |
|---|---|
| Cards had different heights | Used `align-items: stretch` on the flex container |
| Cards overflowed on small screens | Added `flex-wrap: wrap` and `flex: 1 1 260px` |
| Navbar looked crowded on mobile | Switched to `flex-direction: column` in a media query |
| Highlighted pricing card broke mobile layout | Removed `transform: scale()` on small screens |
| Spacing was inconsistent | Used `box-sizing: border-box`, `gap`, and consistent section padding |
| Git push was rejected at first | Set the correct remote URL and used `git push -u origin main` |

---

## 8. Output

The final page contains the following sections in order:

1. **Navbar** with the brand name and links
2. **Hero** with headline, description, and "Get Started" button
3. **Features** with three evenly spaced cards
4. **Pricing** with Basic, Pro (highlighted), and Premium plans
5. **CTA** with a "Join Now" button on a colored background
6. **Footer** with copyright text

**Responsive behavior:**

| Screen | Layout |
|---|---|
| Desktop (above 992px) | Cards and pricing plans in a single row |
| Tablet (600px–992px) | Cards wrap onto multiple lines, smaller headings |
| Mobile (below 600px) | Everything stacks in a single column |

> Add screenshots here:
> `![Desktop View](screenshots/desktop.png)`
> `![Mobile View](screenshots/mobile.png)`

**GitHub Repository:** `https://github.com/<your-username>/product-landing-page`

---

## 9. Conclusion

This project showed how a complete, modern landing page can be built with only HTML and CSS. Flexbox made it simple to align the navbar, cards, and pricing plans, and media queries made the page work across screen sizes. Using Git and GitHub added the habit of committing progress and sharing work online.

The project strengthened skills in page structure, component styling, responsive design, and version control. As future improvements, the page could add a hamburger menu, animations, a contact form, and JavaScript interactivity.
