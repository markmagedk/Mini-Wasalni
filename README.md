# 🌍 Graph Management System  

This C++ program implements a **Graph Management System** that allows users to create, modify, and explore graphs representing cities and their connections (roads). 🏙️🚗 It supports **both weighted and unweighted graphs**, as well as **directed and undirected graphs**.  

## ✨ Features  

1️⃣ **Graph Creation & Management**  
   - Users can create a graph with cities as **nodes** and roads as **edges**.  
   - The graph can be **directed (one-way roads) ➡️** or **undirected (two-way roads) 🔄**.  
   - It can also be **weighted (roads have distances) 📏** or **unweighted 🚫**.  

2️⃣ **Adding & Deleting Cities and Roads**  
   - 🏙️ Add new cities and roads to an existing graph.  
   - ❌ Delete cities (removing all their connections).  
   - 🛣️ Remove specific roads between cities.  

3️⃣ **Graph Storage (Save & Load) 💾**  
   - ✅ Save the graph structure to a file (`Storage.txt`) for future use.  
   - 🔄 Reload the graph when the program restarts.  

4️⃣ **Graph Traversal & Search 🕵️**  
   - 🔍 **DFS (Depth-First Search)**: Explores cities in depth-first order.  
   - 🚶 **BFS (Breadth-First Search)**: Finds the shortest path in unweighted graphs.  
   - 🏎️ **Dijkstra’s Algorithm**: Finds the shortest path in weighted graphs efficiently.  

---

## 🛠️ How the Code Works  

📌 **Graph Representation:**  
- Uses a `Graph` class containing a `map<string, Node>` where each **Node** represents a city.  
- Each **Node** has a vector of connected cities (`adj`), storing city names and road distances.  

📌 **File Handling (`Save()` & `Load()`)**:  
- 💾 `Save()`: Writes graph details into `Storage.txt`.  
- 📂 `Load()`: Reads from the file and reconstructs the graph in memory.  

📌 **User Interaction:**  
- ⌨️ The user can enter commands to **add/delete cities**, **add/delete roads**, **update graphs**, or **search for paths**.  
- 🔄 The program ensures **valid inputs** and prevents errors like duplicate cities or missing roads.  

📌 **Graph Algorithms:**  
- 🔍 `DFS(graphName, cityName)`: Recursively explores the graph.  
- 🚶 `BFS(graphName, source, destination, path)`: Finds the shortest path in unweighted graphs.  
- 🏎️ `Dijkstra(graphName, source, destination, path, totalDistance)`: Uses a **priority queue** (min-heap) to find the shortest path in weighted graphs.  
