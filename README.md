# Linkedin-Feedblocker
Linkedin Feed blocker 2023

🚫 Tired of your LinkedIn feed constantly demanding your attention? So was I! As a solution, I created a script to hide the LinkedIn feed. Why? Because available Chrome plugins just weren't up to the task anymore. Want to reclaim your focus and headspace? Here's how:

Install the Tampermonkey Chrome Extension - it's a user-friendly interface to manage user scripts.

Click on the Tampermonkey extension icon and select "Create a new script" - this will open up a platform for you to customize your browsing experience.

In the editor, replace the existing content with my user script below. Easy, right?


I built this script because the mental clutter that comes with an overactive feed can be quite distracting. I hope it helps you as much as it's helped me.

Give it a try and let me know your thoughts. Does it make your LinkedIn experience smoother?

#linkedin #productivity #tampermonkey

Curious to hear your feedback, let me know if it works for you. 👇👇

```
// ==UserScript==
// @name    Hide Element
// @version 1
// @grant   none
// @match   https://targetwebsite.com/*

// ==/UserScript==
var observer = new MutationObserver(function(mutations) {
   var elements = document.querySelectorAll('[aria-label="Main Feed"]');
   for (var i = 0; i < elements.length; i++) {
       if(elements[i].classList.contains('scaffold-layout__main')){
           elements[i].style.display = 'none';
       }
   }
});

observer.observe(document, { attributes: true, childList: true, subtree: true });
```


