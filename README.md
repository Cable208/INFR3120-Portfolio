# INFR3120 Portfolio - Caleb Agyei

Personal Portfolio Website for INFR3120 – Web and Scripting Programming Assignment 1.

## Project Overview

This project is a personal portfolio website created using HTML5 and CSS3.

The purpose of the website is to introduce myself, provide information about my academic and career interests, showcase previous academic and technical projects, and provide a contact form for visitors.

The website contains four separate HTML pages:

- Home
- About Me
- Projects
- Contact Me

The website also uses separate CSS stylesheets for computer, tablet, and mobile screen sizes to create a responsive layout.

---

## Website Pages

### Home Page

The Home page introduces me as an Information Technology student specializing in Networking and IT Security at Ontario Tech University.

It also provides a brief overview of my interests, including:

- Cybersecurity
- Governance, Risk and Compliance
- Cloud technologies
- Basketball
- Cooking
- Music

A link is included on the Home page that allows the user to navigate directly to the Projects page.

---

### About Me Page

The About Me page provides additional information about my background, interests, and career goals.

The page contains:

- A professional headshot
- An HTML5 introduction video
- Video controls
- A poster image displayed before the video begins
- Personal interests
- Career goals

The introduction video is implemented using the HTML5 `<video>` element.

Example:

```html
<video id="about-video"
       controls
       poster="images/video-poster.png">

    <source src="video/Introduction_portfolio.mp4"
            type="video/mp4">

    Your browser does not support the video element.

</video>
```

The `controls` attribute allows the user to play, pause, adjust the volume, and view the video in fullscreen.

The `poster` attribute displays an image before the video begins playing.

---

### Projects Page

The Projects page highlights academic and technical projects I have completed during my studies.

Each project is placed inside an HTML5 `<article>` element so that every project is treated as its own piece of content.

The projects included are:

- CRM API Security Risk Assessment – Informatica Industry Capstone
- AI Fitness Glasses Security Policy
- BooksInc Database Web Application
- Campus Service Robot Feasibility Study
- Security Information and Event Management (SIEM)
- E-commerce Trust System for Fraudulent Returns
- Ontario Tech Trips Cloud Transition with Terraform

Each project contains a project title and a description explaining the project and my contribution.

On computer screens, project cards are displayed in a two-column layout.

On tablet and mobile screens, the cards are displayed one per row to improve readability on smaller displays.

---

### Contact Me Page

The Contact Me page contains an HTML form that allows a visitor to enter contact information and a message.

The form contains the following fields:

- Name
- Email
- Cell Number
- Comments
- Submit button

HTML validation is used to help ensure that users enter valid information.

The `required` attribute is used on each field so that the form cannot be submitted with an empty required field.

The email field uses:

```html
type="email"
```

This allows the browser to perform basic email address validation.

The phone number field uses:

```html
pattern="[0-9]{10}"
```

This requires the user to enter a 10-digit phone number.

---

## HTML5 Semantic Elements

HTML5 semantic elements are used throughout the website to organize the content and improve the structure of the pages.

Semantic elements used include:

- `<header>`
- `<nav>`
- `<main>`
- `<section>`
- `<article>`
- `<footer>`

For example, the `<header>` contains the website title and navigation, while the Projects page uses `<article>` elements for the individual project descriptions.

---

## Responsive Design

The website uses responsive design so that its layout adjusts to different screen sizes.

Three separate CSS stylesheets are used:

- `css/computer.css`
- `css/tablet.css`
- `css/mobile.css`

The appropriate stylesheet is selected using media queries in the `<head>` of each HTML page.

The viewport meta tag is also included on every page:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

This allows the browser to correctly scale the website on smaller devices.

---

### Computer Viewport

Computer screens use:

```text
960px and larger
```

Stylesheet:

```text
css/computer.css
```

Media query:

```html
media="only screen and (min-width: 960px)"
```

The computer layout provides more horizontal space and uses features such as:

- An 80% main content width
- A maximum content width of 1000px
- Two project cards per row
- Larger spacing
- A profile image positioned on the left
- An introduction video positioned on the right

The Projects page uses CSS floats to create the two-column card layout.

Flexbox is not used in the website.

---

### Tablet Viewport

Tablet screens use:

```text
481px to 959px
```

Stylesheet:

```text
css/tablet.css
```

Media query:

```html
media="only screen and (min-width: 481px) and (max-width: 959px)"
```

The tablet layout adjusts the website by:

- Increasing the main content width to 90%
- Reducing navigation spacing
- Reducing the size of the About Me image and video
- Displaying project cards one per row
- Adjusting the contact form width
- Reducing spacing compared with the computer layout

The navigation remains horizontal on tablet screens.

---

### Mobile Viewport

Mobile screens use:

```text
480px and smaller
```

Stylesheet:

```text
css/mobile.css
```

Media query:

```html
media="only screen and (max-width: 480px)"
```

The mobile layout adjusts the website by:

- Using 94% of the available screen width
- Reducing heading and paragraph font sizes
- Reducing navigation spacing
- Keeping the navigation horizontal
- Reducing the About Me image and video size
- Displaying one project card per row
- Allowing the contact form to use the full available width
- Reducing footer text size and spacing

These changes make the website easier to view and navigate on smaller screens.

---

## CSS Box Sizing

The following rule is used in each stylesheet:

```css
* {
    box-sizing: border-box;
}
```

Using `border-box` keeps an element's padding and border inside its assigned width.

This makes it easier to control the size of elements across different screen sizes.

---

## Linear Gradients

The website uses both a standard linear gradient and an angled linear gradient.

### Header Linear Gradient

The website header uses a vertical linear gradient:

```css
background: linear-gradient(
    to bottom,
    #332C29,
    #63483C
);
```

The gradient moves from a darker brown at the top to a lighter brown at the bottom.

The same header gradient is used across the computer, tablet, and mobile stylesheets.

---

### Angled Linear Gradient

The Home page welcome section uses an angled linear gradient:

```css
background: linear-gradient(
    135deg,
    #FFFFFF,
    #a08e85
);
```

The `135deg` value creates a diagonal transition across the Home page welcome section.

This provides visual separation between the welcome content and the rest of the page.

---

## Adobe Color Scheme

Adobe Color was used to help create the primary colour scheme for the portfolio.

The selected Adobe Color palette includes:

- `#FC4D00`
- `#C95928`
- `#96573C`
- `#63483C`
- `#332C29`

These colours are used throughout the website.

### Colour Usage

`#FC4D00`

Used mainly for hover effects such as navigation links and the submit button.

`#C95928`

Used for the contact form submit button and project heading borders.

`#96573C`

Used for form borders and project card borders.

`#63483C`

Used in the header gradient and for project heading text.

`#332C29`

Used as the primary dark colour for text, the header gradient, and the footer background.

Additional neutral colours are also used:

- `#FFFFFF` for content backgrounds
- `#F4F1EF` for the main page background
- `#a08e85` as a lighter neutral brown in the Home page angled gradient

The neutral colours were added to support the main Adobe Color palette and improve readability.

---

## About Me Image and Video Styling

The About Me page changes the size of the profile image and video depending on the viewport.

The CSS `object-fit` property is used to control how the media fits inside the assigned dimensions.

The profile image uses:

```css
object-fit: cover;
```

This allows the image to fill its assigned area without being stretched.

The video uses:

```css
object-fit: contain;
```

This allows the complete portrait video to remain visible without being cropped.

Fullscreen video also uses:

```css
#about-video:fullscreen {
    width: 100%;
    height: 100%;
    object-fit: contain;
    background-color: black;
}
```

This prevents the portrait video from being cropped when viewed in fullscreen.

---

## Project Card Layout

The Projects page uses individually styled project cards.

On computer screens, the cards use:

```css
.project {
    width: 46%;
    float: left;
    margin: 2%;
}
```

This allows two project cards to appear beside each other.

The following selector is also used:

```css
.project:nth-of-type(odd) {
    clear: left;
}
```

This causes each new pair of cards to begin on a new row.

On tablet and mobile screens, the project cards use:

```css
float: none;
```

This changes the layout to one project card per row.

---

## Contact Form Styling

The Contact Me form changes width depending on the screen size.

On computer screens, the form is limited to 60% of the available content width.

On tablet screens, the form uses 90% of the contact section.

On mobile screens, the form uses 100% of the available width.

The form fields use consistent padding, borders, border radius, and font settings throughout the responsive layouts.

The submit button also uses a hover effect to provide visual feedback to the user.

---

## Footer Layout

The footer contains:

- My Ontario Tech email address
- Copyright information

The CSS property:

```css
clear: both;
```

is used on the footer so that it remains underneath floated content such as the project cards.

The main content areas also use a minimum height so that the footer remains near the bottom of pages that contain less content.

---

## External References

### W3Schools HTML Forms

Reference:

https://www.w3schools.com/html/html_forms.asp

This resource was used as a reference when reviewing HTML form structure, form controls, and input elements.

The final Contact Me form was created using standard HTML elements and validation attributes.

---

### W3Schools W3.CSS Cards

Reference:

https://www.w3schools.com/w3css/w3css_cards.asp

This resource was used as a visual reference for the card-style presentation used on the Projects page.

W3.CSS was not imported into the website.

The final project card layout and styling were written using my own CSS.

---
## AI Assistance

ChatGPT was used as a support tool during the development of this portfolio.

Its use was limited mainly to:

- Helping identify and troubleshoot CSS layout issues on the About Me page, particularly with positioning and sizing the profile image and introduction video across different screen sizes.
- Helping explain how CSS properties such as `float`, `object-fit`, sizing, and responsive layout adjustments affected the About Me page.
- Helping me understand how the card-style design shown in the W3Schools W3.CSS Cards reference could be adapted using my own CSS for the Projects page.
- Helping identify HTML/CSS errors and explain why certain layout issues were occurring.

The final HTML and CSS were reviewed, adjusted, and implemented by me, and I ensured that I understood the code used in the website.
---


## Testing and Validation

The website is designed to be tested using the following tools:

### W3C HTML Validator

Used to check the HTML files for syntax, structural, and markup errors.

Pages to validate:

- `index.html`
- `about.html`
- `projects.html`
- `contact.html`

### W3C CSS Validator

Used to check the three CSS stylesheets for CSS syntax errors.

Stylesheets to validate:

- `computer.css`
- `tablet.css`
- `mobile.css`

### W3C Link Checker

Used to confirm that links between the pages of the portfolio work correctly.

Navigation links tested include:

- Home
- About Me
- Projects
- Contact Me

### WAVE Accessibility Evaluation Tool

Used to review the website for accessibility issues.

Accessibility features included in the website include:

- Semantic HTML5 elements
- Alternative text for the profile image
- Form labels connected to form controls
- Clear navigation links
- Structured headings

### Responsive Testing

The website is tested at computer, tablet, and mobile viewport sizes to confirm that:

- Content remains readable
- Navigation remains usable
- Project cards display correctly
- Images and video remain properly sized
- Contact form fields fit within the screen
- The footer remains positioned correctly

### Spelling Review

The visible content and project descriptions are reviewed for spelling and grammar before submission.

---

## Project File Structure

```
INFR3120-Portfolio/
│
├── index.html
├── about.html
├── projects.html
├── contact.html
├── README.md
│
├── css/
│   ├── computer.css
│   ├── tablet.css
│   └── mobile.css
│
├── images/
│   ├── portfolio_headshot.jpeg
│   └── video-poster.png
│
└── video/
    └── Introduction_portfolio.mp4
```

---

## GitHub Repository

The project is stored in a public GitHub repository.

Repository:https://github.com/Cable208/INFR3120-Portfolio



Git was used throughout the development process to track changes to the project.

---

## GitHub Pages Deployment

The completed portfolio website is deployed using GitHub Pages.

Live Website:https://cable208.github.io/INFR3120-Portfolio/



GitHub Pages allows the HTML, CSS, image, and video files stored in the repository to be accessed through a public website.

---

## Author

Caleb Agyei

Bachelor of Information Technology – Networking and IT Security

Ontario Tech University

2026