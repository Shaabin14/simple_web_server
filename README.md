# EX01 Developing a Simple Webserver

# Date:
 02/10/24
# AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

# DESIGN STEPS:
## Step 1:
HTML content creation.

## Step 2:
Design of webserver workflow.

## Step 3:
Implementation using Python code.

## Step 4:
Serving the HTML pages.

## Step 5:
Testing the webserver.

# PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Power Calculator</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <div class="container">
        <h1>Power Calculator</h1>
        <form id="powerForm">
            <label for="intensity">Intensity (I):</label>
            <input type="number" id="intensity" name="intensity" placeholder="Enter intensity (in amperes)" required>
            
            <label for="resistance">Resistance (R):</label>
            <input type="number" id="resistance" name="resistance" placeholder="Enter resistance (in ohms)" required>
            
            <button type="button" onclick="calculatePower()">Calculate Power</button>
        </form>
        <div class="result" id="result"></div>
    </div>
    <script>
        function calculatePower() {
            // Get input values
            const intensity = parseFloat(document.getElementById('intensity').value);
            const resistance = parseFloat(document.getElementById('resistance').value);

            // Validate inputs
            if (isNaN(intensity) || isNaN(resistance) || intensity <= 0 || resistance <= 0) {
                document.getElementById('result').innerHTML = "Please enter valid positive numbers for intensity and resistance.";
                return;
            }

            // Calculate power
            const power = intensity * intensity * resistance;

            // Display result
            document.getElementById('result').innerHTML = `Power (P) = ${power.toFixed(2)} watts`;
        }
    </script>
</body>
</html>
CSS
body {
    font-family: Arial, sans-serif;
    background-color: #f9f9f9;
    margin: 0;
    padding: 20px;
}
.container {
    max-width: 500px;
    margin: 50px auto;
    background: #fff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}
h1 {
    text-align: center;
    color: #333;
}
label {
    display: block;
    margin: 10px 0 5px;
    font-weight: bold;
}
input[type="number"] {
    width: 100%;
    padding: 10px;
    margin-bottom: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
}
button {
    width: 100%;
    background-color: #4CAF50;
    color: white;
    padding: 10px;
    border: none;
    border-radius: 5px;
    font-size: 16px;
    cursor: pointer;
}
button:hover {
    background-color: #45a049;
}
.result {
    margin-top: 20px;
    font-size: 18px;
    text-align: center;
    color: #333;
}

```
# OUTPUT:
![Screenshot 2024-12-08 122520](https://github.com/user-attachments/assets/4df0696b-0ae9-4160-a2b0-3a63f584ee00)

# RESULT:
The program for implementing simple webserver is executed successfully.
