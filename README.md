# NovaCSS

NovaCSS is a simple CSS framework that our team created using Sass. The main purpose of this framework is to make website styling easier by providing ready-to-use styles for common HTML elements.

Instead of writing the same CSS again and again, developers can use NovaCSS to style headings, buttons, forms, tables, and other elements. We also included utility classes to make it easier to change colors, text sizes, spacing, and borders.

## Features

Our framework includes:

- Sass files organized into separate partials.
- Variables for changing colors, spacing, and rounded corners.
- Default styling for common HTML elements.
- Utility classes for different styling needs.
- A compiled CSS file that can be used directly in a website.
- Simple instructions for using and customizing the framework.

## Installation

To use NovaCSS, download or clone this repository from GitHub.

Copy the `framework.css` file from the `css` folder into your website project.

Then add this line inside the `<head>` section of your HTML file:

```html
<link rel="stylesheet" href="css/framework.css">
```

Once the CSS file is connected, the framework will automatically apply its default styles to common HTML elements.

## How to Use NovaCSS

NovaCSS includes default styling for:

- Headings (h1 to h6)
- Paragraphs and links
- Ordered and unordered lists
- Buttons
- Forms and input fields
- Tables

We also created utility classes that can be added directly to HTML elements.

For example:

```html
<div class="u-bg-soft u-p-3 u-border u-rounded">
  <h2 class="u-text-brand">Welcome to NovaCSS</h2>
  <p class="u-weight-bold">This is our custom CSS framework.</p>
</div>
```

In this example, the utility classes add a background color, padding, border, rounded corners, and text styling.

## Utility Classes

We created utility classes to make styling easier without writing extra CSS.

### Colors

| Class | Purpose |
|---|---|
| `.u-text-brand` | Applies the main theme color to text |
| `.u-text-dark` | Makes text dark |
| `.u-text-white` | Makes text white |
| `.u-bg-brand` | Applies the main theme background color |
| `.u-bg-soft` | Adds a light background color |

### Font Weight

| Class | Purpose |
|---|---|
| `.u-weight-normal` | Normal text |
| `.u-weight-bold` | Bold text |

### Font Size

| Class | Purpose |
|---|---|
| `.u-text-sm` | Small text |
| `.u-text-md` | Regular text |
| `.u-text-lg` | Large text |

### Margin

We created margin classes from `.u-m-0` to `.u-m-4`.

These classes help control the space outside an element.

### Padding

We created padding classes from `.u-p-0` to `.u-p-4`.

These classes help control the space inside an element.

### Borders

| Class | Purpose |
|---|---|
| `.u-border` | Adds a regular border |
| `.u-border-brand` | Adds a border using the theme color |
| `.u-rounded` | Adds rounded corners |

## Customization

One of the main goals of NovaCSS is to make it easy for developers to change the design.

We used Sass variables to control the main theme color, border radius, and spacing.

These variables are located in:

`scss/_tokens.scss`

For example:

```scss
$brand: #2563eb;
$radius: 0.5rem;
```

Developers can change these values based on the design they want.

We also used a Sass spacing map to create the margin and padding utility classes.

After changing the Sass variables, the CSS file needs to be compiled again.

Developers can also change the theme using CSS custom properties. For example, the following CSS can be added after the NovaCSS stylesheet:

```css
:root {
  --brand: #0f766e;
  --radius: 1rem;
}
```

This changes the main theme color and border radius without editing the Sass files.

## Project Structure

We organized our project into separate files so it is easier to understand and maintain.

```text
novacss-framework/
├── index.html
├── README.md
├── package.json
├── package-lock.json
├── scss/
│   ├── _tokens.scss
│   ├── _base.scss
│   ├── _utilities.scss
│   └── framework.scss
└── css/
    └── framework.css
```

Each Sass file has a different purpose:

- `_tokens.scss` contains the variables used in the framework.
- `_base.scss` contains the default styling for HTML elements.
- `_utilities.scss` contains the reusable utility classes.
- `framework.scss` connects the Sass files together.
- `framework.css` is the compiled CSS file used by the browser.

## Building the Framework

We used Node.js and Sass to compile our framework.

First, make sure Node.js and npm are installed.

Open the project folder in VS Code and run:

```bash
npm ci
```

This installs the packages needed for the project.

To compile the Sass files into CSS, run:

```bash
npm run build
```

This creates or updates the `css/framework.css` file.

To automatically compile the CSS when changes are made, run:

```bash
npm run watch
```

## Testing the Framework

We included an `index.html` page to demonstrate how NovaCSS works.

The page contains different HTML elements, including headings, lists, buttons, forms, inputs, and tables.

It also shows how the utility classes can be used to style different elements.

To view the demo, open `index.html` in a web browser.

## Team Members

This project was completed by three team members:

- **Hardik:** Created the GitHub repository, worked on Sass variables, connected the framework files, and prepared the documentation.
- **Amit:** Worked on the default styling for HTML elements.
- **Jishnu:** Worked on utility classes for colors, fonts, spacing, and borders.

## About This Project

We created NovaCSS as part of our MTM6407 Web Development IV Custom CSS Framework assignment at Algonquin College.

Our goal was to build a small, reusable CSS framework while learning how to organize Sass files, use variables, create utility classes, and work together using GitHub.