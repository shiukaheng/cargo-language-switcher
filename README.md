# Usage guide
Cargo Language Switcher provides an easy solution for adding multi-language support to websites built with Cargo. While Cargo is a versatile website builder, it lacks built-in multi-language features. This tool bridges that gap, enabling designers to cater to a global audience without the technical complexities.
## Setting up the script
- Copy and paste the ["page.html"](https://github.com/shiukaheng/cargo-language-switcher/blob/main/page.html) script and CSS snippet to "Design > HTML" section. This should make it work on all pages.
- Make a list of language strings you will use, and choose a default language. In our case, we have "en" and "el". Lets say we want "en" to be the default language. These language strings are arbritrary, just make sure you are using them consistently.
- In the script, modify this section to include your language string:
```javascript
    // Define the language strings
    var defaultLanguage = 'en'; // The default language shown
    var allLanguages = [defaultLanguage, 'el']; // Add more languages as needed
```
## Writing multi-lingual pages
Create a new page and write the content as usual. For parts that are language specific, wrap them in a div, and add a class "content-\<language string\>". Any div wrapped in this class will be hidden by default, and is only shown when the language is selected.

Example:
```html
<div class="content-en">
    <h1>English content</h1>
</div>
<div class="content-el">
    <h1>Ελληνικό περιεχόμενο</h1>
</div>
```
## Creating a language toggle button
Create an HTML element without text. You can style it however you want. Add an id "language-switcher" to it. This button can then be used to cycle through the languages.

## Behaviour
- When someone first visits your website, they'll see the page in your "default" language (like English or "en"), specified in the top section of the script.
- If they click on the language button, the page will switch to the next available language. The website will remember this choice for their future visits.
- If you've written parts of your page in only one language, remember to put them inside those special boxes (called 'divs'). If you skip this step, the language switch button can't change those parts.
- On pages with the address containing 'cargo.site/admin', the language button won't work. This is to keep things safe and unchanged on those pages.
