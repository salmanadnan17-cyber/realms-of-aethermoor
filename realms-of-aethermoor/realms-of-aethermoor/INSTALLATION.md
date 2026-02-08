# Local Installation Guide

If you're installing this world directly to Foundry VTT (not from GitHub), follow these steps:

## Step 1: Find Your Foundry Data Folder

### Windows
1. Press `Win + R`
2. Type: `%localappdata%\FoundryVTT`
3. Press Enter
4. Open the `Data` folder, then the `worlds` folder

### macOS
1. Open Finder
2. Press `Cmd + Shift + G`
3. Type: `~/Library/Application Support/FoundryVTT`
4. Press Enter
5. Open the `Data` folder, then the `worlds` folder

### Linux
1. Open your file manager
2. Navigate to: `~/.local/share/FoundryVTT/Data/worlds`

## Step 2: Install the World

1. Extract the `realms-of-aethermoor.zip` file
2. Copy the entire `realms-of-aethermoor` folder into the `worlds` folder you found in Step 1
3. Your folder structure should look like:
   ```
   FoundryVTT/
   └── Data/
       └── worlds/
           └── realms-of-aethermoor/
               ├── world.json
               ├── data/
               ├── assets/
               └── ...
   ```

## Step 3: Launch the World

1. Start Foundry VTT
2. Click "Return to Setup" if you're in a world
3. Click the "Game Worlds" tab
4. You should see "Realms of Aethermoor" in the list
5. Click "Launch World"

## Troubleshooting

### "World not appearing in list"
- Make sure the folder is named exactly `realms-of-aethermoor`
- Verify that `world.json` is directly inside this folder (not in a subfolder)

### "System 'dnd5e' not installed"
- Go to "Game Systems" tab in Foundry
- Click "Install System"
- Search for "D&D5e" or "Dungeons & Dragons Fifth Edition"
- Click Install
- Then try launching the world again

### "Compatibility warnings"
- Make sure you're running Foundry VTT version 11 or higher
- Update to the latest version of the dnd5e system

## Next Steps

Once the world is loaded:
1. Read the "Welcome to the Realms of Aethermoor" journal entry
2. Review the NPCs in the Actors tab
3. Check out the magic items
4. Use the adventure hooks to start your campaign!

Enjoy your game!
