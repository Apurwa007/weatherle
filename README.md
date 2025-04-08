
# Weather Dashboard Application

Stay informed with real-time and forecasted weather data in a beautifully designed React-based dashboard.

---

## Table of Contents

- [Overview](#overview)
- [Built With](#built-with)
- [Features](#features)
- [Project Structure](#project-structure)
- [API Integration](#api-integration)
- [Installation](#installation)
- [Examples](#examples)
- [Troubleshooting](#troubleshooting)

---

## Overview

This is a **Weather Dashboard Application** designed to provide users with up-to-date and comprehensive weather information. With a user-friendly interface and intuitive features, the app offers real-time data, search capabilities, and forecast views to help users stay weather-aware.

---

## Built With

- React.js
- Vite
- CSS Modules
- Context API
- OpenWeatherMap API
- ESLint & Prettier for linting and formatting
- Custom Design by the developer

---

## Features

- 🌍 Default city: Bhubaneswar, Orissa with real-time weather updates.
- 📍 Geolocation-based weather when you click the **Current Location** button.
- 🔍 Search for any city to view weather data instantly.
- 🌅 Today's Highlights: sunrise, sunset, humidity, pressure, visibility, and “feels like” temperature.
- 📅 3-hour interval forecasts and wind speeds.
- 🗓️ 5-day weather forecast.
- 🌗 Light/Dark mode toggle with preference saved via local storage.

---

## Project Structure

src/ : Source code directory
  - assets/ : Image files, stylesheets, or other static assets
  - components/ : React components
    - ComponentName.jsx : component
    - ComponentName.module.css : Stylesheet for the component using CSS modules
  - context/ : Context providers for the Context API
  - Hooks/ : some custom hooks i needed
  - App.jsx : Main application component which is the <Layout />
  - index.css : Global stylesheet
  - main.js : Entry point of the application
- public/ : Public assets and index.html
- .eslintrc.cjs : ESLint configuration file
- .env.local : Local environment variables (sensitive, not committed to version control)
- vercel.json : Vercel configuration file
- package.json : Project configuration and dependencies
- vite.config.js : Vite configuration file
- README.md : This file

---

## API Integration

The Weather Dashboard uses OpenWeatherMap API for fetching weather data.

### Fetching Weather Data

```javascript
const apiKey = "YOUR_API_KEY";
const city = "YourCity";

fetch(
  `https://api.openweathermap.org/data/2.5/weather?q=${city}&appid=${apiKey}`
)
  .then((response) => response.json())
  .then((data) => displayWeather(data))
  .catch((error) => console.error("Error:", error));
```

---

## Installation

To set up and run the Weather Dashboard locally with an API key, follow these steps:

bash
git clone https://github.com/Apurwa007/weatherle.git
cd your-project-directory
echo "REACT_APP_OPENWEATHERMAP_API_KEY=your-api-key-here" > .env
npm install && npm run dev


Replace your-project-directory with the actual name of your project
directory, and replace your-api-key-here with your OpenWeatherMap API key.

---

## Examples

- Navigate to the site, and you’ll see Cairo's weather by default.
- Use the **Search Bar** to look up other cities.
- Click the 🌞 or 🌜 icon to toggle themes.
- Use **Current Location** to fetch your local weather instantly.

---

## Troubleshooting

- Ensure your `.env.local` file is correctly named and placed.
- If the weather isn't updating, check the API key and limit rate.
- For deployment on Netlify, remember to add your API key in the **project settings** under **Environment Variables**.

---
