# Understanding the UI Components of Search

In this section we look at the various UI components commonly utilized in building a search engine. We will initially base our discussion on the components provided by [Pre-Built Search Component Libraries](./ui-component-libraries-for-search.md).

## Core Components

### Search Box
This is the main input field where a user enters their queries.

### Search Results
This is the area where search results are displayed. It typically includes a list of items with titles, descriptions, and other relevant information.

#### Result Item (Hit)
This is an individual search result displayed within the search results. It usually includes a title, description, and other relevant information.

### Pagination
Pagination allows users to navigate through multiple pages of search results.

### Per Page
This is a dropdown menu that allows users to select the number of search results displayed per page.

### Facets (Refinements, Filters)
Facets are used to refine search results. They are typically displayed as a list of checkboxes or radio buttons that allow users to filter search results by various criteria such as category, price, date, etc.

#### Types of Facet
- Radio Buttons
- Checkboxes
- Hierarchical
- Range (slider)
- Rating
- Toggle

#### Selected Facets (Active Filters)
This is a list of the currently selected facets. It is usually displayed above the search results and allows users to easily remove filters.

### Sort By
Generally this is a dropdown menu that allows users to sort search results by various criteria such as relevance, date, popularity, etc. but sometimes it may be radio buttons or similar.

## Optional Components
- Breadcrumbs
- Geographic
- History
- Menus
- Multi-Select Items
- Stats
- Related Items
- Tag Cloud
- Date Picker
- Tree View
- Tag Filters

## Functionality
- Autocomplete (Typeahead)
- Conditional Facets
- Grouping Results
- Highlight
- Search-as-you-type
- Snippet
- Suggestions
- Voice Search

## UI Elements
- Input Box
- Button
- List
- Checkbox
- Range Slider
- Radio Button
- Dropdown

## Resources
- [InstantSearch.js UI Library Widgets](https://www.algolia.com/doc/api-reference/widgets/js/).
- [ReactiveSearch Components](https://docs.reactivesearch.io/docs/reactivesearch/react/overview/components/).
    - They have sub-pages for each type of component and this includes a screenshot of the visual appearance of the component, which can be quite helpful.
- [Elastic Search UI Components](https://docs.elastic.co/search-ui/api/react/components/search-box)
- David Ubersky's article [Search UI Patterns: Elements](https://ddsky.medium.com/search-ui-patterns-elements-80ea9d241f97)

### Generic Component Libraries
Just a few sample UI component libraries that may be worth consideration. Not meant to be representative or exhaustive.

#### General
- [Bootstrap](https://getbootstrap.com/)
- [Semantic UI](https://semantic-ui.com/)
    - Has some components specifically dedicated to search.
- [Shoelace](https://shoelace.style/)

#### Angular
- [PrimeEng](https://primeng.org/)

#### React
- [Material UI (MUI)](https://mui.com/material-ui/all-components/)
- [MP React Components](https://materialsproject.github.io/mp-react-components/?path=/story/introduction-mp-react-components--page)
    - Focused on material sciences.
- [Chakra](https://chakra-ui.com/docs/components)
- [Radix](https://www.radix-ui.com/)
    - Headless UI.
- [React Bootstrap](https://react-bootstrap.github.io/)

#### Vue
- [PrimeVue](https://primevue.org/)
    - Has DataTable and DataView.