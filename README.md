## Endless Online Combat Assistant

This repository contains a Python-based combat assistant for the MMORPG Endless Online (EO). It leverages memory reading (pymem), process injection (Frida), and a web-based UI (Flask) to provide real-time combat automation and character monitoring.

**Features:**

* **Monster Detection:** Automatically detects and tracks nearby monsters in the game.
* **Combat Kiting:** Uses A* pathfinding to kite monsters while maintaining a safe distance and maximizing damage output.
* **Automatic Attacking:** Automatically attacks monsters within range.
* **Health and Mana Monitoring:** Tracks player HP and Mana, and automatically uses healing skills (F1) when necessary.
* **Resting:** Automatically sits down (F11) to regenerate health when HP falls below a threshold.
* **Web-based UI:** Provides a visual representation of the game map, player and monster locations, and player stats.
* **Address Management:** Allows users to dynamically add and remove memory addresses for tracking specific entities.

**How it works:**

1. **Memory Reading (pymem):** Reads the game's memory to extract player and monster coordinates, health, mana, and other relevant data.
2. **Process Injection (Frida):** Injects a JavaScript script into the game process to intercept specific function calls and retrieve memory addresses for monster objects.
3. **Combat Logic:** Uses A* pathfinding and a set of predefined rules to determine the optimal movement and attack patterns for combat kiting.
4. **Web UI (Flask):** Presents the gathered information in a user-friendly web interface, allowing for real-time monitoring and control.

**Requirements:**

* Python 3
* pymem
* Frida
* Flask
* tkinter
* requests

**Installation:**

1. Install the required packages using pip: `pip install -r requirements.txt`
2. Run the script: `python main.py`

**Usage:**

1. Launch the Endless Online game client.
2. Run the script. You will be prompted to enter the memory addresses for the player's X and Y coordinates.
3. Access the web UI by opening a web browser and navigating to `http://localhost:5000/map`.

**Disclaimer:**

This tool is intended for educational purposes only and should be used responsibly. Using this tool may violate the terms of service of Endless Online. Use at your own risk.

**Contributing:**

Contributions are welcome! Please feel free to submit pull requests or open issues if you encounter any problems or have suggestions for improvement.

**License:**

This project is licensed under the MIT License - see the LICENSE file for details.
