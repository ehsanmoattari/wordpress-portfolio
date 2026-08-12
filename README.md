# 🚀 WordPress Portfolio Pipeline
### Build & Deploy Instant Live Demos

[![WordPress Playground](https://img.shields.io/badge/WordPress-Playground-blue?logo=wordpress)](https://playground.wordpress.net/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## 📌 About This Project

This repository is the **core engine** of a professional pipeline for creating instant, live, and fully functional WordPress demos. 

The goal is to **eliminate the gap between design and a live website**. With a single click, this pipeline generates a complete, interactive demo site. No hosting, no setup, no waiting.

**Why this matters:**
- **For Agencies & Freelancers:** Showcase your work with zero friction.
- **For Clients:** Experience your future website instantly, not through screenshots or PDFs.
- **For Developers:** A modular, reusable blueprint that saves hours of repetitive setup.

---

## ✨ Key Features

- **⚡ Instant Live Demos:** Uses [WordPress Playground](https://playground.wordpress.net/) to spin up a fully functional WordPress site in seconds.
- **🧩 Modular Blueprint:** A single `blueprint.json` file controls the entire setup process.
- **🎨 Pre-configured Stack:** Comes with Kadence Theme, Kadence Blocks pre-installed.
- **🎯 Customizable for Each Client:** Easily change the site name, content, and images via simple URL parameters.
- **📂 Organized Assets:** All plugins, themes, and media are stored locally in the repository for maximum speed and reliability.

---

## 📂 Repository Structure

```
wordpress-portfolio/
├── blueprint.json # Master Blueprint (the core of the pipeline)
├── README.md # This file
├── index.html # Optional landing page for your portfolio
├── themes/ # Theme ZIP files (local installation for speed)
│ └── kadence.zip
├── plugins/ # Plugin ZIP files (local installation)
│ ├── kadence-blocks.zip
│ ├── advanced-custom-fields.zip
│ └── bookingpress.zip
└── my-portfolio/ # Dedicated projects for each client demo
├── sample-content.xml # Default WXR content (services, pages, etc.)
├── salon-dubai/ # Example project folder
│ ├── content.xml # Custom content for this project
│ └── media/ # Project-specific images
│ ├── logo.png
│ └── gallery/
└── salon-london/ # Another example project
├── content.xml
└── media/

```

## 🚀 How to Use This Pipeline

### 1. Prerequisites
- A GitHub account.
- Basic familiarity with WordPress (themes, plugins, and exporting content).

### 2. Create Your Master Blueprint (One-Time Setup)
The `blueprint.json` file is the heart of this pipeline. It defines:
- **WordPress & PHP versions**.
- **Plugins & Themes** to install (fetched locally from the `themes/` and `plugins/` folders).
- **Site options** (name, permalinks, timezone) that can be dynamically set via URL parameters.
- **Content import** (the WXR file that populates the site with pages and services).

### 3. Generate a Client Demo (Step-by-Step)
**Step 1: Create a New Project**
1.  Copy the `sample-content.xml` file from the `my-portfolio/` folder.
2.  Rename it based on the client, e.g., `my-portfolio/salon-istanbul-content.xml`.
3.  Edit the file using a text editor or a WordPress export/import tool to customize the content for the specific client.
4.  Add any client-specific images to the `media/` folder within their project directory.

**Step 2: Customize & Share the Live Link**
Use the following URL structure, replacing the parameters with your client's details:

https://playground.wordpress.net/?blueprint-url=https://raw.githubusercontent.com/[YOUR_USERNAME]/wordpress-portfolio/main/blueprint.json&sitename=[CLIENT_SALON_NAME]&timezone=[TIMEZONE]&content_url=https://raw.githubusercontent.com/[YOUR_USERNAME]/wordpress-portfolio/main/my-portfolio/[CLIENT_PROJECT_FOLDER]/content.xml

**Example URL:**

https://playground.wordpress.net/?blueprint-url=https://raw.githubusercontent.com/ehsanmoattari/wordpress-portfolio/main/blueprint.json&sitename=Luxury%20Salon%20Dubai&timezone=Asia/Dubai&content_url=https://raw.githubusercontent.com/ehsanmoattari/wordpress-portfolio/main/my-portfolio/salon-dubai/content.xml


**Step 3: Present the Demo**
Share this link with the client. They can:
- **Browse** the complete, mobile-responsive website.
- **Navigate** through all pages and services.
- **Experience** the live booking system.
- **Even log in** to the admin dashboard (if the `login` step is set to `true` in the blueprint) to see how easy it is to manage.

---

## 🛠️ Customization Guide

### Adding a New Plugin or Theme
1.  Place the plugin or theme ZIP file in the appropriate folder (`plugins/` or `themes/`).
2.  Add a new `step` in the `blueprint.json` file to install and activate it.
3.  Update the `url` in the `pluginData` or `themeData` to point to the file in your repository.

### Changing the Default Design
- **Colors & Fonts:** These are controlled by the Kadence Theme. You can set default styles in the WordPress Customizer and export them as part of your WXR file.
- **Layouts:** All page layouts are built with Kadence Blocks. You can create and save custom block templates within the WordPress editor.

### Updating the Sample Content
1.  Build a fully designed site in your local WordPress environment.
2.  Go to `Tools > Export` in the WordPress admin.
3.  Select "All content" and download the WXR file.
4.  Replace the `my-portfolio/sample-content.xml` file with the new one.

---

## 📜 License

This project is open-source and available under the [MIT License](https://opensource.org/licenses/MIT). You are free to use, modify, and distribute it for commercial purposes.

---

## 🤝 Contributing

This is a personal pipeline designed for a specific workflow. However, suggestions for improvements or bug reports are welcome. Feel free to open an issue or a pull request.

---

## 📫 Connect

- **GitHub:** https://github.com/ehsanmoattari
- **LinkedIn:** https://linkedin.com/in/ehsan-moattari
<!-- - **Portfolio:** [Your Personal Website Link] -->

---

**Built with ❤️ for efficiency, speed, and making a difference in web design industry.**
