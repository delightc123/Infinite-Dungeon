# Infinite-Dungeon

**A persistent, real-time action dungeon crawler built with Godot 4 + C# (.NET 8).**

Authored and maintained by [Delight Chukwu](https://github.com/delightc123/Infinite-Dungeon). Reimagining classic dark fantasy ARPG atmosphere as an infinite descent into a living, reactive dungeon.

[![Godot 4 .NET](https://img.shields.io/badge/Godot-4.x%20.NET-478CBF?logo=godotengine&logoColor=white)](https://godotengine.org)
[![.NET 8](https://img.shields.io/badge/.NET-8.0-512BD4?logo=dotnet&logoColor=white)](https://dotnet.microsoft.com)
[![C# 12](https://img.shields.io/badge/C%23-12-239120?logo=csharp&logoColor=white)](https://learn.microsoft.com/dotnet/csharp/)
[![Platform](https://img.shields.io/badge/platform-mac%20%7C%20win%20%7C%20linux-lightgrey)](https://github.com/delightc123/Infinite-Dungeon)

---

## Overview

Infinite-Dungeon delivers a deep ARPG loop with an emphasis on build diversity, procedural encounters, and modular C# architecture.

- **Complete Game Loop**: Splash $\rightarrow$ Class Selection (Warrior, Ranger, Mage) $\rightarrow$ Town Hub $\rightarrow$ Procedural Dungeon $\rightarrow$ Combat $\rightarrow$ Loot / Crafting / Bank $\rightarrow$ Death / Respawn.
- **Over 130 Modular Systems**: Fully implemented skill trees (80+ skills), monster families, affix generation, container loot tables, progression tracking, and town economy.
- **Robust C# Architecture**: Built on clean domain-driven architecture with autoloaded singletons (`GameState`, `EventBus`, `SaveManager`) and an automated xUnit test suite.

---

## Quick Start & Setup

### Prerequisites
- **Godot Engine 4.x (.NET edition)**: Ensure Godot with Mono/.NET support is installed.
- **.NET 8+ SDK**: Required to build the C# solutions.

### Build and Run

```bash
# Clone the repository
git clone https://github.com/delightc123/Infinite-Dungeon.git
cd Infinite-Dungeon

# Restore .NET dependencies and build the solution
dotnet build DungeonGame.sln

# Run all unit tests
dotnet test tests/unit/DungeonGame.Tests.Unit.csproj
```

Open the project folder in Godot 4 (.NET Edition) and run the main scene (`res://scenes/main.tscn`).

---

## Game Systems & Architecture

| Subsystem | Namespace / Directory | Key Responsibilities |
| :--- | :--- | :--- |
| **Autoloads** | `scripts/autoloads/` | Core lifecycle singletons: `GameState`, event broadcast channel `EventBus`, and atomic JSON save serializer `SaveManager`. |
| **Combat & Formulas** | `scripts/combat/` | Damage calculations, critical strike rolls, resistance mitigation, and stat block evaluation. |
| **Entities & Enemies** | `scripts/entities/` | Player character controllers, enemy AI behaviors, monster families, and boss encounters. |
| **Inventory & Loot** | `scripts/inventory/` | Slot grids, affixes, depth-based gear tiering, containers, and loot table drop logic. |
| **Skills & Progression** | `scripts/skills/` | Ability database, active skill bars, cooldown state machines, and passive tree mastery. |
| **Town & Economy** | `scripts/town/` | Town hub NPCs, shops, player vault bank, item crafting, and quest tracking. |
| **UI & Canvas** | `scripts/ui/` | Retro HUD, health/mana orbs, inventory grids, settings panels, dialogue windows, and toast notifications. |

---

## Testing & Quality Assurance

Infinite-Dungeon includes an automated xUnit test suite covering core game formulas and mechanics:

```bash
# Run unit tests
dotnet test tests/unit/DungeonGame.Tests.Unit.csproj

# Run integration tests
dotnet test tests/integration/DungeonGame.Tests.Integration.csproj
```

---

## Contributing

Contributions, bug reports, and suggestions are welcome! Please open an issue first to discuss substantial gameplay or architectural changes.

---

## License

Copyright (c) 2026 Delight Chukwu. All rights reserved.
Third-party assets retain their respective licenses (see [CREDITS.md](CREDITS.md)).
