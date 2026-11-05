# TEB2023_ARTIFICIAL INTELLIGENCE LAB TASKS
Author:Chua Xin Ying
## Repository Structure

### Lab 1 Search Foundations:lab01_search_foundations.ipnb
-Cleaned the airport and route data into one graph and ran BFS, DFS and UCS on three queries (KUL-KEF, SIN-EZE, NRT-CPT). BFS gives the fewest flights, UCS gives the shortest distance, and DFS gives long routes that change with neighbour order.

### Lab 2 Heuristic Search: lab02_informed_search_worked.ipnb
-Added a Haversine (straight-line distance) heuristic and ran Greedy Best-First Search and A*, then compared them with UCS. The heuristic never overestimates (0 violations in 30 checks). A* matched UCS's optimal cost with about 96% fewer expanded states. GBFS was fastest but up to 9% longer. Inflating the heuristic (weighted A*) lost the optimality guarantee.

### Lab 3 Search Engineering: lab03_search_engineering_worked.ipnb
-Turned the code into a tested package: all five algorithms return the same `SearchResult`, 8 unit tests pass without any dataset, and a command-line tool reproduces the Lab 2 route. A* matched UCS on cost every time with far fewer expansions, and GBFS was costlier on 7 of 10.

### Lab 4 Fuzzy Logic and ANFIS: lab04_fuzzy_anfis_worked.ipynb

-Built a Mamdani fuzzy controller (temperature and humidity to ventilation %) and a Sugeno ANFIS for CO prediction on the UCI Air Quality data.

#### Lab 5 Robotics Sensor Control: lab05_robotics_sensor_control_worked.ipynb
-Learned a wall-following controller for a SCITOS G5 robot from 24 ultrasonic sensors. A four-sensor decision tree gave readable rules at about 92% accuracy (0.90 macro F1) versus 99% for a random forest on all sensors, but its F1 fell to 0.71 under 10% sensor noise.

#### Lab 6 Handwriting OCR Evaluation: lab06_handwriting_ocr_worked.ipynb
-Benchmarked Tesseract OCR on 89 handwritten medicine-name images. Raw images gave 0% exact match, 0.875 character error rate and 39 blank predictions; a grayscale, border and resize pipeline cut blanks to 15 and CER to 0.788, but only 1 of 89 names was read exactly, because the engine still can't handle cursive.
