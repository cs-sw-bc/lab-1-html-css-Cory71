### **Step 9 – Open Your Project Locally**

To view your project in a web browser, follow these steps:
1. Open Visual Studio Code.
2. Navigate to your project folder.
3. Right-click on `index.html` and select "Open with Live Server" or open it directly in your browser.

Quick Start (Windows PowerShell):

```powershell
# from the project root open the main page in your default browser
Start-Process index.html
```

If you received a motorcycle image as an attachment and want it shown on the homepage, run this (adjust the source filename):

```powershell
# copy the image from your Downloads to the repo images folder and name it motorcycle-real.png
Copy-Item -Path "$env:USERPROFILE\Downloads\<your-file-name>.png" -Destination "$(Resolve-Path .)\images\motorcycle-real.png"
```

Optimizing images (optional)

If you have ImageMagick installed, generate optimized PNG and WebP sizes used by the site with these commands (run from the repo root):

```powershell
# 800px wide optimized PNG and WebP
magick convert images\motorcycle-real.png -resize 800 -quality 85 images\motorcycle-real-800.png
magick convert images\motorcycle-real.png -resize 800 -quality 80 images\motorcycle-real-800.webp

# 400px wide optimized PNG and WebP
magick convert images\motorcycle-real.png -resize 400 -quality 85 images\motorcycle-real-400.png
magick convert images\motorcycle-real.png -resize 400 -quality 80 images\motorcycle-real-400.webp

# larger size for featured view (1200px)
magick convert images\motorcycle-real.png -resize 1200 -quality 85 images\motorcycle-real-1200.png
magick convert images\motorcycle-real.png -resize 1200 -quality 80 images\motorcycle-real-1200.webp
```

Files added in this demo:
- `index.html` — home page with links to Cars and Motorcycles pages
- `cars.html` — short page about cars
- `motorcycles.html` — short page about motorcycles
- `css/styles.css` — styling for the site
- `images/README.txt` — placeholder instructions for adding images
# 🧪 Lab 1: Building a Responsive Website with AI

**Duration:** 2 hours 30 minutes  
**Tools:** ChatGPT (free version) or GitHub Copilot, Visual Studio Code, Bootstrap, and Chrome/Edge  

---

## 🎯 Learning Objectives

By the end of this lab, you will be able to:

- Build a **multi-page responsive website** (for products or services) using HTML, CSS, and Bootstrap  
- Apply a consistent **color scheme** based on color harmony principles  
- Use **AI tools responsibly** to assist your coding process while understanding each line of code  

---

## 🧱 Lab Overview

In this lab, you’ll design a small business website — it could be for **products** (e.g., handmade candles, gadgets, books) or **services** (e.g., photography, web design, yoga classes).  
You’ll use **AI tools** like ChatGPT or GitHub Copilot to assist you, but the focus is on understanding and modifying the generated code to fit your creative vision.

You will:
1. Plan the concept and structure of your website  
2. Build each page with AI assistance, step-by-step  
3. Choose and apply a professional color scheme  
4. Make your website responsive using Bootstrap  

---

## Step-by-Step Instructions

### **Step 1 – Project Setup**

1. Create a new folder named `MyWebsite`.  
2. Inside it, create:
   - `index.html` (Home page)
   - `about.html`
   - `products.html` or `services.html` (depending on your theme)
   - A folder named `items` containing individual pages for each product or service (`item1.html`, `item2.html`, etc.)
   - A `css` folder with a `style.css` file

💡 **Decide on your business theme:**
Before coding, choose what your website is about.

Examples:
- A bakery showcasing cakes and pastries 🍰  
- A photography service portfolio 📸  
- A handmade crafts store 🧵  
- A fitness trainer offering programs 💪  

This will guide your content, images, and page structure.

---

### **Step 2 – Choose Your Website’s Color Scheme**

Before you begin designing, decide on the color harmony you’ll use.

1. Learn about color schemes here:
   - [W3Schools: Color Schemes](https://www.w3schools.com/colors/colors_schemes.asp)
   - [Canva Color Wheel](https://www.canva.com/colors/color-wheel/)
2. Experiment with:
   - **Monochromatic** (one hue, different shades)
   - **Analogous** (colors next to each other on the wheel)
   - **Complementary** (opposite colors)
   - **Triadic** (three evenly spaced colors)
3. Choose 3–4 main colors: background, text, accent, and highlight.  
4. Write down their **hex codes** — you’ll use them in your CSS file.

---

### **Step 3 – Build the Home Page**

Use ChatGPT or Copilot to generate small sections at a time:
- A **navigation bar** linking to Home, About, and Products/Services  
- A **hero section** introducing your business  
- A **footer** with contact or copyright info  

🧠 **Important:**
After AI generates code, **read and understand every line**.  
If something doesn’t make sense, ask:
> “Explain what this Bootstrap class does”  
> “What does this `<div>` structure achieve?”  

You’re not just copying — you’re learning how the website works.

---

### **Step 4 – About Page**

Build an About page describing:
- Who you or your company is  
- What values or goals drive the business  
- Optionally include a photo or logo  

Use AI to structure the layout. This page can be made responsive too !

---

### **Step 5 – Products or Services Page**

1. Create a **Bootstrap card grid layout** that showcases all your products or services.
2. Refer to Unit 1 - lesson 6 for reference. This can guide your interaction and requests to your AI assistant.
3. Each card should include:
   - Image  
   - Short description  
   - Button/Link that says **“Learn More”** linking to the individual item page  

---

### **Step 6 – Individual Item Pages**

In the `items` folder:
- Create separate pages like `item1.html`, `item2.html`, etc.  

Each page should contain:
- Title and description  
- Image or gallery  
- Price, features, or benefits  
- Link to go back to the Products/Services page  

---

### **Step 7 – Make It Responsive**

1. Use Bootstrap’s **grid system** (`container`, `row`, `col-*`) to make layouts flexible.  
2. Add **media queries** in your `style.css` for small refinements.  
3. Test your website at different screen sizes (mobile, tablet, desktop).

---

### **Step 8 – Apply Your Color Scheme**

1. Open `style.css` and apply the colors you selected earlier.
2. Alternately, you can ask your CoPilot/AI to do this job for you. Add in the color codes you copied earlier and ask your AI to integrate it into your website.
3. Keep refining until you are happy and prooud of your website.
