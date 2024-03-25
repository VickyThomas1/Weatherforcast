# Weatherforcast
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Weather Prediction</title>
</head>
<body>
    <h1>Weather Prediction</h1>
    <form id="weatherForm">
        <label for="temperature">Temperature:</label>
        <input type="number" id="temperature" name="temperature" required>
        <button type="submit">Predict Weather</button>
    </form>

    <div id="predictionResult" style="display: none;">
        <h2>Prediction Result:</h2>
        <p id="weatherPrediction"></p>
    </div>

    <script>
        document.getElementById("weatherForm").addEventListener("submit", function(event) {
            event.preventDefault(); // Prevent form submission
            // Get the temperature value entered by the user
            var temperature = parseFloat(document.getElementById("temperature").value);
            // Perform the weather prediction based on temperature
            var weatherPrediction = temperature >= 25 ? "Sunny" : "Rainy";
            // Display the prediction result
            document.getElementById("weatherPrediction").textContent = "Predicted Weather: " + weatherPrediction;
            document.getElementById("predictionResult").style.display = "block";
        });
    </script>
</body>
</html>
