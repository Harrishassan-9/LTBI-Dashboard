# LTBI-Dashboard

Data Cleaning and Pre-Processing:
The dataset tb_2022-09-30.csv was cleaned and preprocessed to prepare it for further
analysis. Missing values were handled by replacing them with appropriate substitutes;
numeric columns had missing values filled with their respective column means, whilemissing values in the iso2 column were replaced with "NA". Outlier detectionandremoval were performed on numeric columns using the Interquartile Range (IQR)
method. Rows with values outside the range of Q1−1.5×IQRQ1 - 1.5 \times
IQRQ1−1.5×IQR and Q3+1.5×IQRQ3 + 1.5 \times IQRQ3+1.5×IQR were identifiedand excluded. While the initial plan included standardizing the numeric columns using the Z-scoremethod, this step was commented out, leaving the data in its unstandardized form. The cleaned dataset, free of outliers and missing values, was savedas
Cleaned_Final.csv for subsequent use. These preprocessing steps ensure that thedataset is clean, consistent, and ready for analysis or modeling.

Main Page:
The provided HTML document creates a visually appealing webpage withabackground image and a fixed navigation bar at the top. The page has a smooth fadein and fade-out effect, enhancing the user experience during page transitions. Thenavigation bar, which is always visible at the top of the page, includes links to various
pages, such as "Force-Directed Graph", "Map Chart", "Timeline Visualization", "Hierarchical Tree Map", "Sunburst Chart" and “Dashboard”. These links are styledwith a transparent background, rounded edges, and a hover effect that highlights thelinks when the mouse pointer hovers over them. The main content area is centered within the page, ensuring that it does not overlapwith the navigation bar. The page is designed to use the entire viewport, andthebackground image is set to cover the screen, ensuring a consistent, visually appealingdesign. The fade-out effect is triggered when any navigation link is clicked, and after
a slight delay matching the duration of the fade-out animation, the page transitions tothe link's destination. This provides a smooth and visually rich experience for users as
they navigate between different visualizations on the website. The JavaScript functionality manages the smooth page transitions by preventingthedefault navigation behavior and applying the fade-out class to the body. Whenthenew page loads, the fade-out class is removed to restore the normal opacity. This
seamless integration of transitions creates an elegant user experience as users exploredifferent types of visualizations provided on the site.

Visualization Report: Force-Directed Graph with ZoomandPan:
The force-directed graph visualization is an interactive and dynamic tool createdusing D3.js to explore relationships and connections between entities representedas
nodes and links. The graph employs a force simulation to position nodes, balancinglink forces, charge repulsion, collision avoidance, and centering to ensure anaesthetically pleasing layout. Users can interact with the graph through zooming, panning, and dragging nodes, allowing detailed exploration of complex networks. Clicking on a node toggles its expanded state, visually highlighting related nodes andlinks for better analysis. The visualization features a gradient backgroundtransitioning from light blue to dark blue, enhancing its visual appeal. Nodes arestyled with a default teal color, transitioning to orange with black outlines whenexpanded, while links are color-coded based on relationship types for clarity. The tooltip dynamically displays node-specific information when a node is expanded, adjusting its position to follow the cursor for user convenience. The graph retrieves its
data from a server endpoint, enabling real-time updates and flexibility in datasets. Robust event handling is implemented to support interactions like dragging, zooming, and node expansion, while error handling ensures smooth operation by logging dataloading issues. This visualization is highly applicable in various domains, suchas
social network analysis, knowledge graphs, supply chain management, and biological
networks, offering insights into complex relationships through an engagingandintuitive interface. It is a modern and efficient tool that combines technical
functionality with user-centric design to meet the needs of diverse analytical tasks.

Hierarchical treemap visualization:
The HTML document creates an interactive hierarchical treemap visualization usingD3.js to display tuberculosis (TB) cases across different regions and countries. Thepage has a dark background with the main heading "Hierarchical Tree Map of TBCases" positioned at the top. Below this, the treemap chart is displayed on the left, and a legend showing the regions' full names is placed on the right. The chart allows
for zooming functionality with "Zoom In" and "Zoom Out" buttons, which adjust thescale of the treemap. The treemap itself represents TB case data, where each rectanglecorresponds to a country, and its size is proportional to the number of TBcases. Thecolor of each rectangle is based on its region, with a color scale that differentiates
regions like Africa, Americas, Europe, and others. Additionally, the user can hover
over the legend items to highlight specific regions in the treemap, providing a moreinteractive and intuitive data exploration experience. The treemap is designed to provide a clear overview of TB cases globally, withdetailed labels showing the region and country names for better readability. The zoomfunctionality allows for enhanced navigation within the treemap, making it easier toexplore specific regions or countries in greater detail. This visualization is a useful
tool for understanding the distribution of TB cases worldwide, making it easytoidentify high-burden regions and countries.

Map Chart:
The provided HTML code represents a web page that displays a map with countrymarkers, specifically showing countries affected by tuberculosis (TB). The mapis
built using the Leaflet.js library, which is a powerful tool for embedding interactivemaps on websites. The map is centered globally at a default zoom level of 2, allowingfor an overview of all the countries. The map tiles are sourced from OpenStreetMap, awidely-used, free mapping platform. The code defines a set of coordinates for various countries using a JavaScript object, countryCoords, which maps each country to its respective latitude and longitude. These coordinates are then used to position markers on the map. The map's markers
are color-coded based on the number of new TB cases reported in each country, withcolors ranging from green (for fewer cases) to orange and red (for higher case counts). The markers themselves are circle-shaped and dynamically placed based onthecoordinates of each country. Additionally, each marker is clickable and displays apopup with the country's name and the number of new TB cases, allowing users tointeract with the map and view the data in more detail. The data, includingthemarkers' country names and TB case numbers, is dynamically passed to the map froma Flask backend through the markers variable. This integration allows the map tobeupdated with data provided by the server, making it adaptable to real-time datachanges.

Time-Line Visualisation:
The HTML page is designed to visualize an animated timeline using D3.js. It loads
data from a server endpoint (/tv_data) and uses this data to generate an interactive andanimated graph. The timeline visualizes data points as circles whose size is
dynamically adjusted based on a value (tot.newrel) from the dataset, and their positionon the graph is determined by other numerical columns (new.sp and tot.newrel). Users
can interact with the graph using a range slider, which allows themto select a year
and update the graph accordingly. Additionally, a play button enables an automaticplayback of the timeline, updating the graph year by year. The graph also includes
tooltips that provide more detailed information when users hover over the data points, showing attributes like the region, new SP, and total new release values. A color scale is applied to the data points, with different colors representing different
regions. The legend at the top of the page corresponds to these regions, providingavisual cue to help users identify the color associations. The page also includes
responsive features, such as margin adjustments for the graph, to ensure a smoothuser
experience across different screen sizes. This interactive timeline provides a clear andengaging way to visualize and explore trends over time, with the ability to playthrough the years or manually select a specific year.

Sun Burst:
The provided HTML code creates a web page that displays a Sunburst Chart usingPlotly. The page consists of a title, "Sunburst Chart," and a section where the chart's
HTML content is dynamically embedded through a placeholder
({{ chart_html|safe }}). This placeholder allows the chart to be rendered correctly, with the content passed from a backend framework. Additionally, there is a linkthat
allows users to navigate back to the homepage. The structure is designedfor
integration with a server-side application like Flask or Django to display the chart.

Dashboard:
The dashboard for data visualization is designed as an integrated platformthat
combines multiple visual representations into a cohesive interface. Access tothedashboard is facilitated by a dedicated Dashboard button placed on the main page. When this button is clicked, it redirects users to the dashboard page, where all
visualizations are showcased. The dashboard incorporates five distinct visualizations, each serving a unique purposein presenting complex datasets effectively. These visualizations include:
 Force-Directed Graph: This visualization illustrates relationships and connections
within the data in a dynamic and interactive manner. Nodes and links arearranged using force simulation to emphasize their interdependencies.  Map Chart: This component displays geographical data, effectively mappingcountries and their associated values (e.g., TB cases). It provides users withaclear spatial understanding of data distribution.  Hierarchical Layout: Representing hierarchical datasets, this visualization allows
users to explore data structures, such as parent-child relationships, in a tree-likeformat.  Timeline Visualization: This component uses an animated timeline to highlight
temporal data trends, enabling users to analyze changes over time interactively.  Sunburst Chart: The Sunburst Chart represents data hierarchies and proportions
through a circular layout. It provides zooming and panning capabilities for a morefocused analysis. These visualizations are seamlessly integrated into the dashboard using a combinationof HTML for structure and SVG for rendering graphical elements. The design ensures
that all components are well-aligned and displayed responsively, providing a userfriendly experience. Each visualization occupies a designated area withinthedashboard, ensuring clarity and accessibility. By combining these diverse visualization methods on a single page, the dashboardserves as a powerful tool for comprehensive data analysis, enabling users to interact
with and interpret data from multiple perspectives.
