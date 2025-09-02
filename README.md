# Stylus CSS script for black background with dim white text for soothing in eyes 
- Install stylus extension and feed this CSS for google AI studio in it
- Works in firefox but not on chrome
- Deactivate extensions like dark reader for google ai studio for this to work 
```
/*
================================================================
  Custom High-Contrast Theme for Google AI Studio
  - Background: Black (#000000)
  - Text: Dim White (#aaaaaa)
================================================================
*/

/* 
 * 1. Universal Selector ("The Big Hammer")
 * This forces the background and text color on almost every element.
 * The `!important` tag is crucial to override the site's existing styles.
*/
* {
    color: #aaaaaa !important;
    background-color: transparent !important;
    border-color: #333333 !important; /* A dark gray for borders so they are still visible */
    background-image: none !important; /* Removes background gradients */
}

/* 
 * 2. Set the main page background
 * This ensures the root of the page is black.
*/
html, body {
    background-color: #000000 !important;
    color: #aaaaaa !important;
}

/*
 * 3. Specific Overrides for UI Elements
 * Some elements need a slightly different background to be usable.
 * We'll make them a very dark gray instead of pure black.
*/
button, 
input, 
textarea, 
select,
div[role="button"],
.mat-mdc-form-field-flex, /* Material Design input container */
.mat-mdc-chip-set, /* Chip container */
.mat-mdc-select-panel, /* Dropdown panel */
.mat-mdc-menu-content {
    background-color: #111111 !important;
    color: #aaaaaa !important;
    border: 1px solid #444444 !important;
}

/* Ensure placeholder text is also visible */
::placeholder {
    color: #666666 !important;
    opacity: 1 !important;
}

/*
 * 4. Links
 * Make sure links are still identifiable.
*/
a {
    color: #cccccc !important; /* A slightly brighter gray for links */
    text-decoration: underline !important;
}

a:hover {
    color: #dddddd !important;
}

/*
 * 5. Icons
 * Material icons sometimes have their own color set.
*/
.material-symbols-outlined, .mat-icon {
    color: #aaaaaa !important;
}

/*
 * 6. Dim Bold Text & Headings
 * Overrides the universal selector for all emphasized text
 * like bold tags and heading tags.
*/
b, strong,
h1, h2, h3, h4, h5, h6,
b *, strong *,
h3 *, h4 *, h5 *, h6 * {
    color: #8d8d8d !important; /* A darker gray for bold/headings */
}

h1 *, h2 * {
    color: #747373 !important; 
}

/*
================================================================
  7. Scrollbar Visibility Fix
  Overrides the universal selector for the custom scrollbar
  elements in Google AI Studio.
================================================================
*/

/* Styles the main vertical line of the scrollbar track */
.scrollbar-line {
    background-color: #333333 !important; /* A dark gray to make it visible */
}

/* Styles the draggable handle of the scrollbar */
.scrollbar-handle {
    background-color: #555555 !important; /* A medium gray for the handle */
    border: 1px solid #777777 !important;
}

/* Styles the small dot indicators on the scrollbar */
.prompt-scrollbar-dot {
    background-color: #aaaaaa !important; /* Use the main text color for visibility */
    border: 1px solid #cccccc !important;
}

/* Styles the active or focused dot indicator */
.ms-button-active .prompt-scrollbar-dot {
    background-color: #ffffff !important; /* Make the active dot white */
    border-color: #ffffff !important;
}
```