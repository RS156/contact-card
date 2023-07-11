# Contact card for apps like sitch.cards

This is the contct card built with Svelte + Vite

# Configure your personal data in the app

Both the socialmedia links and contact cards are configurable.

**Steps**
1. In ./sr/assets, open 'socialLinkIcons.json' and 'contactCardInfo.json'.
2. For social link  icons, iconClass needs to be used from fontawesome icons (https://fontawesome.com/icons). 
3. In contact card, label and info can be edited. Icon object is also present which needs to be used from fontawesome icons

## Recommended IDE Setup

[VS Code](https://code.visualstudio.com/) + [Svelte](https://marketplace.visualstudio.com/items?itemName=svelte.svelte-vscode).

## Build Steps
1. Run npm install to install all the dependencies
2. Run npm run dev to test out your changes locally.
3. Run npm run build, to generated the production build. The production build will be created in 'dist' folder.
4. Deploy the static site in dist folder to make the application live