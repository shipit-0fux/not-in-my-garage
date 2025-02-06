# 🚫 Not-In-My-Garage 🚫

*Ever notice how car shopping sites let you filter **for** specific makes and models, but **none** of them let you say "show me EVERYTHING EXCEPT Nissan Rogues"?* 

This frustration led to **Not-In-My-Garage**: a Tampermonkey userscript that *finally* lets you banish those unwanted vehicles from your car shopping experience.

A simple but powerful tool that automatically hides listings for vehicles you never want to see again. *Because some cars just don't deserve a spot in your garage.*


## Features
- Automatically hides listings for specified makes/models
- Works across multiple car shopping sites:
  - Cars.com
  - AutoTrader.com
  - Carvana.com
  - Carmax.com
  - CarFax.com
  - CarGurus.com
- Customizable block list
- Instant filtering as you browse
- No page reloads required

## Installation
1. Install [Tampermonkey](https://www.tampermonkey.net/) for your browser
2. Click [here](link-to-raw-script) to install the script
3. The script will automatically activate when you visit supported car shopping sites

## Configuration
Edit the `blockedModels` array in the script settings to customize which vehicles you want to hide:
```javascript
const blockedModels = [
    'buick encore',
    'dodge journey',
    'ford ecosport',
    // Add your automotive nemeses here
];
```

## Adding Support for New Sites

Quick guide to add a new car shopping website:

1. Create a new site handler in `sitesConfig` object:
```javascript
const siteConfig = {
    'www.example.com': {
       container: '.listing-card', // CSS selector for each listing that will be hidden
       textElement: '.vehicle-title',   // CSS selector in which to search for a blocked model
    }
};
```

---
*Disclaimer: This script is not affiliated with any of the supported car shopping websites.*

## Contributing
Found a bug? Want to add support for another car site? PRs welcome!

## Known Issues
- Some sites may update their layouts, potentially breaking the filters
- Currently case-sensitive matching only

## License
MIT License - See LICENSE file for details

- Inspired by countless hours of scrolling past Nissan Rogues

---
*Disclaimer: This script is not affiliated with any of the supported car shopping websites.*
