# Case Study: Build a Componentized New Tab Page

Objective
Recreate a lightweight, componentized version of a browser new tab page using Vue.js and
Nuxt. The goal is to test your ability to build UI from spec, use reusable components, and
manage data rendering and tracking interactions.

## Requirements

Core Features

1. Search Bar (functional)

    - Centered input field with placeholder: “Search the web or type a URL”.
    - On submission, redirect the user to a Yahoo search results page using their
query. Example: https://search.yahoo.com/search?p=searchterm

1. Quick Link Tiles (Top Icons)
    - Load icons data server side.
    - Render a row of 6 app icons: e.g. Facebook, YouTube, Spotify, Dribbble, PayPal, and one “+” button.
    - Icons should be reusable components and link to related external sites.
1. Tab-Based Newsfeed Navigation

    - Categories: Home, News, Sports, Money, Lifestyle, Politics, Health, Food,
Entertainment. Clicking each tab should load the corresponding feed data
1. News Tiles
    - Use mock data to display:
        - Title
        - Source (e.g., earlychip.com)
        - Optional tag (e.g., “Sponsored”)
        - Timestamp or story meta
    - Include a featured tile (larger) and standard tiles (smaller).
    - Include a “Related Stories” section as seen in the screenshot below.

1. Interaction Tracking

    - Fire a tile_shown event/log when a tile becomes visible (use
IntersectionObserver).
    - Fire a tile_clicked event/log when a tile is clicked.

## Technical Requirements

    - Use Vue + Nuxt
    - Create reusable components: AppIcon.vue, NewsTile.vue, TabNav.vue, etc.
    - No need to build real APIs — use mock data and simulate the calls
    - Basic responsive layout is required. Page should render properly on mobile devices as
well as desktop.
    - All external API calls should happen once on the server-side and hydrate correctly on
the client.
    - Feel free to add any enhancements or extra features that would improve the user
experience.
