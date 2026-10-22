# TEB2023_ARTIFICIAL INTELLIGENCE LAB TASKS
Author:Chua Xin Ying
## Repository Structure

### Lab 1 Search Foundations:lab01_search_foundations.ipnb
-Cleaned the airport and route data into one graph and ran BFS, DFS and UCS on three queries (KUL-KEF, SIN-EZE, NRT-CPT). BFS gives the fewest flights, UCS gives the shortest distance, and DFS gives long routes that change with neighbour order.

### Lab 2 Heuristic Search: lab02_informed_search_worked.ipnb
-Added a Haversine (straight-line distance) heuristic and ran Greedy Best-First Search and A*, then compared them with UCS. The heuristic never overestimates (0 violations in 30 checks). A* matched UCS's optimal cost with about 96% fewer expanded states. GBFS was fastest but up to 9% longer. Inflating the heuristic (weighted A*) lost the optimality guarantee.

### Lab 3 Search Engineering: lab03_search_engineering_worked.ipnb
-Turned the code into a tested package: all five algorithms return the same `SearchResult`, 8 unit tests pass without any dataset, and a command-line tool reproduces the Lab 2 route. A* matched UCS on cost every time with far fewer expansions, and GBFS was costlier on 7 of 10.
