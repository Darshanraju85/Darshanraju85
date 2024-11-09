# Weather App

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Weather App</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div id="app">
        <h1>Weather App</h1>
        <input type="text" id="cityInput" placeholder="Enter city name" />
        <button id="getWeatherBtn">Get Weather</button>
        <div id="currentWeather">
            <h2>Current Weather</h2>
            <p id="weatherCondition"></p>
            <p id="temperature"></p>
            <p id="humidity"></p>
            <p id="windSpeed"></p>
            <p id="dateTime"></p>
        </div>
        <div id="forecast">
            <h2>7-Day Forecast</h2>
            <canvas id="weatherChart"></canvas>
        </div>
    </div>
    <script src="app.js"></script>
</body>
</html>M
<!---
Darshanraju85/Darshanraju85 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

Css-code:-

body {
    font-family: Arial, sans-serif;
    margin: 10px;
    padding: 20px;
    background-color: #f8f0f0;
}

.app {
    max-width: 800px;
    margin: auto;
    padding: 20px;
}

.weather-form {
    display: flex;
    justify-content: space-between;
}

.weather-form input {
    flex: 1;
    padding: 10px;
    font-size: 16px;
}

.weather-form button {
    padding: 10px 20px;
    font-size: 16px;
    background-color: #007bff;
    color: white;
    border: none;
    cursor: pointer;
}

.weather-form button:hover {
    background-color: #0056b3;
}

.weather-display {
    margin-top: 20px;
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 2px 10px rgba(138, 243, 243, 0.1);
}

.weather-display h2 {
    margin: 0;
}

.weather-display ul {
    list-style-type: chrome;
    padding: 12;
}

.weather-display li {
    margin: 10px ;
}

/* Responsive Styles */
@media (max-width: 600px) {
    .weather-form {
        flex-direction: column;
    }

    .weather-form input {
        margin-bottom: 20px;}
there is an error in these code[if anyone can want to clear that please contect darshanraju587@gmail.com]

/jscode:-

jsx
import React, { useState } from 'react';
import axios from 'axios';
import WeatherForm from './components/WeatherForm';
import WeatherDisplay from './components/WeatherDisplay';

const App = () => {
    const [weatherData, setWeatherData] = useState(null);

    const fetchWeather = async (city) => {
        const apiKey = 'YOUR_API_KEY'; // Replace with your actual API key
        const response = await axios.get(`https://api.weatherapi.com/v1/forecast.json?key=${apiKey}&q=${city}&days=7`);
        setWeatherData(response.data);
    };

    return (
        <div className="app">
            <WeatherForm onSearch={fetchWeather} />
            <WeatherDisplay weatherData={weatherData} />
        </div>
    );
};

export default App;

if anyone want to change take your time to make changes in that.
