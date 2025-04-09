# 📦 ItemConfigLib

A lightweight and flexible library for loading and validating custom item configurations from YAML files in Spigot/Bukkit plugins. Supports enchantments, attributes, and much more.

---

## ✨ Features

- ✅ Simple YAML-based item configuration
- 🧱 Supports enchantments, lore, display names, and material validation
- 📜 Easy integration into any Bukkit/Spigot plugin
- ⚠️ Built-in logging for config issues
- 🧪 Designed for testing & reusability

---

## 📦 Installation (via JitPack)

> You'll need to [build with BuildTools](https://www.spigotmc.org/wiki/buildtools/) and have the full `spigot` dependency available locally.

```xml
# TODO
````

* * *

📘 Example `items.yml`
----------------------

```yaml
epic_sword:
  material: DIAMOND_SWORD
  name: "&bEpic Sword"
  lore:
    - "&7This sword was forged by the ancients"
    - "&eUse it wisely!"
  enchantments:
    - sharpness 5
    - unbreaking 3
    - fire_aspect 2
  attributes:
    - generic.attack_damage ADD_NUMBER 12.0 HAND
    - generic.attack_speed ADD_SCALAR 1.6 HAND
  flags:
    - HIDE_ENCHANTS
    - HIDE_ATTRIBUTES
  unbreakable: true
  datacontainer:
    - myplugin:custom_id string epic_sword_001
    - myplugin:rarity string legendary
  custommodeldata: 1001
```

* * *

🧪 Usage
--------

```java
# TODO
```

* * *

🔑 Supported YAML Keys
----------------------

| Key | Type | Description |
| --- | --- | --- |
| `material` | String | Bukkit `Material` name |
| `name` | String | Display name (supports color codes) |
| `lore` | List | Item lore lines |
| `enchantments` | List | Format: `enchant level` |
| `attributes` | List | Format: `attribute operation value [slot]` |
| `flags` | List | Bukkit `ItemFlag` enums |
| `unbreakable` | Boolean | Marks the item as unbreakable |
| `custommodeldata` | Integer | Custom model data for resource pack support |
| `color` | String | RGB color for leather armor (e.g. `255,0,0`) |
| `base_potion` | String | Base potion type |
| `potion_effects` | List | Custom potion effects |
| `firework` | List | Firework effect configs |
| `firework_power` | Integer | Power level of firework |
| `patterns` | List | Banner pattern entries |
| `datacontainer` | List | PDC entries: `namespace:key type value` |
| `hide_all_attributes` | Boolean | Hides all item flags |
| `hide` | List | Specific flags to hide |
| `texture` | String | Base64 head texture |
| `owner` | String | Head owner (player name) |
| `skull_uuid` | String | UUID for head owner |
| `book` | Section | For written books (title, author, pages) |
| `trim` | Section | Armor trim (1.20+): `material`, `pattern` |
| `amount` | Integer | Item amount |

* * *

📁 Project Structure
--------------------

```
itemconfiglib/
├── config/
│   ├── ItemYamlKeys.java
│   └── YamlItemFormatter.java
├── util/
│   ├── Logger.java
│   └── StringUtils.java
├── errors/
│   └── InvalidItemConfigException.java
└── responses/
    └── YamlItemParseResponse.java
```

* * *

👥 Contributing
---------------

*   Pull requests are welcome!
    
*   Open issues for bugs, suggestions, or improvements.
    
*   Star the repo if you like the project ⭐
    

* * *

📜 License
----------

MIT License © [RaulH22](https://github.com/RaulH22)  
Use freely in public or commercial plugins.

* * *


