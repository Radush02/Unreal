# Stealth Extraction - Unreal Engine 5

## Overview
Stealth Extraction is a stealth-based FPS developed in Unreal Engine 5. The player must complete various mission objectives while avoiding detection using a combination of strategic movement, environmental interactions, and AI manipulation.

## Features
- **Stealth Mechanics:** Stay undetected by avoiding enemies and security cameras.
- **Dynamic AI Behavior:**
    - AI enemies patrol with either predefined routes or random movement. 
    - AI reacts to noises, prioritizing distractions and enemy threats. 
    - AI chases the player upon detection until the player is caught. 
    - Eliminated AI must be hidden to prevent discovery by cameras. 
- **Advanced Sound Detection:** AI differentiates between types of noises and only the closest enemy investigates high-priority sounds. 
- **Security Cameras:**
    - Cameras scan the area with a cone-shaped field of view and detect players or bodies left in the open. 
    - Triggering cameras too often calls reinforcements and leads to mission failure. 
    - Cameras can be disabled by hacking the server in a mini-game. 
- **Environmental Interactions:**
    - Use forklifts and other objects to create noise and distract AI. 
    - Hide bodies in dumpsters or lockers to prevent alarms. 
    - Use keycards to unlock doors and access restricted areas. 
    - Disable electric panels to open locked gates. 
- **Skill-Based Mini-Game:**
    - Disabling cameras requires precise timing in a mini-game where the player must hit the correct zones to succeed. 
    - Hitting the green zone grants 50 points, hitting the blue zone grants 25 points. 
    - Hitting the red zone creates noise that attracts enemies and closes the server. 
- **Multiple Levels:**
    - A tutorial level introduces basic mechanics. 
    - The main mission, called "Outpost", requires stealing a briefcase while avoiding detection. 
- **Mission Briefing:** The pause menu provides a briefing with the mission objectives. 
- **Death Animation:** Upon being captured, the camera tilts towards the player’s hands as they are handcuffed.
- **Phone:** Currently unused, but planned for activating abilities in future updates. 

## Controls
- **Movement:** WASD 
- **Crouch:** Ctrl 
- **Jump:** Space 
- **Sprint:** Shift 
- **Interact:** E (Open doors, pick up objects, disable security, etc.) 
- **Attack:** Left Mouse Button (Melee attack) 
- **Switch Camera View:** Q (Toggle between first-person and third-person) 
- **Pause Menu:** Tab 

## AI Behavior & Design Patterns
- **Behavior Tree AI:** AI decision-making based on surroundings and player actions. 
- **NavMesh & Pathfinding:** AI follows optimal paths while avoiding obstacles. 
- **Blackboard:** Stores and manages information about the AI's state, such as last heard sound, noise priority, and locations. 
- **NavMeshBoundsVolume:** Defines where the AI can move and how far they can go. 
- **Observer Pattern:** Used for updating various events like AI detections and health changes. 
- **State Pattern:** AI switches between patrol, chase, investigate, and idle states. 
- **Strategy Pattern:** Unified interaction system where objects trigger different behaviors upon interaction. 

## Installation & Setup
1. Download and install Unreal Engine 5.
2. Clone or download this repository.
3. Open the project in Unreal Engine 5.
4. Click "Play" to start testing.

## Future Improvements
- More complex AI behaviors and additional enemy types.
- Expanded levels and objectives.
- Include abilities such as finding the nearest camera, silently killing enemies, and more.
    - These abilities will be activated through the in-game phone. 
- Open crates with crowbars to find loot.

## Credits
- **Developer:** Cordunianu Radu
- **Engine:** Unreal Engine 5
- **Assets:** Various sources including Sketchfab and Epidemic Sound.

## License
This project is for educational and personal use only. Commercial use is strictly prohibited.