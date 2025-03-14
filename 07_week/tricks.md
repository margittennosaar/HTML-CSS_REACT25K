# Essential tips & tricks for webpages

Here’s a collection of **beginner-friendly** JavaScript tricks that will make your webpage **interactive, responsive, and user-friendly**. These are some of the most **common** features used in modern websites.

## **Mobile menu (hamburger menu)**
Toggle a mobile menu with a button click.

**HTML**
```html
<button id="menu-toggle" aria-expanded="false">☰ Menu</button>
<nav id="menu" class="mobile-menu">
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Services</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
```

**JavaScript**
```js
const menuToggle = document.querySelector("#menu-toggle");
const menu = document.querySelector("#menu");

menuToggle.addEventListener("click", () => {
  menu.classList.toggle("active");
  menuToggle.setAttribute("aria-expanded", menu.classList.contains("active"));
});

document.addEventListener("click", (event) => {
  if (!menu.contains(event.target) && !menuToggle.contains(event.target)) {
    menu.classList.remove("active");
    menuToggle.setAttribute("aria-expanded", "false");
  }
});
```

**CSS**
```css
.mobile-menu {
  display: none;
}
.mobile-menu.active {
  display: block;
}
```

## Back-to-Top Button
A button that appears when scrolling down and smoothly scrolls to the top.

**HTML**
```html
<button id="back-to-top">Back to Top</button>
```

**JavaScript**
```js
const backToTop = document.querySelector("#back-to-top");

window.addEventListener("scroll", () => {
  backToTop.style.display = window.scrollY > 300 ? "block" : "none";
});

backToTop.addEventListener("click", () => {
  window.scrollTo({ top: 0, behavior: "smooth" });
});
```

## Modal Window
Opens a popup/modal and closes when clicking outside or pressing `Esc`.

**HTML**
```html
<button id="open-modal">Open Modal</button>
<div id="modal" class="modal">
  <div class="modal-content">
    <button id="close-modal">Close</button>
    <h2>Modal Window</h2>
    <p>This is a simple modal.</p>
  </div>
</div>
```

**JavaScript**
```js
const modal = document.querySelector("#modal");
const openModal = document.querySelector("#open-modal");
const closeModal = document.querySelector("#close-modal");

openModal.addEventListener("click", () => modal.classList.add("show"));
closeModal.addEventListener("click", () => modal.classList.remove("show"));

document.addEventListener("keydown", (e) => {
  if (e.key === "Escape") modal.classList.remove("show");
});
```

## Dark Mode Toggle
Switch between light and dark mode and save the setting in local storage.

```html
<button id="theme-toggle">Toggle Dark Mode</button>
```


**JavaScript**
```js
const themeToggle = document.querySelector("#theme-toggle");
themeToggle.addEventListener("click", () => {
  document.body.classList.toggle("dark-mode");
  localStorage.setItem("theme", document.body.classList.contains("dark-mode") ? "dark" : "light");
});

if (localStorage.getItem("theme") === "dark") {
  document.body.classList.add("dark-mode");
}
```

```css
body {
  background-color: #ffffff;
  color: #000000;
  transition: background-color 0.3s ease, color 0.3s ease;
}

.dark-mode {
  background-color: #121212;
  color: #ffffff;
}
```

## Copy to clipboard
Copy text from an element to the clipboard.

**HTML**
```html
<p id="copyText">This is some text to copy.</p>
<button id="copyBtn">Copy</button>
```

**JavaScript**
```js
document.querySelector("#copyBtn").addEventListener("click", () => {
  const text = document.querySelector("#copyText").textContent;
  navigator.clipboard.writeText(text);
});
```

## Expand/Collapse FAQ Section
Click a question to expand/collapse the answer.

**JavaScript**
```js
document.querySelectorAll(".faq-question").forEach(item => {
  item.addEventListener("click", () => {
    item.nextElementSibling.classList.toggle("visible");
  });
});
```

## Typing Effect
Creates a typing animation.

**JavaScript**
```js
const text = "Hello, World!";
let i = 0;
function typeEffect() {
  if (i < text.length) {
    document.querySelector("#typing").textContent += text.charAt(i);
    i++;
    setTimeout(typeEffect, 100);
  }
}
typeEffect();
```

