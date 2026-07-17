# Wuthering Waves Character Build Database

A JSON database of character metadata, upgrade materials, base stats, skill multipliers, and build recommendations for Wuthering Waves.

This database is automatically updated twice a month.

---

## 📦 Download Database Archives

To avoid cloning the entire repository history, you can download pre-packaged, up-to-date archives directly from our latest release assets:

### Standard Databases
*   [**Download Standard JSON (wuwa-db.zip)**](https://github.com/TheInternetUse7/wuwa-character-build-db/releases/download/latest/wuwa-db.zip)  
    *Formatted, human-readable JSON files with indentation (ideal for local inspection).*
*   [**Download Standard Tarball (wuwa-db.tar.gz)**](https://github.com/TheInternetUse7/wuwa-character-build-db/releases/download/latest/wuwa-db.tar.gz)  
    *Tarball alternative of the standard, formatted dataset.*

### Minified Databases
*   [**Download Minified JSON (wuwa-db-minified.zip)**](https://github.com/TheInternetUse7/wuwa-character-build-db/releases/download/latest/wuwa-db-minified.zip)  
    *Whitespace-stripped JSON files (ideal for bandwidth efficiency).*
*   [**Download Minified Tarball (wuwa-db-minified.tar.gz)**](https://github.com/TheInternetUse7/wuwa-character-build-db/releases/download/latest/wuwa-db-minified.tar.gz)  
    *Tarball alternative of the minified dataset.*

---

## 📂 Directory Structure

```text
├── schema.json          # JSON schema for validating character builds
└── data/
    ├── characters.json  # Roster of all characters, elements, rarities, and slugs
    └── builds/
        ├── camellya.json
        ├── aemeath.json
        └── ...
```

---

## 🛠️ Usage & Integration

Developers can fetch files directly from GitHub's CDN to integrate them into Discord bots, websites, or applications.

### 1. Fetching the Character Roster Directory
```javascript
// Fetch the list of all available character slugs
fetch('https://raw.githubusercontent.com/TheInternetUse7/wuwa-character-build-db/main/data/characters.json')
  .then(response => response.json())
  .then(data => {
    const characters = data.data.characters;
    console.log(characters);
  });
```

### 2. Fetching a Specific Character Build Guide
```javascript
const characterSlug = "camellya";

fetch(`https://raw.githubusercontent.com/TheInternetUse7/wuwa-character-build-db/main/data/builds/${characterSlug}.json`)
  .then(response => response.json())
  .then(build => {
    console.log(`Weapon recommendation: ${build.data.best_weapons[0].weapon_name}`);
  });
```

---

## ⚖️ License

This database is licensed under the [MIT License](LICENSE). Game data and assets belong to Kuro Games.
