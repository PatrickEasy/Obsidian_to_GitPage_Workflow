# Obsidian to GitHub Pages Workflow

This repository automatically converts and publishes Markdown files to GitHub Pages using Jekyll.

## How It Works

1. **Add or edit** any `.md` file in this repository
2. **Commit and push** your changes to the `main` or `master` branch
3. **GitHub Actions** automatically builds the site with Jekyll
4. **Your site** is published at: `https://PatrickEasy.github.io/Obsidian_to_GitPage_Workflow/`

## Setup Instructions

### Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** → **Pages**
3. Under "Build and deployment":
   - Source: Select **GitHub Actions**
4. Save the settings

### First Deployment

After you push these files and enable GitHub Pages:
- The workflow will run automatically (check the **Actions** tab)
- Your site will be available at the URL above within a few minutes

## Adding New Pages

Simply add new `.md` files to the repository and they'll be automatically published. Remember to:
- Add links to new pages in `index.md` so they're discoverable
- Use proper Markdown formatting
- Commit and push your changes

## Local Testing (Optional)

To test locally before pushing:

```bash
# Install dependencies
bundle install

# Run Jekyll locally
bundle exec jekyll serve

# Visit http://localhost:4000/Obsidian_to_GitPage_Workflow/
```

## File Structure

- `index.md` - Homepage
- `*.md` - Your content files (like Christmas Presents.md)
- `_config.yml` - Jekyll configuration
- `.github/workflows/jekyll.yml` - GitHub Actions workflow
- `Gemfile` - Ruby dependencies

## Notes

- The site uses the Minima theme by default
- Files are automatically rebuilt on every push
- Check the Actions tab for build status
