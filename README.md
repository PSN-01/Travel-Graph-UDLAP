# Travel Graph UDLAP


This Google Colab notebook calculates and visualizes the shortest walking paths within the Universidad de las Américas Puebla (UDLAP) campus. Using OpenStreetMap data and Dijkstra’s algorithm, the notebook finds optimal pedestrian routes between specific campus locations provided in a CSV file.

At the beginning of the notebook, necessary libraries such as geopandas, shapely, networkx, matplotlib, and osmnx are installed. Then, the walking network graph around UDLAP is created and visualized. The notebook reads a CSV file containing the coordinates and names of important points on campus. Once this data is loaded, the user is prompted to choose an origin and destination from the dataset, and the notebook calculates the shortest route between them based on distance.

The main functionality is an interactive terminal where the user can repeat multiple trips by inputting different node IDs. Each path is displayed with segment-by-segment information including distance, speed, travel time, and the longest segment. All routes are plotted over the UDLAP campus walking graph and visualized in color.

# Flowchart

![Image](https://github.com/user-attachments/assets/8f801a47-a6bf-4f4a-8d68-f8f67e58c5de)

# How to Upload the CSV File to Google Colab

To run this notebook successfully, you need to upload the dataset in CSV format. Follow these steps carefully.

Step 1: Download the dataset in Excel format and make sure to save it as a CSV file (comma-separated values).

Step 2: Open the Colab notebook that was shared with you. On the left-hand side, click the small folder icon located in the upper-left corner. A sidebar will open. Inside that sidebar, click the "Upload file" button. A file selector will appear. Choose the CSV file you saved.

![Image](https://github.com/user-attachments/assets/b27e9123-cfd9-4572-95b5-6ce01f8ad66c)

Step 3: Once the file is uploaded, locate the following block of code in the notebook:

```python
path = r"/content/nodos_udlap - Hoja 1.csv"
df = pd.read_csv(path)
df
```

Step 4: Click the 3 dots in the CSV file you just uploaded, then click copy path and insert it inside the line:

```python
path = r"NEW PATH OF THE CSV FILE YOU JUST UPLOADED"
```

Step 5: Continue running each cell from top to bottom including the new path of the csv, in the notebook until you reach the main interactive route planner. This is where you’ll be asked if you want to start a new trip, and input the origin and destination vertex IDs.

Step 6: The final block of code handles the full route calculation, visualization, and statistics. You can perform multiple trips during one session. Once you’re done, the complete map with all routes will be displayed.

# FINAL OUTPUT

![Image](https://github.com/user-attachments/assets/a6aefc04-2be7-4f14-a188-3e861c880e21)

# Notes:

This notebook works entirely within Colab using publicly available map data and your uploaded CSV file. You don’t need to install anything locally. All paths are calculated using Dijkstra’s algorithm on a walkable graph generated from OpenStreetMap.

The interface is simple and interactive, designed so that users can explore routes through the UDLAP campus intuitively.

(Insert image showing the final route output, if available)

Project developed for academic and visualization purposes.

