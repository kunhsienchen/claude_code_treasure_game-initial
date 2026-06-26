# Deploy to Vercel

Use this command to publish the current local project to Vercel.

## What it does
- Builds the Vite app
- Deploys it to Vercel
- Returns a public URL for the deployed project

## Command
```bash
cd /Users/chenkunhsien/Downloads/claude_code_treasure_game-initial
npx vercel --prod
```

## Notes
- This project is a Vite + React app, so Vercel will serve the built output.
- If this is the first deployment, Vercel may ask you to log in or link the project to a Vercel account.
