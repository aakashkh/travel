# Travel Blog

This is a travel blog built with Hugo and Tailwind CSS.

## Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/aakashkh/travel.git
   ```
2. **Install dependencies:**
   ```bash
   npm install
   ```
3. **Run the development server:**
   ```bash
   hugo server -D
   ```

## Adding a New Post

1. **Create a new post:**
   ```bash
   hugo new posts/your-post-title.md
   ```
2. **Edit the new post:**
   The new post will be created in the `content/posts` directory. Edit the file to add your content.

## Deployment

This project is automatically deployed to GitHub Pages using a GitHub Actions workflow. The workflow is defined in `.github/workflows/gh-pages.yml`.

When changes are pushed to the `main` branch, the workflow will:
1. Build the Hugo site.
2. Deploy the contents of the `public` directory to the `gh-pages` branch.
