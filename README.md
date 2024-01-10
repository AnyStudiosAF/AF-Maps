# Interactive Map JavaScript Code

This code is created to generate an interactive world map with different data visualization layers. Here is a brief overview of its main functionalities:

## Variables

- **triggerColor**: A string that represents the main color code - `#004C78`.
- **pickedColor**: A placeholder variable for dynamic colors in the application.
- **maps**: An array to keep all the SVG codes of different maps - they're imported from Figma.
- **countries**: An array of countries to be used in the interactive map.
- **colors**: An array of string hex color codes that is used to show different categories on the map.

## Procedures

Open the webpage, automatically, the map corresponding to the last item in the dataTriggers array is loaded. The dataTriggers from the navigation items are made active and an eventListener is added to each item.

When a mouseover event occurs on a navigation item, it triggers a function that loads a different SVG map and modifies key attributes about the clicked item. For every country in the `countries` array, a "mouseover" and "mouseout" eventListener is added.

Moreover, clicking on a specific country opens a new webpage `/countries/{country-name}` - where `{country-name}` represents the ID of the country element in the SVG.

## Event Handlers

- **handleMapContainerMouseEnter()**: Triggered when the mouse enters the mapContainer. It finds elements with IDs containing "Dot" or "dot" and sets pointer-events: none. It also logs the `<g>` for each matching country in the list.
- **handleCountryMouseOver()**: Triggered when the mouse hovers over a country. It handles the dynamic color-fill properties and interaction of specific paths within a country's `<g>` SVG element.
- **handleCountryMouseOut()**: Triggered when the mouse no longer hovers a country. It returns the color of the specific paths to the initial state and removes any active `href`.

The map changes and reacts to a different layer/category selection - representing the active category in a different color and the selected country with its dwell map details. Also, it enables navigation to a specific country's details page.
