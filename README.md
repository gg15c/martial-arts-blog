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
| Markdown        | Content writing format   |

## 📁 Project Structure

    martial-arts-blog/
    ├── archetypes/          # Post templates
    ├── content/             # All your content
    │   ├── posts/           # Blog posts (Markdown)
    │   └── about.md         # About page
    ├── data/                # Data files
    ├── layouts/             # Custom layouts
    ├── static/              # Static assets (images, etc.)
    ├── themes/PaperMod/     # Blog theme
    ├── hugo.toml            # Site configuration
    └── README.md            # This file

## ✍️ How to Add a New Post

    # 1. Create new post
    hugo new posts/my-new-post.md

    # 2. Edit the post
    nano content/posts/my-new-post.md

    # 3. Set draft: false when ready

    # 4. Preview locally
    hugo server -D

    # 5. Save source code
    git add .
    git commit -m "New post: my new post"
    git push origin main

    # 6. Build site
    hugo --minify

    # 7. Deploy to gh-pages
    cd /tmp
    rm -rf gh-pages-deploy
    git clone https://github.com/gg15c/martial-arts-blog.git gh-pages-deploy
    cd gh-pages-deploy
    git checkout gh-pages
    git rm -rf .
    cp -r ~/martial-arts-blog/public/* .
    git add .
    git commit -m "Deploy: my new post"
    git push origin gh-pages
    rm -rf /tmp/gh-pages-deploy
    cd ~/martial-arts-blog
    git checkout main

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
    hugo server -D

Visit http://localhost:1313/martial-arts-blog/

## 📂 Branches

| Branch       | Purpose                                          |
|--------------|--------------------------------------------------|
| main         | Source code (Markdown, config)                   |
| gh-pages     | Built website (HTML) served by GitHub Pages      |

## 📝 Content

| Post                            | Tags                            |
|---------------------------------|---------------------------------|
| Front Kick Basics               | kicks, fundamentals, beginner   |
| Essential Martial Arts Stances  | stances, fundamentals, beginner |

## 📜 License

© 2026 This project is for personal use. All content is original.