# Weather Display Widget – A Mini React Project

A small React + Vite weather application that lets users search for a city and view its current weather details, including temperature, humidity, minimum/maximum temperature, and a short weather description. The app uses the OpenWeatherMap API and presents the result in a styled Material UI card with weather-based icons and background images.

## Features

- Search for any city by name
- Fetch live weather data from OpenWeatherMap
- Display current temperature in Celsius
- Show humidity, min/max temperature, and feels-like temperature
- Display a description of the current weather condition
- Use dynamic weather icons and image backgrounds based on conditions
- Built with React and Vite for a lightweight frontend setup

## Tech Stack

- React 19
- Vite 8
- JavaScript
- Material UI
- OpenWeatherMap API

## Project Structure

```text
Weather-Display-Widget--A-Mini-React-Project/
├── index.html
├── package.json
├── package-lock.json
├── vite.config.js
├── eslint.config.js
├── .gitignore
├── public/
│   ├── favicon.svg
│   └── icons.svg
├── src/
│   ├── App.css
│   ├── App.jsx
│   ├── InfoBox.css
│   ├── InfoBox.jsx
│   ├── SearchBox.css
│   ├── SearchBox.jsx
│   ├── WeatherApp.jsx
│   ├── index.css
│   └── main.jsx
└── README.md
```

## How It Works

The app is organized into a few main components:

- `App.jsx` renders the main weather application.
- `WeatherApp.jsx` manages the weather state and passes it to the UI components.
- `SearchBox.jsx` handles the input form and fetches weather data from OpenWeatherMap.
- `InfoBox.jsx` displays the weather result in a card layout.

The app stores the fetched weather data in React state and updates the UI whenever the user searches for a new city.

## Setup

1. Clone the repository.
2. Install dependencies:

```bash
npm install
```

3. Create a `.env` file in the root directory and add your OpenWeatherMap API key:

```env
VITE_WEATHER_API_KEY=your_api_key_here
```

> The app expects the environment variable name `VITE_WEATHER_API_KEY`.

4. Start the app in development mode:

```bash
npm run dev
```

5. Open the local Vite URL shown in the terminal to view the app in the browser.

## Available Scripts

```bash
npm run dev
npm run build
npm run preview
npm run lint
```

## API Usage

The app calls the OpenWeatherMap endpoint:

```text
https://api.openweathermap.org/data/2.5/weather
```

with the following parameters:

- `q` = city name
- `appid` = API key
- `units` = metric

This ensures temperature values are returned in Celsius.

## Example Behavior

When the user enters a city such as `London`, the app fetches weather data and displays:

- current temperature
- felt temperature
- minimum and maximum temperature
- humidity
- weather description

If the city is invalid or the API call fails, the app shows an error message:

```text
No such place exists!
```

## Notes

- The app is intentionally minimal and educational in scope.
- It demonstrates a typical React state-driven API integration.
- The default weather state is initialized to a sample value (`Wonderland`) until the user performs a search.

## License

This project is a small frontend mini-project and does not include a formal license file.

## Author

Created by Mohit Kholia.
