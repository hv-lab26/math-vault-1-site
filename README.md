[![Code and docs: MIT](https://img.shields.io/badge/code%20%26%20docs-MIT-green)](LICENSE)

# Maths Unit 1 Vault - Website

This repo builds [maths-unit-1-vault](https://github.com/) (my Obsidian notes for Functions and Introductory Calculus) into a browsable website using [Quartz](https://quartz.jzhao.xyz/), and deploys it to GitHub Pages automatically on every push.

## Updating the site

1. Edit the markdown files under `content/Content/`, or replace them with a fresh copy of the Obsidian vault.
2. Commit and push to the `v5` branch.
3. GitHub Actions rebuilds and redeploys the site automatically (check the **Actions** tab for progress).

## Local preview

```
npm install
npx quartz build --serve
```
then open http://localhost:8080.
