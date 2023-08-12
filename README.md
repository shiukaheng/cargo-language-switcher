# Usage guide
## Setting up the script
- Copy and paste "page.html" script and CSS snippet to "Design > HTML" section. This should make it work on all pages.
- Make a list of language strings you will use, and choose a default language. In our case, we have "en" and "el". Lets say we want "en" to be the default language. 
- In the script, modify this section to include your languages:
```javascript
    // Define the default and alternate languages
    var defaultLanguage = 'en';
    var allLanguages = [defaultLanguage, 'el'];
```
## Writing multi-lingual pages
Create a new page and write the content as usual. For parts that are language specific, wrap them in a div, and add a class "content-<language>". Any div wrapped in this class will be hidden by default, and is only shown when the language is selected.

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