# Style Transfer Lab Website

## 📌 Overview
This repository hosts the website for the **Style Transfer Lab**, built using Jekyll with the **Alembic theme**. The site includes blog posts, research papers, and general lab information.

---

## 🔧 Setup Instructions


### Clone the Repository
```sh
git clone https://github.com/style-transfer-lab/your-repo.git
cd your-repo
```

### Install Gems and Run Jekyll Locally if needed
To run the website locally, install **Jekyll and Bundler**:
```sh
gem install jekyll bundler

```sh
bundle install
```
```sh
bundle exec jekyll serve
```
The site will be available at **http://localhost:4000**.

---

## 📄 Adding a New Paper
Each paper is stored in the `papers/` directory as a Markdown file (`.md`).

### Example Paper File Structure
Save your paper as `papers/title-of-paper.md` and follow this format:
```yaml
---
layout: paper
title: "Your Paper Title"
authors: "Author 1, Author 2, Author 3"
conference: "Conference Name (Year)"
permalink: /papers/title-of-paper/
abstract: "A short abstract describing the paper."
image: "/assets/images/title-of-paper.jpg"
---

## Abstract  
Write a longer abstract or summary of your paper here.
```
- **`layout: paper`** ensures the correct page format.
- **`image:`** should be uploaded to `assets/images/` and referenced in the front matter.
- **`permalink:`** should match the file name.

---

## 📝 Editing the Blog
Blog posts are stored in `_posts/` and must follow the Jekyll naming convention: 
```
YYYY-MM-DD-title-of-post.md
```
Example:
```yaml
---
layout: post
title: "New Research on Color Transfer"
date: 2025-03-17
author: "Your Name"
categories: research
---

Your blog content goes here.
```

---

## 🖼 Adding Images
All images should be stored in `assets/images/`.

- Use **descriptive file names** (e.g., `color-transfer-modflows.jpg` instead of `image1.jpg`).
- Reference images in Markdown as follows:
  ```md
  ![Alt Text](/assets/images/image-name.jpg)
  ```

---

## 🚀 Deploying Updates
1. **Commit your changes**:
   ```sh
   git add .
   git commit -m "Adding new paper: Title of Paper"
   git push origin main
   ```
2. The site will update automatically via GitHub Pages.

---

## ❓ Need Help?
- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [Alembic Theme](https://alembic.darn.es/)
- Contact the lab admin for repo access or technical issues.

---

### 🔥 Happy Coding!


# Starter kit for [Alembic](https://alembic.darn.es/)

This is a very simple starting point if you wish to use Alembic [as a Jekyll theme gem](https://alembic.darn.es/#as-a-jekyll-theme) or as a [GitHub Pages remote theme](https://github.com/daviddarnes/alembic-kit/tree/remote-theme) (see `remote-theme` branch).


**[Download the GitHub Pages kit](https://github.com/daviddarnes/alembic-kit/archive/remote-theme.zip)**
