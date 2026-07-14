# AI Coding Guidelines for Map Generation Exercise

## Project Overview
This repository contains a Jupyter notebook exercise (`DV0101EN-Exercise-Generating-Maps-in-Python.ipynb`) for creating interactive maps in Python, part of the IBM Data Science Capstone course. The focus is on geospatial data visualization using the Folium library.

## Architecture
- **Single Notebook Structure**: All code resides in one Jupyter notebook with sequential cells for learning and exercises.
- **Data Flow**: Load geospatial data (e.g., CSV with lat/lng) into pandas DataFrames, then visualize on Folium maps.
- **Key Components**: Map creation, markers, circles, choropleths, and marker clusters for handling large datasets.

## Essential Libraries and Patterns
- **Folium**: Core for maps. Create base maps with `folium.Map(location=[lat, lng], zoom_start=10)`. Add features like `folium.Marker([lat, lng], popup='text').add_to(map)`.
- **Pandas**: Data manipulation. Read data with `pd.read_csv()`, filter coordinates, and pass to map features.
- **Numpy/Matplotlib**: Supporting libs for data processing and basic plots.
- Example: In [cell 15](DV0101EN-Exercise-Generating-Maps-in-Python.ipynb#L210-L214), create a world map: `world_map = folium.Map()`.

## Developer Workflows
- **Execution**: Run cells in order using Jupyter. Cells depend on previous executions (e.g., imports, data loading).
- **Package Installation**: Use `!pip install folium pandas numpy` in notebook cells for dependencies.
- **Data Sources**: Often use sample data like San Francisco incidents or world coordinates; load from URLs or local files.
- **Output**: Maps render inline in Jupyter; save as HTML with `map.save('filename.html')` if needed.

## Project-Specific Conventions
- **Variable Naming**: Maps named like `world_map`, `sanfran_map`; data like `df_incidents`; coordinates as `latitude`, `longitude` lists.
- **Map Customization**: Use tiles like 'Stamen Toner' for different styles; add layers for overlays.
- **Error Handling**: Folium handles invalid coordinates gracefully; validate data before mapping.
- **Performance**: For many markers, use `folium.plugins.MarkerCluster` to group points, as in [cell 23](DV0101EN-Exercise-Generating-Maps-in-Python.ipynb#L313-L327).

## Integration Points
- **External Data**: Fetch from web (e.g., GeoJSON for choropleths) or use provided datasets.
- **No APIs**: Pure client-side rendering; no server dependencies.
- **Export**: Maps are self-contained HTML files for sharing.

Reference: [Main Notebook](DV0101EN-Exercise-Generating-Maps-in-Python.ipynb)</content>
<parameter name="filePath">c:\Docs\Courses\DSCapstone\.github\copilot-instructions.md