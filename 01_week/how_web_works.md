# How the Web Works

In web development, understanding how the web works is fundamental. Here, we break down the process and concepts into simple terms to help you grasp the basics of web functionality.

## The Web's building blocks

### Client-Server Model
- **Client:** The browser (e.g., Chrome, Firefox) that requests and displays information.
- **Server:** A computer that stores and serves website data to the client.

### HTTP and HTTPS
- **HTTP:** Stands for HyperText Transfer Protocol; facilitates communication between clients and servers.
- **HTTPS:** A secure version of HTTP using encryption to protect data in transit.

### DNS (Domain Name System)
- Translates human-readable web addresses (like `example.com`) into IP addresses (like `192.168.1.1`).
- Acts as the web’s phonebook.

## How It Works: Step-by-Step

1. **You type a URL into your browser.**
   - Example: `www.example.com`

2. **The browser sends a request to a DNS server.**
   - The DNS server finds the IP address of the website.

3. **The browser requests data from the server.**
   - Using HTTP or HTTPS, it asks for the files that make up the website.

4. **The server responds with website files.**
   - Files include HTML (structure), CSS (style), and JavaScript (interactivity).

5. **The browser renders the website.**
   - It processes the files and displays the web page on your screen.

```plaintext
URL -> DNS -> Server -> Response -> Rendering
```

## Key Components of a Web Page

- **HTML:** Defines the structure of the content (e.g., headings, paragraphs, links).
- **CSS:** Styles the page (e.g., colors, fonts, layouts).
- **JavaScript:** Adds interactivity (e.g., animations, form validation).

```html
<!DOCTYPE html>
<html>
<head>
  <title>Example</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <h1>Welcome to the Web</h1>
  <p>This is how it works!</p>
  <script src="script.js"></script>
</body>
</html>
```