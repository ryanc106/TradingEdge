<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trading Position Size Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
        }
        .container {
            max-width: 400px;
            margin: auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 10px;
            box-shadow: 2px 2px 12px rgba(0, 0, 0, 0.1);
        }
        input, button {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            font-size: 16px;
        }
        button {
            background-color: #28a745;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #218838;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Trading Position Size Calculator</h2>
        <label>Account Size ($):</label>
        <input type="number" id="accountSize" placeholder="Enter account size">
        
        <label>Risk Per Trade (%):</label>
        <input type="number" id="riskPercent" placeholder="Enter risk %">
        
        <label>Stop Loss ($):</label>
        <input type="number" id="stopLoss" placeholder="Enter stop loss">
        
        <button onclick="calculatePositionSize()">Calculate</button>
        
        <h3 id="result"></h3>
    </div>

    <script>
        function calculatePositionSize() {
            let accountSize = parseFloat(document.getElementById('accountSize').value);
            let riskPercent = parseFloat(document.getElementById('riskPercent').value);
            let stopLoss = parseFloat(document.getElementById('stopLoss').value);
            
            if (!accountSize || !riskPercent || !stopLoss) {
                document.getElementById('result').innerText = "Please fill in all fields";
                return;
            }
            
            let riskAmount = (riskPercent / 100) * accountSize;
            let positionSize = riskAmount / stopLoss;
            
            document.getElementById('result').innerText = `Position Size: ${positionSize.toFixed(2)} units`;
        }
    </script>
</body>
</html>
