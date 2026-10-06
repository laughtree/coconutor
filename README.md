# Coconuter

Coconuter is a web-based tower defense game built with Cocos Creator / Construct-style game development workflow. The player builds and protects a main base, gathers resources through production buildings, and places defensive towers to survive enemy waves at night.

Play the deployed version: [https://coconuter-fbad6.web.app/](https://coconuter-fbad6.web.app/) (目前因負責同學 firebase 已移除無法正常使用)

## Contribution Abstract

此專案為軟體設計與實驗課程的期末專案，由我與其他同學組成的 6 人團隊進行開發。
最初構想為我所提出，參考 Rimworld 、 Mindustry 等作品，以塔防結合沙盒為核心玩法，由大家討論得到共識後依據時程與成員能力調整為如今版本。
其中我所負責的項目如下，詳情可見 Media 段落中截圖與影片
- 沙盒地圖的柏林雜訊地形生成
- 小地圖
  
  <img width="234" height="225" alt="圖片" src="https://github.com/user-attachments/assets/f1dedcb6-050c-4407-97ec-e79867585e9b" />

- 相機移動控制，靠近地圖邊緣時施加阻尼並平滑回彈
- 遊戲內建築物、資源點等無外部素材可用的貼圖與動畫繪製
- 砲台索敵機制與子彈邏輯
相關部分截圖如下:

  
其餘同學貢獻請見下表:

<img width="819" height="415" alt="圖片" src="https://github.com/user-attachments/assets/5a872606-c28f-4131-a61e-f36ed15ffd83" />

## Media

![Coconuter gameplay overview](docs/images/gameplay-overview.jpg)

- [Media gallery](docs/README.md)
- [Day-night cycle GIF](docs/videos/day-night-cycle.gif)


## Game Overview

The game starts with the player placing a main base. The objective is to protect that base by collecting resources and building defensive structures before enemies appear.

The map contains different resource areas. Each production building can only be placed on a compatible terrain type: (My Part)

- **Lumber Mill**: gathers wood
- **Quarry**: gathers stone
- **Mine**: gathers ore or mineral resources

Collected resources are used to build defensive towers around the base.

## Core Gameplay

```text
Place main base
  -> Build resource production buildings
  -> Gather resources
  -> Build defensive towers
  -> Prepare during daytime
  -> Defend against enemies at night
  -> Survive the level
```

## Defensive Buildings (My Part)

The game includes multiple tower types for defending the base:

- **Cannon Tower**: deals damage to enemies from range
- **Sword Tower**: close-range defensive structure
- **Mage Tower**: magical attack tower for enemy control or damage

Each tower contributes to the defense layout and helps prevent enemies from reaching the main base.

## Day-Night System

Coconuter uses a day-night cycle:

- **Daytime**: players build, gather resources, and prepare defenses.
- **Nighttime**: enemies spawn and attack the base.

Enemies only appear at night, so the player must use the daytime phase efficiently to prepare for the next wave.

## Levels

The game contains two levels. Difficulty is mainly controlled by enemy quantity and wave pressure.

## Lobby Features

The lobby includes:

- opening animation
- sign up and login
- scoreboard
- settings
- visual art style presentation

## Game Features

### Mini Map (My Part)

A mini map helps players understand the overall map layout and monitor important areas during gameplay.

### Procedural Terrain (My Part)

The project uses Perlin noise to generate or shape map variation, giving the terrain a more organic layout.

### BFS Pathfinding

Enemies use BFS pathfinding to navigate toward the player base. This allows enemy movement to react to the map layout and obstacles.

### Animation (My Part)

The game includes animated UI/gameplay elements to make the lobby and in-game interactions feel more polished.

### Art Direction (My Part)

Coconuter uses a custom visual style for its buildings, map, and game interface.

## Tech Stack

| Area | Tools / Concepts |
| --- | --- |
| Game Engine | Cocos Creator / web game build workflow |
| Deployment | Firebase Hosting |
| Procedural Generation | Perlin noise |
| Pathfinding | BFS pathfinding |
| Gameplay Systems | Tower defense, resource collection, day-night cycle |
| UI Systems | Lobby, login/signup, scoreboard, settings |

## Repository Notes

This repository contains a web game build. Some generated files may come from the game engine export process, so the source structure may differ from a hand-written web application.
