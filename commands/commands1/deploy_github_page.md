# Deploy to GitHub Pages

Use this command to build the production site. The project is now configured to publish automatically to GitHub Pages through a GitHub Actions workflow.

## What it does
- Builds the Vite app for production
- Uploads the generated dist folder as a GitHub Pages artifact
- Deploys it automatically when the main branch is updated

## Command
```bash
cd /Users/chenkunhsien/Downloads/claude_code_treasure_game-initial
npm run deploy:github
```

## Required GitHub setup
1. Push this repository to GitHub.
2. Open the repository on GitHub.
3. Go to Settings → Pages.
4. Set Source to GitHub Actions.

## Expected URL
Once the workflow runs successfully, the app will be available at:
https://<your-github-username>.github.io/claude_code_treasure_game-initial/
