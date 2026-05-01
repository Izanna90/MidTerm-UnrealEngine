Midterm Project: Third-Person Combat Simulation

Student Name: Theo Fisch Dewailly
Course: 3D Game Applications
Engine Version: Unreal Engine 5 (Spring 2026)

1. Project Overview

This project is a third-person combat simulation built using the Unreal Engine 5 Third Person template. Following the assignment constraints, the entire environment and all characters are constructed using primitive meshes (cubes, spheres, and cylinders). The game features a player-controlled character facing off against three AI-driven enemies in a tactical arena.

2. Core Features

Combat System: Both player and AI use a projectile-based system. Each actor starts with 10 HP, and each hit reduces health by 1 HP.
Custom HUD: A Widget Blueprint displays the player's health bar, remaining ammunition, and all three enemy health bars.
AI Behavior Tree: Enemies use a structured Behavior Tree to make decisions:

Retreat: Maintain a tactical distance if the player is too close.
Attack: Fire projectiles when the player is within Line of Sight (LOS).
Roam: Move to random locations within the arena when the player is not detected.

Win/Loss Conditions:

Victory: Eliminate all 3 enemies.
Defeat: Reaching 0 HP or running out of ammunition.

3. Technical Implementation

Navigation: A NavMesh Bounds Volume is used for AI pathfinding.
Sensing: A custom BTService updates the player's location and visibility status every 0.3 seconds.
Environment: The arena was designed using BSP brushes and primitives, strategically placed to offer cover and break the AI's Line of Sight.

4. Known Bugs / Incomplete Features

None at this time.

5. Controls

Move: W, A, S, D
Jump: Space Bar
Fire: Left Mouse Button
Restart: Click the "Restart" button on the Game Over/Victory screen.
