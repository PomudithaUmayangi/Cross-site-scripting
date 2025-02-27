# 🚀 Cross-Site Scripting (XSS) Vulnerability Labs

## 🌟 Welcome to Your XSS Adventure!
Dive into the world of web security with our Cross-Site Scripting (XSS) Vulnerability Labs! This hands-on project is designed to empower you with the knowledge of XSS vulnerabilities, showing you how they work and how to defend against them. Let’s embark on this exciting journey together!

## 📚 What You’ll Learn
- **Understanding XSS**: What it is and why it matters.
- **Types of XSS Vulnerabilities**: Explore the different flavors of XSS.
- **Hands-On Labs**: Get practical experience with real-world examples.

## ❓ What is XSS?
**Cross-Site Scripting (XSS)** is a sneaky security vulnerability that lets attackers inject malicious scripts into web pages. When users visit these compromised pages, the scripts run in their browsers, potentially leading to data breaches and other nefarious activities. Let’s learn how to spot and prevent them!

## 🔍 Types of XSS Vulnerabilities

### 1. 🌐 Reflected XSS
- **How It Works:** The attacker sends a malicious script via a URL, and the server reflects it back without any checks.
- **Example:** If you enter `<script>alert(1)</script>` into a search bar, voilà! An alert box pops up.

### 2. 🗄️ Stored XSS
- **How It Works:** This time, the script is stored on the server (like in a comment section) and runs every time the page is loaded.
- **Example:** Submitting `<script>alert(1)</script>` as a comment means every visitor gets that alert!

### 3. 🏗️ DOM-Based XSS
- **How It Works:** This occurs when client-side scripts manipulate the DOM, allowing for direct execution of injected scripts.
- **Example:** Using `location.search` to pull user input directly into the page can lead to exploits.

## 🛠️ Lab Examples

### Lab 1: 🚨 Reflected XSS
- **Task:** Inject `<script>alert(1)</script>` into a search bar.
- **Outcome:** An alert box will greet you!

### Lab 2: 💾 Stored XSS
- **Task:** Post a comment with `<script>alert(1)</script>`.
- **Outcome:** Every visitor sees the alert when they access the page.

### Lab 3: 🖼️ DOM XSS with `innerHTML`
- **Task:** Try `<img src=1 onerror=alert(1)>`.
- **Outcome:** If the image fails to load, it triggers an alert!

### Lab 4: 🔗 jQuery Anchor Href XSS
- **Task:** Change a link to `javascript:alert(document.cookie)`.
- **Outcome:** Clicking the link reveals your cookies in an alert.

### Lab 5: 🔄 Hash Change Event XSS
- **Task:** Use an iframe with an `onload` attribute like this:
  ```html
  <iframe src="YOUR-LAB-URL" onload="this.src+='<img src=x onerror=print()>'"></iframe>
