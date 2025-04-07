# Kyle's Portfolio Site

This is my personal portfolio site built with [Hugo](https://gohugo.io/) using the [Blowfish theme](https://github.com/nunocoracao/blowfish). It showcases my experience, projects, and writing related to software engineering, cloud infrastructure, and security.

The site is deployed via [Netlify](https://www.netlify.com/) and updates automatically from the `main` branch.

## Features

- **Fast static site** powered by Hugo and the Blowfish theme
- **Blog section** that mirrors LinkedIn posts (auto-published via GitHub Actions)
- **Commenting system** using [Giscus](https://giscus.app/) and GitHub Discussions
- Custom layouts and logic to:
  - Sort blog posts by publish date
  - Maintain weight-based ordering for other content sections
  - Schedule posts via feature branches (e.g. `blog/2025-04-10_example-post`)

## Structure

    content/
      ├── blog/              # Blog posts in markdown
      ├── projects/          # Project writeups
      └── about.md           # About me section

    layouts/
      ├── blog/list.html     # Blog list view override (ordered by date)
      ├── partials/comments.html  # Giscus integration
      └── _default/          # Default templates

## Scheduled Blog Posting

Blog posts can be scheduled ahead of time by creating feature branches named in the format:

    blog/YYYY-MM-DD_post-topic

A [GitHub Actions workflow](.github/workflows/scheduled-blog-merge.yml) runs hourly and merges branches into `main` on their publish date, triggering a deploy on Netlify.

## Deployment

This site is continuously deployed via Netlify. Any push to `main` triggers a rebuild.
