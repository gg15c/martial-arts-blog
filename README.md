# 🥋 Martial Arts Blog

A static blog built with [Hugo](https://gohugo.io/) and hosted on
[GitHub Pages](https://pages.github.com/).

## 🌐 Live Site

👉 [https://gg15c.github.io/martial-arts-blog/](https://gg15c.github.io/martial-arts-blog/)

## 🛠️ Tech Stack

| Tool            | Purpose                  |
|-----------------|--------------------------|
| Hugo            | Static site generator    |
| PaperMod        | Blog theme               |
| GitHub Pages    | Free hosting             |
| GitHub Actions  | Automatic deployment     |
| Markdown        | Content writing format   |

## 📁 Project Structure

    martial-arts-blog/
    ├── .github/workflows/   # GitHub Actions deploy workflow
    ├── archetypes/          # Post templates
    ├── content/             # All your content
    │   ├── posts/           # Blog posts (Markdown)
    │   └── about.md         # About page
    ├── data/                # Data files
    ├── layouts/             # Custom layouts
    ├── static/              # Static assets (images, etc.)
    ├── themes/PaperMod/     # Blog theme
    ├── deploy.sh            # Manual deploy script (backup)
    ├── hugo.toml            # Site configuration
    └── README.md            # This file

## 📂 Branches

| Branch       | Purpose                                          |
|--------------|--------------------------------------------------|
| main         | Source code (Markdown, config, theme)             |
| gh-pages     | Built website (HTML) served by GitHub Pages       |

## ✍️ How to Add a New Post

### Step 1: Create a new post

    hugo new posts/my-new-post.md

### Step 2: Edit the post and set draft to false

    nano content/posts/my-new-post.md

Make sure the front matter has:

    ---
    title: "My New Post"
    date: 2026-01-01
    tags: ["tag1", "tag2"]
    summary: "A short description."
    draft: false
    ---

    Your content here...

Note: New posts default to draft: true.
Change it to draft: false or the post will not appear on the live site.

### Step 3: Preview locally

    hugo server -D --baseURL http://localhost:1313/

Open http://localhost:1313/ in your browser.
Press Ctrl+C to stop the server.

### Step 4: Push to GitHub (auto deploys)

    git add .
    git commit -m "New post: my new post"
    git push origin main

GitHub Actions will automatically:
1. Build the site with Hugo
2. Push the built HTML to gh-pages branch
3. Site updates in 2-3 minutes

## 🚀 Deployment

### Automatic (GitHub Actions)

Every push to main branch triggers automatic deployment.
No manual steps needed.

Monitor deployments at:
https://github.com/gg15c/martial-arts-blog/actions

### Manual (Deploy Script — Backup)

If GitHub Actions fails, use the backup script:

    ./deploy.sh

## 🏗️ Local Development

### Prerequisites

- [Hugo Extended](https://gohugo.io/installation/)
- [Git](https://git-scm.com/)

### Setup

    # Clone the repo
    git clone https://github.com/gg15c/martial-arts-blog.git
    cd martial-arts-blog

    # Initialize theme submodule
    git submodule update --init

    # Run local server
    hugo server -D --baseURL http://localhost:1313/

Visit http://localhost:1313/

## 📝 Content

| Post                            | Tags                            |
|---------------------------------|---------------------------------|
| Front Kick Basics               | kicks, fundamentals, beginner   |
| Essential Martial Arts Stances  | stances, fundamentals, beginner |

## 📜 License

© 2026 This project is for personal use. All content is original.