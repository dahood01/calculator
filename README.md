<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #ff9292;
            padding: 50px;
        }
        .calculator {
            background: rgb(255, 255, 255);
            padding: 20px;
            border-radius: 10px;
            display: inline-block;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
        }
        input {
            font-size: 20px;
            width: 100px;
            text-align: center;
            margin: 10px;
        }
        button {
            font-size: 20px;
            margin: 5px;
            padding: 10px 20px;
            border: none;
            background-color: #28a745;
            color: white;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #236832;
        }
        #result {
            font-size: 24px;
            margin-top: 10px;
        }
    </style>
</head>
<body>

    <h1>Simple Calculator</h1>
    <div class="calculator">
        <input type="number" id="num1" placeholder="Enter number">
        <input type="number" id="num2" placeholder="Enter number">
        <br>
        <button onclick="calculate('add')">Add (+)</button>
        <button onclick="calculate('subtract')">Subtract (-)</button>
        <p id="result">Result: 0</p>
    </div>

    <script>
        function calculate(operation) {
            let num1 = parseInt(document.getElementById("num1").value);
            let num2 = parseInt(document.getElementById("num2").value);
            let result = 0;

            if (operation === 'add') {
                result = num1 + num2;
            } else if (operation === 'subtract') {
                result = num1 - num2;
            }

            document.getElementById("result").textContent = "Result: " + result;
        }
    </script>

</body>
</html>

