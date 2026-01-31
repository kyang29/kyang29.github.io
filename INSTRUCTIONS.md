# Kong.io Blog Application Instructions

This project is a static site generated with [Hugo](https://gohugo.io/), using the [Blowfish](https://blowfish.page/) theme.

## Prerequisites

- **Hugo**: Ensure you have Hugo installed (Extended version recommended).
  - Check version: `hugo version`
- **Git**: Required for version control and theme management.
- **Go**: Required if using Hugo Modules (optional for this setup as it uses submodules, but good to have).

## Project Setup

1.  **Navigate to the project directory**:
    ```bash
    cd quickstart
    ```

2.  **Initialize/Update Submodules** (This installs the theme):
    ```bash
    git submodule update --init --recursive
    ```

## Local Development

To run the local development server with live reload:

```bash
hugo server
```

- Access the site at: `http://localhost:1313/`
- **Note**: Drafts are not shown by default. To view drafts, use:
    ```bash
    hugo server -D
    ```

## Managing Content

### Creating a New Post

Create a new markdown file in the `content/posts` directory:

```bash
hugo new posts/my-new-post.md
```

This will create a file with the default front matter.

### Front Matter

Example front matter for a post:

```yaml
---
title: "My New Post"
date: 2026-01-31
draft: true
tags: ["personal", "tech"]
summary: "A brief summary of the post."
---
```

- Set `draft: false` when you are ready to publish.

## Building for Production

To build the static site (generates files in the `public/` directory):

```bash
hugo
```

The content of the `public/` folder is what you deploy to your hosting provider (e.g., GitHub Pages, Netlify, Vercel).

## Theme Maintenance

The **Blowfish** theme is configured as a Git submodule.

To update the theme to the latest version:

```bash
git submodule update --remote --merge
```

## Structure Overview

- **`content/`**: Your markdown content (posts, pages).
- **`config/_default/`**: Configuration files (`hugo.toml`, `params.toml`, `menus.en.toml`).
- **`themes/`**: Contains the `blowfish` theme submodule.
- **`static/`**: Static assets (images, files) served as-is.
- **`assets/`**: Assets processed by Hugo (CSS, JS).
- **`public/`**: Build output (ignored by Git).
