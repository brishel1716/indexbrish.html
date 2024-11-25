<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IP and Weather Info</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #ADD8E6; /* Light Baby Blue */
        }
        img {
            width: 300px;
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <h1>JavaScript & API's</h1>
    <p>With basic knowledge of JavaScript and API's I can find out:</p>

    <!-- New Image at the Top -->
    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ1DmLCy9PSJfFqO55mNTYOQLx3x8THsbokkw&s" alt="API Concept">

    <h1>IP and Weather Information</h1>
    <p>Your Public IP Address: <span id="ip-address"></span></p>
    <p>Your Location: <span id="location"></span></p>
    <p>Weather at Your Location: <span id="weather">Sunny, 29°C</span></p>
    <p>Weather at Your ISP Location: <span id="isp-weather">Partly Cloudy, 28°C</span></p>

    <script>
        // Example with only IP and Location fetching
        fetch('https://api.ipify.org?format=json')
            .then(response => response.json())
            .then(data => {
                // Display Public IP Address
                document.getElementById('ip-address').textContent = data.ip;

                // For this example, set static location since weather is predefined
                const location = "Teakettle Village, Cayo District, Belize";
                document.getElementById('location').textContent = location;
            })
            .catch(error => console.error('Error:', error));
    </script>

    <!-- New Image at the Bottom -->
    <img src="https://img.freepik.com/premium-vector/computer-with-api-concept-modern-technologies-innovations-cloud-service-data-exchange-storage-with-information-computer-monitor-with-server-cartoon-flat-vector-illustration_118813-15996.jpg" alt="API Concept">
</body>
</html>
