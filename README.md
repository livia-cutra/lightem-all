# LightEmAll Game Project

## Overview
During my **Fundamentals of Computer Science 2 (Fundies 2)** course, I developed **LightEmAll**, a grid-based puzzle game that combines strategy and problem-solving. The main challenge? Rotate tiles on a grid to connect all the wires and light up the entire board. To enhance gameplay, I added features like scoring, step tracking, and a timer.

---

## Key Features

### **Game Mechanics**
- **Interactive Grid:** The game board consists of tiles called `GamePieces`, each with connections in four directions—top, right, bottom, and left.
- **Tile Rotation:** Click on tiles to rotate them, aligning the connections to allow power to flow from the central power station.
- **Power Station Movement:** Use the arrow keys to move the power station around the grid. Valid moves depend on the connections between tiles, adding an extra layer of strategy.

### **Algorithm Integration**
- **Kruskal's Algorithm:** Implemented to generate a **Minimum Spanning Tree (MST)** during board initialization, ensuring all tiles are efficiently connected.
- **Union-Find Structure:** Used to sort and process edges between tiles, forming the MST and establishing logical connections.

### **Extra Credit Features**
- **Gradient Coloring:** Wires change color based on their distance from the power station, visually indicating the strength of the power connection. This was achieved with the `calculateWireColor` method.
- **Steps Counter:** Tracks how many times you've rotated a tile. Each rotation increments the step counter, displayed on the screen.
- **Score Tracking:** The aim is to receive the lowest score possible, as it reflects the amount of steps taken to light the whole board.
- **Timekeeping:** A timer tracks gameplay duration, displaying minutes and seconds using the `onTick` method.
- **Restart Functionality:** The `resetBoard` method resets the board, steps, score, and timer for a fresh start.

---

## Winning Condition
- **Breadth-First Search (BFS):** The game uses BFS starting from the power station to check if all tiles are powered. Once every tile is lit, you receive a congratulatory message!

---

## Testing
These are some examples of what I tested:
- **Kruskal's MST and Edge Sorting:** Verified that the MST is correctly created and edges are sorted as expected.
- **Tile Rotation and Connectivity:** Confirmed that rotating tiles updates their connections accurately.
- **BFS Propagation and Win Conditions:** Ensured the BFS correctly identifies when all tiles are powered.
- **Extra Credit Features:** Tested gradient coloring, timekeeping, and step tracking to verify their functionality.

---

## Running the Game
1. Clone the repository or save the provided `.java` file(s).
2. Import the project into your preferred IDE (e.g., IntelliJ IDEA, Eclipse, VS Code).
3. Add the **Tester** and **JavaLib** libraries to your project build path.
4. Run the `LightEmAllExamples2` class to start the game.
5. The game board initializes, and you can start playing. Enjoy!

---

## Controls
- **Mouse Click:** Rotate tiles by clicking on them.
- **Arrow Keys:** Move the power station up, down, left, or right.
- **Key 'e':** End the game at any time.

---

## Development Insights
Working on this project was both challenging and rewarding:
- **Graph Theory Application:** Implementing Kruskal's Algorithm required a deep dive into graph theory, including efficient sorting and comparator logic for edges.
- **Dynamic Coloring Calculations:** The gradient coloring feature involved precise calculations to smoothly blend colors based on distance from the power station.
- **Balancing Complexity and Modularity:** I aimed to make the game mechanics engaging while maintaining a clean, modular, and testable codebase.

---

Enjoy playing **LightEmAll** and thank you for reading! 🎮💡
