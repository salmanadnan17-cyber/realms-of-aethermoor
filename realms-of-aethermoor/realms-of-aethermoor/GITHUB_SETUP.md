# How to Upload to GitHub and Install via Manifest URL

## Step 1: Upload to GitHub

1. **Go to GitHub and create a new repository:**
   - Visit: https://github.com/new
   - Repository name: `realms-of-aethermoor`
   - Make it **Public** (required for Foundry to access it)
   - **Do NOT** check "Add a README file" (we already have one)
   - Click "Create repository"

2. **Upload the files:**
   
   **Option A - Using GitHub Web Interface (Easiest):**
   - After creating the repo, you'll see a screen with upload options
   - Click "uploading an existing file"
   - Extract the zip file I provided
   - Drag and drop ALL files and folders from the extracted folder
   - Add commit message: "Initial commit"
   - Click "Commit changes"

   **Option B - Using Git Command Line:**
   ```bash
   # Extract the zip file first, then open terminal in that folder
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/realms-of-aethermoor.git
   git push -u origin main
   ```

## Step 2: Update the Manifest URL

After uploading, you need to update `world.json` with your actual GitHub username:

1. On GitHub, navigate to your repository
2. Click on `world.json`
3. Click the pencil icon (Edit)
4. Replace `YOUR-USERNAME` in both URLs with your actual GitHub username:
   ```json
   "manifest": "https://raw.githubusercontent.com/YOUR-ACTUAL-USERNAME/realms-of-aethermoor/main/world.json",
   "download": "https://github.com/YOUR-ACTUAL-USERNAME/realms-of-aethermoor/archive/refs/heads/main.zip",
   ```
5. Click "Commit changes"

## Step 3: Get Your Manifest URL

Your manifest URL will be:
```
https://raw.githubusercontent.com/YOUR-USERNAME/realms-of-aethermoor/main/world.json
```

**Example:** If your GitHub username is `johnsmith`, the URL would be:
```
https://raw.githubusercontent.com/johnsmith/realms-of-aethermoor/main/world.json
```

## Step 4: Install in Foundry VTT

1. In Foundry VTT, click **"Install World"**
2. Paste your manifest URL in the **"Manifest URL"** field
3. Click **"Install"**
4. Wait for installation to complete
5. Launch the world!

## Important Notes:

- The repository **MUST be public** for Foundry to access it
- Use the **raw.githubusercontent.com** URL, not the regular github.com URL
- Make sure you replace `YOUR-USERNAME` with your actual username in the world.json file
- The `/main/` part of the URL refers to your main branch name

## Troubleshooting:

**"Unable to load valid world manifest data"**
- Make sure you edited world.json to replace YOUR-USERNAME
- Verify the repository is public
- Check that you're using the raw.githubusercontent.com URL

**"System may not be undefined"**
- Make sure you have the D&D 5e system installed in Foundry first
- Go to "Game Systems" → Search for "dnd5e" → Install

That's it! Once uploaded to GitHub, you can share this manifest URL with anyone and they can install your world with one click!
