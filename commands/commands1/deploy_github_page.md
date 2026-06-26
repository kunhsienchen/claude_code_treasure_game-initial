# Deploy to GitHub Pages

Use this command to build the project and publish the static site to GitHub Pages.

## What it does
- Builds the Vite app for production
- Publishes the generated dist folder to the gh-pages branch
- Makes the app available at a GitHub Pages URL

## Command
```bash
cd /Users/chenkunhsien/Downloads/claude_code_treasure_game-initial
npm run deploy:github
```

## Notes
- This project uses Vite, so the build output is generated in the dist folder.
- The GitHub Pages URL will look like:
  https://<your-github-username>.github.io/claude_code_treasure_game-initial/
- Make sure your repository exists on GitHub and has GitHub Pages enabled.
