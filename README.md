# Mapper - a Graphical Information System (GIS) application

Overview:
  - A map application that turns binary data of a city into GIS with UI and various functionalities
  - Implemented with the easyGL library, which only allows basic graphical operations like drawing straight lines and coloring areas
  
Front end features optimized based on user expereince:
  - Sizes of objects (buildings, streets, grasslands etc.) based on user zooming level
  - Filtration of objects based on zoom level
      - Optimal filtration & zooming algorithm y = x ^ 0.66
  - Rendering of edges / curves
    
Back end algorithms & functionalities
  - Search: Allows user to search for specific streets / locations and auto zoom into the destination
    - Utilized vectors and multi maps to maximize the search speed
  - Path Finding: finds shortest path for any two chosen points on the map
    - Applied Dijkstra's Algorithm to the data structure designed for the map, achieved very satisfactory performance
    - Intergrated the solution with A-Star technique based on a physical euclidean distance heuristic, improved performance in most cases
  - Route planning: a similar traveling-salesman problem, resolved with an altered version of the path finding function

Implementation code are in libstreetmap/src

A more detailed final project report documentation: 
  https://docs.google.com/document/d/1DBmeeYcobygr-ExJpoWJ-o9VmCs3cj1OnHoJOy5E2Jo/edit?usp=sharing
