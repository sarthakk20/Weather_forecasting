#JS

```script.js

document.getElementById('getWeather').addEventListener('click', function() {
    const city = document.getElementById('city').value;
    const APIKey = '2675a0482e5c8100dce84fc9f2ecfe88'; 
    const apiUrl = `https://api.openweathermap.org/data/2.5/weather?q=${city}&units=metric&appid=${APIKey}`;

    fetch(apiUrl)
        .then(response => response.json())
        .then(data => {
            const weatherData = document.getElementById('weatherData');
            // console.log(data);
            if (data.cod === 200) {
                weatherData.innerHTML = `
                    <h2 id="cityName">${city}, ${data.sys.country}</h2>
                    <h3 id="h3">Temperature: ${data.main.temp} °C</h3>
                    <p>weather: ${data.weather[0].description}</p>
                    <p>Humidity: ${data.main.humidity}%</p>
                    <p>Wind Speed: ${data.wind.speed} m/s</p>
                `
            } else if(city === "") {
                weatherData.innerHTML = `<h4>Please enter city name </h4>`;
            }
            else{
                weatherData.innerHTML = `<h4>City not found</h4>`;
            }
        })
        .catch(error => {
            console.error('Error fetching the weather data:', error);
            document.getElementById('weatherData').innerHTML = `<p>Error fetching the weather data</p>`;
        });
});
```