# RDX-Run 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RDX Lottery Predictor</title>
    <style>
        body { text-align: center; font-family: Arial, sans-serif; background-color: black; color: white; }
        h1 { font-size: 40px; margin-top: 20px; }
        button { padding: 10px 20px; font-size: 18px; cursor: pointer; margin-top: 20px; }
    </style>
</head>
<body>
    <h1>🔥 RDX SE PANGA NAHI LENE KA 🔥</h1>
    <p>Lottery Predictor</p>
    <button onclick="predict()">Predict Next Lottery Result</button>
    <p id="result"></p>

    <script>
        function predict() {
            let history = JSON.parse(localStorage.getItem("lottery_history")) || [];
            if (!Array.isArray(history) || history.length < 5) {
                document.getElementById("result").innerText = "Not enough data";
                return;
            }

            let counts = {};
            history.forEach((num, index) => {
                let weight = index / history.length;
                counts[num] = (counts[num] || 0) + 1 + weight;
            });

            let maxFrequency = Math.max(...Object.values(counts));
            let mostFrequentNumbers = Object.keys(counts).filter(num => counts[num] === maxFrequency);
            mostFrequentNumbers = mostFrequentNumbers.filter(num => counts[num] > 1);

            let prediction = mostFrequentNumbers.length > 0
                ? mostFrequentNumbers[Math.floor(Math.random() * mostFrequentNumbers.length)]
                : "No strong prediction";

            document.getElementById("result").innerText = `Next Prediction: ${prediction}`;
        }
    </script>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RDX Lottery Predictor</title>
    <style>
        body { text-align: center; font-family: Arial, sans-serif; background-color: black; color: white; }
        h1 { font-size: 40px; margin-top: 20px; }
        button { padding: 10px 20px; font-size: 18px; cursor: pointer; margin-top: 20px; }
    </style>
</head>
<body>
    <h1>🔥 RDX SE PANGA NAHI LENE KA 🔥</h1>
    <p>Lottery Predictor</p>
    <button onclick="predict()">Predict Next Lottery Result</button>
    <p id="result"></p>

    <script>
        function predict() {
            let history = JSON.parse(localStorage.getItem("lottery_history")) || [];
            if (!Array.isArray(history) || history.length < 5) {
                document.getElementById("result").innerText = "Not enough data";
                return;
            }

            let counts = {};
            history.forEach((num, index) => {
                let weight = index / history.length;
                counts[num] = (counts[num] || 0) + 1 + weight;
            });

            let maxFrequency = Math.max(...Object.values(counts));
            let mostFrequentNumbers = Object.keys(counts).filter(num => counts[num] === maxFrequency);
            mostFrequentNumbers = mostFrequentNumbers.filter(num => counts[num] > 1);

            let prediction = mostFrequentNumbers.length > 0
                ? mostFrequentNumbers[Math.floor(Math.random() * mostFrequentNumbers.length)]
                : "No strong prediction";

            document.getElementById("result").innerText = `Next Prediction: ${prediction}`;
        }
    </script>
</body>
</html>
