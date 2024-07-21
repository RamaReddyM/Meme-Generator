# Meme Generator

## Project Overview

### HTML (`index.html`)

The HTML file sets up the structure and content of the web page:
- **Document Type Declaration (`<!DOCTYPE html>`)**: Defines the document type and version of HTML being used.
- **Meta Tags (`<meta>`)**: Provides metadata about the document (character set, viewport settings).
- **Title (`<title>`)**: Sets the title of the webpage displayed in the browser tab.
- **External Resources (`<link>` and `<script>`)**: Links external CSS (`style.css`) for styling and external JavaScript (`Main.js`) for functionality.
- **Body Content**:
  - **Meme Generator Container (`<div class="meme-generator">`)**: Contains all elements related to the meme generation interface.
  - **Generate Meme Button (`<button class="generate-meme-btn">`)**: Triggers the fetching and display of a new meme.
  - **Meme Details**:
    - **Meme Image (`<img>`)**: Initially empty, it displays the fetched meme image.
    - **Meme Title (`<h2 class="meme-title">`)**: Initially shows "Loading...", updates with the title of the fetched meme.
    - **Meme Author (`<div class="meme-author">`)**: Displays the author information of the meme.

### CSS (`style.css`)

The CSS file defines the visual appearance and layout of the meme generator:
- **Global Reset and Basic Styles**: Resets default margins, paddings, and box-sizing for all elements, sets default font family, background color, and text color for the entire document.
- **Header Styles**: Styles for `.logo-title` include padding, margin, background color, border, font size, and text transformation.
- **Font Awesome Icons**: Customizes Font Awesome icons (`fa-solid` and `fa-regular`) with specific colors.
- **Meme Generator Container Styles (`.meme-generator`)**: Defines a centered container with maximum width, padding, background color, border radius, and box shadow.
- **Meme Image Styles (`.meme-generator img`)**: Ensures the meme image scales to fit its container with rounded corners and a light shadow.
- **Generate Meme Button Styles (`.meme-generator .generate-meme-btn`)**: Styles the button with padding, border, background color, text color, font size, font weight, border radius, cursor style, and hover effects using transitions.
- **Responsive Design (`@media` Queries)**: Adjusts padding and font size within `.meme-generator` for screens narrower than 600px.

### JavaScript (`Main.js`)

JavaScript adds interactivity and functionality to the meme generator:
- **DOM Selection (`document.querySelector()`)**: Retrieves references to HTML elements (`generateMemeBtn`, `memeImage`, `memeTitle`, `memeAuthor`) for manipulation.
- **`updateDetails` Function**: Updates the meme image source (`memeImage`), meme title (`memeTitle innerHTML`), and meme author (`memeAuthor innerHTML`) based on data fetched from the API.
- **`generateMeme` Function**: Uses `fetch` API to asynchronously fetch a random meme from "https://meme-api.com/gimme/wholesomememes". Upon successful retrieval, it calls `updateDetails` to update the displayed meme details.
- **Event Handling (`addEventListener()`)**: Attaches a `click` event listener to `generateMemeBtn`, triggering the `generateMeme` function when the button is clicked.
- **Initial Meme Generation**: Calls `generateMeme()` immediately when the page loads to display an initial meme.

### Summary

The Meme Generator project combines HTML for structure, CSS for styling, and JavaScript for dynamic functionality. It fetches random wholesome memes from an external API, allowing users to generate and view new memes with a single click. The project demonstrates responsive design principles and provides a seamless user experience across different devices.
