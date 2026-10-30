# Tank Wars

A local two-player top-down tank shooter built in Unity (C#). Two players share one keyboard, fight off waves of AI enemies, and grab power-ups that change how they shoot.

<!-- Add a GIF or screenshot of gameplay here, e.g. ![Gameplay](docs/gameplay.gif) -->

## Features

- **Two players, one keyboard.** Each tank has its own control scheme and Rigidbody2D movement, so both players can drive and fire at the same time.
- **AI enemies.** Enemies use Unity's NavMesh to chase whichever player is closest, and speed up once a player is within range.
- **Enemy spawning.** A spawner drops a new enemy at a random spawn point every few seconds.
- **Power-ups.** Power-ups appear at random positions on the map, without reusing a position until the others have been used:
  - **Rapid fire:** faster shots for 10 seconds
  - **Burst:** fires five bullets in quick succession
  - **Shield:** a 10-second shield that destroys enemies on contact
- **Game over flow.** A singleton `GameManager` pauses the game and loads a Game Over scene.

## Controls

| Action | Player 1 | Player 2 |
|---|---|---|
| Drive forward | Up Arrow | W |
| Rotate | Left / Right Arrow | A / D |
| Fire | Space | V |

## Running it

1. Install **Unity 2022.3.34f1** (or another 2022.3 LTS version) through Unity Hub.
2. Clone this repository and open the folder in Unity Hub (**Add project from disk**).
3. Open `Assets/Scenes/SampleScene.unity` and press **Play**.

## Project structure

```
Assets/
  Scenes/    SampleScene (gameplay), GameOverScene
  Scripts/   Player controllers, bullets, enemies, spawners, power-ups, GameManager
  Prefabs/   Tanks, bullets, enemies, power-ups; NavMeshComponents (Unity's 2D NavMesh extension)
```

## Built with

- Unity 2022.3 LTS, C#
- Unity Physics 2D (Rigidbody2D, colliders and triggers)
- NavMeshComponents for 2D enemy pathfinding
