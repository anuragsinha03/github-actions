# GitHub Actions Setup for github-actions-demo

This repository contains a simple static HTML project deployed automatically to GitHub Pages using GitHub Actions.

---

## What This Project Does

- On every push to the `main` branch, a GitHub Actions workflow runs.
- The workflow checks out your code and deploys the contents (your HTML file) to the `gh-pages` branch.
- GitHub Pages then serves your site directly from the `gh-pages` branch.

---

## How GitHub Actions Works Here

1. **Trigger:** On every commit pushed to the `main` branch.
2. **Checkout:** The workflow checks out your repository code.
3. **Deploy:** Uses the `peaceiris/actions-gh-pages` action to publish your HTML files from the root directory (`.`) to the `gh-pages` branch.
4. **Serve:** GitHub Pages serves your site from the `gh-pages` branch.

---

## GitHub Actions Workflow File

Here is the key part of your workflow file (`.github/workflows/deploy.yml`):

## Important GitHub Repository Settings

To ensure your site deploys and serves correctly, configure the following in your repository settings:

### 1. Set GitHub Pages Source to `gh-pages` Branch

- Go to your repository **Settings** → **Pages**.
- Under **Source**, select the **gh-pages** branch.
- Save the settings.

This tells GitHub Pages to serve your site from the branch where your workflow deploys the static files.

### 2. Enable Workflow Permissions

- Go to your repository **Settings** → **Actions** → **General**.
- Under **Workflow permissions**, ensure **Read and write permissions** are enabled.
- Also, check **Allow GitHub Actions to create and approve pull requests** if needed.

This is required so the workflow can push the built files to the `gh-pages` branch.

---

## How to Use

1. Make a change to your HTML file or add new static files.
2. Commit and push the changes to the `main` branch.
3. GitHub Actions will automatically run the workflow.
4. After the workflow completes successfully, your updated site will be live at: https://anuragsinha03.github.io/github-actions/

